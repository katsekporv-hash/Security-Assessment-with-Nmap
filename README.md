# Security-Assessment-with-Nmap
**Overview**

This portfolio demonstrate my practical project that shows your ability to use Nmap for network discovery, security assessment, and reconnaissance. It is often used by students in cybersecurity, penetration testing, and network administration to demonstrate skills..

*Recruitor-facing portfolio: Clearly shows what i can do, how i think, how i document sercurity work.*

*Beginner-friendly guide:Helps new cybersecurity learners understand Nmap from the ground up without being overwhelmed.*

Focus is not just on running commands, but on why they used, what the results mean, and how they support sercurity decisions  

**Introduction to Nmap**

Nmap (Network Mapper) is an open-source tool used to discover devices on a network and identify services running on them.

Main uses:
* Host discovery (finding active devices)
* Port scanning
* Service and version detection
* Operating system detection
* Security auditing
*it is widely used in ethical hacking and cybersecurity.*

 **Command:**
*nmap 192.168.225.139*

**Lab Environment**

Scanning Host:Kali Linux

Target: Metaspoitable2 (local Lab)

*All scans in the portfolio are conducted in a controlled and authorized environment*

---
**Phase 1:Host Discovery Objective**

Used to identify active systems on a network.

**Command:**

*nmap -sn 192.168.225.0/24*

Meaning:

-sn → Ping scan (discover hosts without scanning ports)

Example output:

Nmap scan report for 192.168.225.139

Host is up 2 (0.00018s latency)

ScreenShot 

<img width="552" height="183" alt="Screenshot 2026-03-16 224324" src="https://github.com/user-attachments/assets/2ad2c10f-b4cb-4a47-9b82-cd71409adb1a" />

---
**Phase 2: Basic Scanning**

Port scanning is used in network security and penetration testing to discover:

* Open ports
* Running services
* Possible entry points into a system

  **Command:**
  nmap 192.168.225.139

  screenshot
  
  <img width="538" height="540" alt="Screenshot 2026-03-16 231301" src="https://github.com/user-attachments/assets/1587837c-9b5a-47e3-9c17-83d10b2aa649" />

  ---
  **Phase 3: Scan a Specific Port or Multiple Port**
  
  You can scan a single port or multiple port.

  **Command for single port:**
  
  nmap -p 80 192.168.225.139

  NB: scanning port 80, port 80 is for http.

  **For multiple ports**
  
  it scan all the 65,535 ports.

  **Command: for Multiple ports**
  
  nmap -p 192.168.225.139

  NB: no port is specified.

  screenshot below is a single port.
  
<img width="543" height="177" alt="{6A618A3E-EE38-48AA-9C0B-7469C0885675}" src="https://github.com/user-attachments/assets/4402c068-d41b-41db-8b35-4e2e327984e1" />

---

**Phase 4: Service and Version Detections.**

it identify what services are running and their versions.

**Command:**

nmap -sV 192.168.225.139

-sV: Detects service versions

**Analyst Insight**

Knowing the exact version helps correlate services with known vulnerabilities

screenshot
<img width="1005" height="577" alt="Screenshot 2026-03-16 235107" src="https://github.com/user-attachments/assets/8f6e4e9e-8f0e-4bfd-a53e-bc2df6b4e983" />

---

**phase 5: Aggressive Scan Command**

Gather maximum information in a single scan.

**Command**

nmap -A 192.168.225.139

It enables:

* OS detection (-O)

* Service & version detection (-sV)

* Script scanning (NSE scripts)

* Traceroute

  screenshot
  
<img width="1206" height="910" alt="Screenshot 2026-03-17 071242" src="https://github.com/user-attachments/assets/4ab7d6e3-87e1-4a1c-b761-1ddbe7504a1d" />

**Use it when you need:**

* Full network reconnaissance

* Detailed security assessment

* Information for penetration testing

---

  
**Phase 6: Operation System (OS) detection**

identify the type of operating system running on a target machine (e.g., Linux, Windows).

**Command**

nmap -O 192.168.1.10

**Explanation:**

* -O → Enables OS detection

* Requires administrator/root privileges to work properly

  **How It Works**

Nmap analyzes:

* TCP/IP stack behavior

* Packet responses

* Network characteristics

Then compares them to its OS fingerprint database to guess the OS.

Screenshot

<img width="928" height="436" alt="Screenshot 2026-03-17 074316" src="https://github.com/user-attachments/assets/28008d81-7d94-40ac-875c-d1b524ca9fc5" />

---

**Phase 7: Nmap Scripting Engine (NSE)**

a powerful feature that allows you to run scripts to automate tasks like:

* Detecting vulnerabilities

* Gathering detailed information

* Brute-force testing (in authorized labs)

* Checking misconfigurations

  **Command**

  nmap --script=default 192.168.225.139

  **What it does:**

* Runs default safe scripts

* Provides additional info about services

**Vulnerability Scanning**

**Command**

nmap --script=vuln 192.168.1.10

This checks for:

* Known vulnerabilities

* Weak configurations

  Screenshot

  <img width="1092" height="935" alt="Screenshot 2026-03-17 081934" src="https://github.com/user-attachments/assets/808db0df-4daa-4e8d-906f-e390edfc2ed7" />


  ---

**Output Management in Nmap**

Output management in Nmap means saving, organizing, and formatting scan results so you can analyze them later or include them in reports.

**Saving output helps you:**

* Keep records of scans

* Analyze results later

* Create professional reports

* Share findings

**Command**

  nmap -oN result.txt 192.168.1.10

* -oN → Normal (readable) format

* Saves output to result.txt

**Save in All Formats at Once**

Command:

nmap -oA scan_results 192.168.1.10

This creates:

* scan_results.nmap (normal)

* scan_results.xml

* scan_results.gnmap

---

**Demonstrated skills**

* Network discovery
* Port scanning
* Service and OS detection
* Vulnerability assessment using NSE
* Reconnaissance techniques
* Output management
* Security analysis using Nmap.

  ---
  
  **Conclusion**

This project demonstrated the practical use of Nmap in conducting network reconnaissance and security assessment. Through a series of structured scans, including host discovery, port scanning, service and version detection, operating system identification, and the use of the Nmap Scripting Engine (NSE), valuable insights were gathered about target systems.

---

**Security Insight**

**How Cybercriminals Can Use Nmap**

Cybercriminals use Nmap during the reconnaissance phase of an attack to gather information about a target.

**1. Identifying Open Ports**

* Discover open ports such as:

22 (SSH)

80 (HTTP)

* These ports act as entry points into a system

**2. Detecting Services and Versions**

* Identify software versions (e.g., outdated Apache or OpenSSH)

* Exploit known vulnerabilities in old versions

**3. OS Detection**

* Determine the operating system (Windows, Linux)

* Launch OS-specific attacks

**4. Vulnerability Scanning (NSE)**

* Use scripts to detect weaknesses

* Target misconfigurations and exposed services

**5. Network Mapping**

* Understand network structure
* Identify valuable targets like servers or databases

  ---

  **How Cybersecurity Professionals Use Nmap**

Ethical hackers and security teams use Nmap to protect systems and improve security.


**1. Security Auditing**

* Scan systems to identify open ports and services

* Detect unnecessary or risky exposures

**2. Vulnerability Assessment**

* Find outdated or vulnerable software

* Fix issues before attackers exploit them

**3. Network Monitoring**

* Keep track of devices connected to a network

* Detect unauthorized systems

**4. Penetration Testing**

* Simulate real-world attacks in a controlled environment

* Test how secure a system is

**5. Hardening Systems**

* Close unused ports

* Update software

* Configure firewalls properly

  ---

  **Key Takeaway**

The difference between a cybercriminal and a cybersecurity professional is intent and authorization.

* Cybercriminals use Nmap to exploit weaknesses

* Professionals use it to identify and fix weaknesses










  
