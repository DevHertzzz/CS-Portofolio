# Introduction
Welcome to my cybersecurity portofolio, this repository was made to showcase my study journey, technical skill, and theoritical skill in the field of cybersecurity. This git repository was made to be my digital CV and to demonstate my passion in the field of cybersecurity.

# About Me
Hello, I am DevHertzzz, I am a student in the field of cybersecurity. And currently, I am still growing and learning on attacking legally & defending systems and data. Until today, I'm still pursuing a perfection in my offensive & defensive cybersecurity skills, with a focus on penetration testing and applying the best mitigations and response to an attack.

**Current Role**: Student
**Passion** : I have a strong interest on computer-based intelligence. Such as cybersecurity. And, I love practicing my penetration testing skill & defending systems from unwanted attacks.
**Fun Facts** : I spend most of my time infront of my computer. And I love doing research about most-recent attacks and the internet interest.

# Technical Skills

## Tools
**Penetration Test**: NMap, LOIC (Low Orbital Ion Cannon), hping3, Burp Suite, Metasploit, Hydra, SQLMap, John the ripper
**Network Analysis**: Wireshark, tcpdump, Netcat
**Malware Analysis**: Virustotal, njrat, any.run
**SIEM**: Wazuh, Splunk.

## Programming Languages
- Bash
- Python
- Golang
- C+ / C++
- Javascript

## Concepts and Frameworks

### Concepts
- Cyber Security Concepts: Networking, System Security, Authentication, Vulnerability Assessment, Exploitation, Privilege Escalation, and Post-Exploitation
- Offensive Security: Reconnaissance, Enumeration, Web Exploitation (OWASP Top 10), Password Attacks
- Defensive Security: Log Analysis, SIEM Monitoring, Incident Response, Threat Detection  

### Frameworks
- MITRE ATT&CK
- NIST Cybersecurity Framework
- OWASP Top 10
- CVSS Scoring System

# Certifications and Training

## Certifications
- None

## Tranining Platforms
- Tryhackme (THM)
- Hack The Box (HTB)
- Private-use Lab (Wazuh)

## Project Experience
After reading this, you'll see two example projects i've done so far throughtout my journey in this cybersecurity career.

### **Project 1:Basic Pentesting**
**Introduction:** On this THM lab, we're given a set of task to do. The task(s) are: brute forcing, hash cracking, service enumeration, linux enumeration. These tasks are given to learn as much as possible of offensive cybersecurity fundamentals. And make sure you're using their vpn, OpenVPN. The target on this project is an IP address given by the tryhackme room. Tools used: NMap, enum4linux, Gobuster, Hydra, John the ripper.

**Reconnaissance & Scanning:**
1. OSINT
- The target was identified as an active host within the controlled network.
3. Network mapping
- The target host was confirmed to be reachable and active.
4. Port scanning
- Multiple open ports were identified, including : SSH, HTTP, SMB.
- This indicates a broad attack surface with multiple potential entry points.
5. Service enumeration
- SMB enumeration revealed valid usernames and accessible shares.
- Web enumeration identified hidden directories containing sensitive information.
6. Vulnerability scanning
These vulnerabilities were found during our vulnerability scanning.
- Information disclosure via web directory
- Exposed SMB service revealing user data
- Potential for credential-based attacks due to discovered usernames
7. Command snippets
- gobuster [ip_a]
- nmap --script vuln [ip_a]

**Exploitation:**
1. Vulnerability identified
- Information disclosure via web directory
- Exposed SMB service revealing user data
- Potential for credential-based attacks due to discovered usernames
3. Exploit chosen
- Bruteforce SSH attack was conducted due to revealed usernames
4. Execution steps
- Find the valid credentials
- Valid credentials was found
- Login to the system
5. Code snippets/payloads
- hydra [wordlist_directory] [ip_a]
6. Proof of Concept
- Successful login to the target system via SSH confirmed initial access.

**Post-Exploitation & Privilege Escalation:**
1. Privilege Escalation Method:
- Privilege escalation was achieved through misconfigured system permissions and accessible sensitive files.
3. Execution Steps:
- Find a vulnerability (outdated service, etc) that leads to privilege escalation
- Exploit the vulnerability to do privilege escalation
4. Tools:
- LinPeas
5. PoC:
- Root-level access was successfully obtained, indicating full system compromise.

**Reporting & Finalization:**
1. Executive Summary
- The assessment that was done found a few vulnerabilities, including exposed services, information disclosure, and weak credentials. These issues made an attacker gain initial access and escalate privileges, resulting in full system compromise.
3. Impact Assessment
- Unauthorized access to system services
- Exposure of sensitive information
- Full compromise of the target system
4. Mitigation Recommendation
- Enforce strong password policies
- Disable or secure unnecessary services (e.g., SMB)
- Restrict access to sensitive web directories
- Apply least privilege principles
- Implement monitoring and alerting for brute force attempts
5. Lessons Learned
- Proper enumeration is critical in identifying attack vectors
- Weak credentials still remains as a security risk
- Misconfigurations can lead to many security breaches
- A structured methodology improves penetration testing effectiveness

### **Project 2:MrRobotCTF**
**Introduction:** On this THM lab, we're given a set of task to do. The task(s) are: to find a wordlist and find your way to get all of the 3 keys. And make sure you're using their local vpn, openVPN but with a modified one. The target on this project is an IP address given by the tryhackme room. Tools used: NMap, enum4linux, Gobuster/dirb/Nikto, Hydra, Burp suite, Reverse Shell, LinPeas.

**Reconnaissance & Scanning:**
1. OSINT
2. Network mapping
3. Port scanning
4. Service enumeration
5. Vulnerability scanning
6. Command snippets

**Exploitation:**
1. Vulnerability identified
2. Exploit chosen
3. Execution steps
4. Code snippets/payloads
5. Proof of Concept

**Post-Exploitation & Privilege Escalation:**
1. Privilege Escalation Method: 
2. Execution Steps: 
3. Tools: 
4. PoC:

**Reporting & Finalization:**
1. Executive Summary
2. Impact Assessment
3. Mitigation Recommendation
4. Lessons Learned
