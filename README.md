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

Example command:
*nmap 192.168.1.1*

**Lab Environment**

Scanning Host:Kali Linux

Target: Metaspoitable2 (local Lab)

*All scans in the portfolio are conducted in a controlled and authorized environment*

---
**Phase 1:Host Discovery Objective**

Used to identify active systems on a network.

Command:

*nmap -sn 192.168.1.0/24*

Meaning:

-sn → Ping scan (discover hosts without scanning ports)

Example output:

Nmap scan report for 192.168.1.10
Host is up (0.002s latency)



  
