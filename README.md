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
* The target was identified as an active host within the controlled network.
3. Network mapping
* The target host was confirmed to be reachable and active.
4. Port scanning
* Multiple open ports were identified, including : SSH, HTTP, SMB.
* This indicates a broad attack surface with multiple potential entry points.
5. Service enumeration
* SMB enumeration revealed valid usernames and accessible shares.
* Web enumeration identified hidden directories containing sensitive information.
6. Vulnerability scanning
These vulnerabilities were found during our vulnerability scanning.
* Information disclosure via web directory
* Exposed SMB service revealing user data
* Potential for credential-based attacks due to discovered usernames
7. Command snippets
* gobuster [ip_a]
* nmap --script vuln [ip_a]

**Exploitation:**
1. Vulnerability identified
* Information disclosure via web directory
* Exposed SMB service revealing user data
* Potential for credential-based attacks due to discovered usernames
3. Exploit chosen
* Bruteforce SSH attack was conducted due to revealed usernames
4. Execution steps
* Find the valid credentials
* Valid credentials was found
* Login to the system
5. Code snippets/payloads
* hydra [wordlist_directory] [ip_a]
6. Proof of Concept
* Successful login to the target system via SSH confirmed initial access.

**Post-Exploitation & Privilege Escalation:**
1. Privilege Escalation Method:
* Privilege escalation was achieved through misconfigured system permissions and accessible sensitive files.
3. Execution Steps:
* Find a vulnerability (outdated service, etc) that leads to privilege escalation
* Exploit the vulnerability to do privilege escalation
4. Tools:
* LinPeas
5. PoC:
* Root-level access was successfully obtained, indicating full system compromise.

**Reporting & Finalization:**
1. Executive Summary
* The assessment that was done found a few vulnerabilities, including exposed services, information disclosure, and weak credentials. These issues made an attacker gain initial access and escalate privileges, resulting in full system compromise.

2. Impact Assessment
* Unauthorized access to system services
* Exposure of sensitive information
* Full compromise of the target system

3. Mitigation Recommendation
* Enforce strong password policies
* Disable or secure unnecessary services (e.g., SMB)
* Restrict access to sensitive web directories
* Apply least privilege principles
* Implement monitoring and alerting for brute force attempts

4. Lessons Learned
* Proper enumeration is critical in identifying attack vectors
* Weak credentials still remains as a security risk
* Misconfigurations can lead to many security breaches
* A structured methodology improves penetration testing effectiveness

### **Project 2:MrRobotCTF**
**Introduction:** On this THM lab, we're given a set of task to do. The task(s) are: to find a wordlist and find your way to get all of the 3 keys. And make sure you're using their local vpn, openVPN but with a modified one. The target on this project is an IP address given by the tryhackme room. Tools used: NMap, enum4linux, Gobuster/dirb/Nikto, Hydra, Burp suite, Reverse Shell, LinPeas.

**Reconnaissance & Scanning:**

1. OSINT
* OSINT activities were minimal due to the isolated nature of the lab environment.
* Initial interaction with the web application provided useful clues for further exploration.

2. Network Mapping
* The target host was successfully identified as active and reachable within the network.

3. Port Scanning
* Open ports were discovered, with HTTP being the primary service exposed.
* This indicated that the web application would likely be the main attack surface.

4. Service Enumeration
* Directory enumeration revealed hidden paths and files within the web server.
* A robots.txt file exposed valuable information, including a wordlist that played a key role in later stages.
* Further analysis identified a WordPress login panel as a potential entry point.

5. Vulnerability Scanning
* The application exposed sensitive files that should not have been publicly accessible.
* Weak authentication controls made the system vulnerable to brute force attacks.
* Misconfigurations within the web application increased the overall attack surface.

6. Command Snippets
* NMap -sv [ip_a]
* dirb [ip_a]
* Nikto [ip_a]

**Exploitation:**

1. Vulnerability Identified
* Sensitive information leakage through robots.txt and exposed directories.
* Weak login credentials on the WordPress authentication page.

2. Exploit Chosen
* A brute force attack was performed against the WordPress login interface using discovered data.

3. Execution Steps
* Usernames and wordlists obtained during enumeration were used for authentication attempts.
* Valid credentials were successfully identified through repeated login attempts.

4. Code Snippets / Payloads
* Hydra was used to automate the brute force attack process.
* A reverse shell was deployed after gaining access to establish system-level interaction.

5. Proof of Concept
* Successful login to the web application confirmed initial access.
* The reverse shell provided direct interaction with the target system.

---

**Post-Exploitation & Privilege Escalation:**

1. Privilege Escalation Method
* Privilege escalation was achieved through misconfigured system permissions and accessible system components.

2. Execution Steps
* System enumeration was performed to identify potential privilege escalation paths.
* Misconfigurations were leveraged to gain higher-level access.

3. Tools
* LinPEAS was used to assist in identifying privilege escalation opportunities.
* Built-in Linux commands were used for manual validation.

4. PoC
* Elevated privileges were verified using system identity commands.
* Root-level access was successfully obtained, completing full system compromise.

**Reporting & Finalization:**

1. Executive Summary
* The assessment revealed several security weaknesses, including exposed sensitive data, weak authentication, and system misconfigurations.
* These issues allowed an attacker to gain access and take full control of the system.

2. Impact Assessment
* Unauthorized access to both the web application and underlying system.
* Exposure of sensitive information that could be further exploited.
* Complete compromise of the target environment.

3. Mitigation Recommendation
* Restrict access to sensitive files such as robots.txt and hidden directories.
* Enforce strong password policies and implement account lockout mechanisms.
* Secure web application configurations to reduce unnecessary exposure.
* Apply the principle of least privilege across all users and services.
* Monitor login activity to detect and prevent brute force attacks.

4. Lessons Learned
* Even small information leaks can significantly help an attacker.
* Weak passwords are still one of the most common and dangerous vulnerabilities.
* Proper enumeration is essential for uncovering hidden attack paths.
* Following a structured approach makes the attack process more efficient and effective.
