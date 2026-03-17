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

ScreenShot placeholder
<img width="552" height="183" alt="Screenshot 2026-03-16 224324" src="https://github.com/user-attachments/assets/2ad2c10f-b4cb-4a47-9b82-cd71409adb1a" />

---
**Phase 2: Basic Scanning**

Port scanning is used in network security and penetration testing to discover:

* Open ports
* Running services
* Possible entry points into a system

  **Command:**
  nmap 192.168.225.139
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









  
