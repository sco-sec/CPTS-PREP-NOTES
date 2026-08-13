# 📋 Module Overview

## 🎯 Overview

This module covers comprehensive Linux privilege escalation techniques, methodologies, and tools. Linux privilege escalation is a critical skill for penetration testers, as it allows gaining elevated access on compromised Linux systems through various attack vectors.

> **⚠️ Note**: Module includes advanced kernel exploitation techniques that should be used with extreme caution and proper understanding of system stability risks.

## 📚 Module Structure

```
linux-priv-esc/
├── README.md                          # This overview file
├── environment-enumeration.md         # System reconnaissance and information gathering
├── services-internals-enumeration.md # Deep system analysis and service enumeration
├── credential-hunting.md              # Systematic credential discovery across file system
├── path-abuse.md                      # PATH variable manipulation and command hijacking
├── wildcard-abuse.md                  # Wildcard character exploitation for privilege escalation
├── escaping-restricted-shells.md      # Techniques for breaking out of restricted shells
├── special-permissions.md             # SUID/SGID binary exploitation and GTFOBins
├── sudo-rights-abuse.md               # Sudo privilege misconfigurations and GTFOBins exploitation
├── privileged-groups.md               # LXD, Docker, Disk, ADM group privilege escalation
├── capabilities.md                    # Linux capabilities privilege escalation exploitation
├── vulnerable-services.md             # Known service vulnerabilities and exploitation
├── cron-job-abuse.md                  # Cron job misconfiguration exploitation
├── lxd-container-escape.md            # LXD container privilege escalation exploitation
├── docker-container-escape.md         # Docker container privilege escalation exploitation
├── logrotate-exploitation.md          # Logrotate vulnerability exploitation and race conditions
├── miscellaneous-techniques.md        # Additional techniques (traffic capture, NFS, tmux hijacking)
├── shared-libraries.md                # LD_PRELOAD shared library hijacking exploitation
├── shared-object-hijacking.md         # Custom library RUNPATH hijacking exploitation
├── python-library-hijacking.md        # Python module import hijacking exploitation
├── sudo-cve-exploits.md               # Sudo CVE exploitation (Baron Samedit, Policy Bypass)
├── polkit-pwnkit.md                   # Polkit CVE-2021-4034 Pwnkit privilege escalation
├── dirty-pipe.md                      # Dirty Pipe CVE-2022-0847 kernel vulnerability exploitation
├── netfilter-kernel-exploits.md       # Netfilter kernel module CVE exploits (advanced)
├── linux-hardening.md                 # Defensive measures and system hardening practices
├── permissions-based-privesc.md       # File permissions, SUID/SGID exploitation
├── service-based-privesc.md          # Running services and process exploitation
├── configuration-based-privesc.md     # Misconfigurations and weak settings
├── kernel-exploitation.md            # Operating system vulnerabilities
├── application-specific-privesc.md   # Vulnerable installed software
├── automated-tools.md                # LinPEAS, LinEnum, and enumeration scripts
├── persistence-techniques.md         # Maintaining elevated access
└── skills-assessment.md              # Practical exercises and challenges
```

## 🚀 Getting Started

### Prerequisites

* **Basic Linux Knowledge**: Command line familiarity
* **Initial Access**: Shell on target Linux system
* **Methodology Understanding**: Systematic approach to enumeration
* **Tool Familiarity**: Common privilege escalation tools

### Attack Flow

```
Initial Access → Environment Enumeration → Vulnerability Identification → Privilege Escalation → Persistence
```

## 📋 Module Content

### ✅ **Completed Sections**

> **📊 Complete Coverage**: 24 privilege escalation techniques from basic enumeration to advanced kernel exploitation

#### **🔍** [**Environment Enumeration**](environment-enumeration.md)

* **System Information Gathering** - OS version, kernel, hardware details
* **User and Group Analysis** - Account enumeration and permission mapping
* **Network Configuration** - Interface analysis and internal network discovery
* **File System Analysis** - Mounted drives, hidden files, temporary directories
* **Security Controls Detection** - Firewall, SELinux, AppArmor identification
* **Initial Reconnaissance Checklist** - Systematic enumeration workflow

#### **🔧** [**Services & Internals Enumeration**](services-internals-enumeration.md)

* **Running Services Analysis** - Process enumeration and service identification
* **User Activity Investigation** - Login history, current users, command history
* **Scheduled Tasks Discovery** - Cron jobs, systemd timers, automation scripts
* **Installed Software Assessment** - Package analysis and GTFObins cross-reference
* **Configuration File Discovery** - System configs, application settings, credentials
* **Process Investigation** - System calls, memory analysis, /proc filesystem

#### **🔍** [**Credential Hunting**](credential-hunting.md)

* **File System Credential Search** - Configuration files, scripts, backups with stored secrets
* **SSH Key Discovery** - Private keys, known\_hosts analysis, lateral movement opportunities
* **Database Credential Extraction** - WordPress, MySQL, PostgreSQL, application databases
* **History File Investigation** - Bash history, command logs, user activity traces
* **Advanced Discovery Techniques** - Memory analysis, environment variables, process inspection

#### **🛤️** [**PATH Abuse**](path-abuse.md)

* **PATH Variable Manipulation** - Directory precedence exploitation and command hijacking
* **Writable Directory Detection** - PATH enumeration and write permission analysis
* **Script Hijacking Techniques** - Sudo scripts, cron jobs, and relative command exploitation
* **Binary Substitution Attacks** - Malicious script creation and execution interception

#### **🌟** [**Wildcard Abuse**](wildcard-abuse.md)

* **Shell Wildcard Exploitation** - Argument injection through filename expansion
* **tar Command Abuse** - checkpoint-action exploitation for command execution
* **Cron Job Targeting** - Automated wildcard script exploitation
* **Command Injection Payloads** - Sudo privilege escalation and SUID binary creation

#### **🚪** [**Escaping Restricted Shells**](escaping-restricted-shells.md)

* **SSH Bypass Techniques** - Remote shell restriction circumvention
* **Command Substitution Escapes** - Backtick and $() exploitation
* **Environment Variable Abuse** - SHELL and PATH variable manipulation
* **Built-in Command Exploitation** - Vi, less, man page escape sequences

#### **🔐** [**Special Permissions**](special-permissions.md)

* **SUID/SGID Binary Discovery** - Finding and enumerating special permission files
* **GTFOBins Exploitation** - Leveraging known privilege escalation binaries
* **Common Binary Abuse** - Text editors, interpreters, file utilities exploitation
* **Custom Binary Analysis** - Reverse engineering and shared library hijacking

#### **⚡** [**Sudo Rights Abuse**](sudo-rights-abuse.md)

* **Sudo Permission Enumeration** - Identifying misconfigured sudo privileges
* **GTFOBins Sudo Exploitation** - Text editors, interpreters, system tools abuse
* **Advanced Sudo Techniques** - Command injection, wildcard abuse, environment manipulation

#### **👑** [**Privileged Groups**](privileged-groups.md)

* **Container Group Exploitation** - LXD/LXC and Docker group privilege escalation
* **System Group Abuse** - Disk, ADM, shadow group privilege vectors
* **Direct Root Access** - Container mounting and raw device manipulation

#### **🎭** [**Capabilities**](capabilities.md)

* **Capability Enumeration** - Finding binaries with dangerous capability assignments
* **File Permission Bypass** - cap\_dac\_override exploitation for system file modification
* **UID/GID Manipulation** - cap\_setuid/cap\_setgid abuse for privilege escalation

#### **⚙️** [**Vulnerable Services**](vulnerable-services.md)

* **Service Version Enumeration** - Identifying outdated software with known vulnerabilities
* **Screen 4.5.0 Exploitation** - CVE-2017-5618 ld.so.preload overwrite attack
* **Common Service CVEs** - Apache, Nginx, MySQL, SSH, Sudo vulnerability identification

#### **⏰** [**Cron Job Abuse**](cron-job-abuse.md)

* **Cron Job Discovery** - Finding scheduled tasks and writable script identification
* **Process Monitoring** - pspy usage for cron job pattern detection
* **Script Modification Attacks** - Command injection and reverse shell payloads

#### **🐳** [**LXD Container Escape**](lxd-container-escape.md)

* **LXD Group Exploitation** - Container manager privilege escalation techniques
* **Privileged Container Creation** - Host filesystem mounting and root access
* **Container Image Management** - Importing and utilizing existing container images

#### **🐋** [**Docker Container Escape**](docker-container-escape.md)

* **Docker Group Exploitation** - Container runtime privilege escalation techniques
* **Host Filesystem Mounting** - Volume mounting for direct host access
* **Privileged Container Execution** - Bypassing container isolation mechanisms

#### **📜** [**Logrotate Exploitation**](logrotate-exploitation.md)

* **Logrotate Vulnerability Assessment** - Version identification and prerequisite verification
* **Logrotten Exploit Execution** - Race condition exploitation for privilege escalation
* **Configuration Mode Analysis** - Create vs compress mode detection and exploitation

#### **🔧** [**Miscellaneous Techniques**](miscellaneous-techniques.md)

* **Passive Traffic Capture** - Network sniffing for credential extraction using tcpdump
* **Weak NFS Privileges** - no\_root\_squash exploitation for SUID binary upload
* **Tmux Session Hijacking** - Privileged session attachment through weak socket permissions

#### **📚** [**Shared Libraries**](shared-libraries.md)

* **LD\_PRELOAD Exploitation** - Environment variable abuse for shared library injection
* **Malicious Library Creation** - Custom shared object compilation and deployment
* **Sudo Environment Bypass** - Transforming safe commands into privilege escalation vectors

#### **🎯** [**Shared Object Hijacking**](shared-object-hijacking.md)

* **RUNPATH Directory Exploitation** - Writable library path hijacking in SUID binaries
* **Custom Library Injection** - Missing function implementation for privilege escalation
* **Binary Dependency Analysis** - ldd and readelf usage for vulnerability identification

#### **🐍** [**Python Library Hijacking**](python-library-hijacking.md)

* **Python Module Import Exploitation** - sys.path manipulation and module precedence abuse
* **PYTHONPATH Environment Abuse** - Environment variable manipulation for import redirection
* **Writable Module Directory Hijacking** - Higher-priority path exploitation for code injection

#### **🚨** [**Sudo CVE Exploits**](sudo-cve-exploits.md)

* **CVE-2021-3156 Baron Samedit** - Heap buffer overflow exploitation for immediate root access
* **CVE-2019-14287 Policy Bypass** - Negative user ID exploitation for privilege escalation
* **Version-Specific Exploitation** - OS and sudo version correlation for successful exploitation

#### **🔐** [**Polkit/Pwnkit**](polkit-pwnkit.md)

* **CVE-2021-4034 Pwnkit Exploitation** - Memory corruption in pkexec for universal privilege escalation
* **Polkit Authorization Bypass** - PolicyKit service vulnerability affecting most Linux distributions
* **Zero-Prerequisite Escalation** - Any local user exploitation without special permissions

#### **💧** [**Dirty Pipe**](dirty-pipe.md)

* **CVE-2022-0847 Kernel Exploitation** - Pipe mechanism abuse for arbitrary file writes as root
* **Kernel Version Targeting** - Vulnerability affecting Linux kernels 5.8-5.17
* **File Modification Attacks** - /etc/passwd modification and SUID binary hijacking techniques

#### **🌐** [**Netfilter Kernel Exploits**](netfilter-kernel-exploits.md) _(Advanced)_

* **Multiple Kernel CVEs** - CVE-2021-22555, CVE-2022-25636, CVE-2023-32233 exploitation
* **Wide Kernel Range Coverage** - Targeting kernels from 2.6 to 6.3.1 versions
* **High-Risk Exploitation** - Kernel-level attacks with system stability considerations

#### **🛡️** [**Linux Hardening**](linux-hardening.md)

* **Defensive Security Measures** - Comprehensive hardening practices and configuration management
* **Update Management** - Kernel and package update strategies for vulnerability mitigation
* **Security Auditing** - Lynis scanner usage and custom hardening validation scripts

### 🎯 **Module Complete**

This comprehensive Linux Privilege Escalation module covers **24 complete techniques** ranging from basic enumeration to advanced kernel exploitation, providing thorough coverage of all major privilege escalation vectors in Linux environments.

**Skill progression**: Basic enumeration → Configuration attacks → Service exploitation → Container escapes → Kernel exploits → Defensive hardening

## 🛠️ Tools and Techniques

### Manual Enumeration

* **System Commands**: uname, id, whoami, sudo -l
* **File System**: find, ls, cat, grep
* **Network**: ifconfig, netstat, route, arp
* **Process**: ps, top, systemctl, service

### Automated Tools

* **LinPEAS**: Comprehensive Linux enumeration
* **LinEnum**: Classic privilege escalation enumeration
* **linux-smart-enumeration**: Intelligent selective enumeration
* **PEASS-ng**: Advanced privilege escalation suite

### Exploitation Frameworks

* **Metasploit**: Post-exploitation modules
* **GTFOBins**: Living off the land binaries
* **ExploitDB**: Public exploit database
* **Custom Scripts**: Tailored enumeration and exploitation
* **Kernel Exploits**: CVE-specific exploits (⚠️ **High risk - use with caution**)

## 🎯 Learning Objectives

By completing this module, you will be able to:

1. **Perform systematic environment enumeration** on Linux systems
2. **Identify privilege escalation vectors** through various attack surfaces
3. **Exploit common misconfigurations** to gain elevated privileges
4. **Utilize automated tools effectively** while understanding manual techniques
5. **Maintain persistence** after successful privilege escalation
6. **Document findings professionally** for penetration test reports

## 🛡️ Defensive Considerations

### Common Misconfigurations

* Excessive sudo permissions
* Writable files in PATH
* SUID binaries on sensitive executables
* Unpatched kernel vulnerabilities
* Service running as root unnecessarily

### Hardening Recommendations

* Regular system updates and patching (especially kernel updates)
* Principle of least privilege enforcement
* File permission auditing
* Service account isolation
* Monitoring and logging implementation
* **Special attention to kernel exploits** - Advanced techniques require careful testing

## 📖 Prerequisites Knowledge

### Linux Fundamentals

* Command line navigation
* File system structure
* User and group concepts
* Process management
* Network configuration basics

### Security Concepts

* Unix permissions model
* SUID/SGID concepts
* Service architecture
* Kernel space vs user space
* Authentication and authorization

## 🏆 Success Metrics

### Skill Development Goals

* **Manual Enumeration Proficiency**: Perform thorough recon without tools
* **Attack Vector Recognition**: Identify privilege escalation opportunities
* **Tool Integration**: Combine manual and automated techniques effectively
* **Stealth Operations**: Conduct enumeration without detection
* **Documentation Skills**: Create comprehensive findings reports

### Practical Milestones

* Successfully escalate privileges on various Linux distributions
* Identify and exploit SUID/SGID vulnerabilities
* Abuse service misconfigurations for privilege escalation
* Utilize kernel exploits safely and effectively (with caution for advanced techniques)
* Establish persistent elevated access
* Master 24 different privilege escalation techniques including advanced kernel exploits and defensive hardening

***

_This Linux Privilege Escalation module provides comprehensive coverage of techniques, tools, and methodologies for gaining elevated privileges on Linux systems, essential for penetration testers and security professionals._
