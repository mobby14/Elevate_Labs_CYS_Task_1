# Cybersecurity Internship – Network Port Scanning Project

## Project Overview
This project demonstrates basic network reconnaissance techniques by scanning a local network to discover open ports and running services on connected devices. 

## Objectives
- Identify open ports on devices in the local subnet using TCP SYN scanning
- Assess potential security risks associated with open ports
- Recommend remediation and security best practices

## Tools Used
- **Nmap:** Network scanning tool for identifying open ports and services

## Methodology
1. Installed Nmap from the official website
2. Use Command Prompt/Terminal to find the local IP subnet (e.g., 172.XX.XX.0/24)
   <br>2.1. For Windows[CMD], Use ipconfig.
   <br>2.2. For Mac[Terminal], Use ipconfig getsummary en0[for wireless]/en1 [for ethernet].
4. Performed TCP SYN scan using `nmap -sS 172.XX.XX.0/24`
5. Documented IPs and open ports found during the scan
6. Researched services running on common and unknown ports
7. Evaluated security exposure of open ports

# Network Scan Results and Service Descriptions

| IP Address | Open Ports              | Services and Descriptions                                                         |
|------------|------------------------|-----------------------------------------------------------------------------------|
| Unknown    | 21, 53, 49152, 62078   | **21 - FTP:** File Transfer Protocol for transferring files, but insecure by default. <br> **53 - Domain (DNS):** Resolves domain names to IP addresses, essential for internet communication. <br> **49152 - Unknown:** Dynamically assigned ephemeral port, service varies. <br> **62078 - iPhone-sync:** Used by Apple devices for syncing data with computers. |
| Unknown    | 49152, 62078           | **49152 - Unknown:** As above, requires further investigation. <br> **62078 - iPhone-sync:** As above, related to Apple device syncing.                              |
| Unknown    | 135, 139, 445, 2968, 3580 | **135 - MSRPC:** Microsoft Remote Procedure Call, for system communications but can be vulnerable. <br> **139 - NetBIOS-SSN:** Supports Windows file/printer sharing; often targeted for attacks. <br> **445 - Microsoft-DS:** SMB protocol for file sharing; critical but widely exploited. <br> **2968 - ENPP:** Less common, possibly network proxy or proprietary service. <br> **3580 - NATI-SVRLOC:** Used for network address translation server location, depends on network setup. |


## Key Learnings
### Open Port
- Open ports are the doors which allows the local pc to communicate in internet but as it says it is a door.
- Therefore, We need to properly secure the door from the hackers ie. thieves.

### NMap Syntax
- Nmap TCP SYN scans provide fast and stealthy detection of open ports.
- It works by sending a TCP packet with the SYN flag set (which is the first step in establishing a TCP connection) to the target port.
- This method is "stealthy" because it does not complete the full TCP connection, which means it is less likely to be logged or detected by the target system, making it useful for reconnaissance without raising alarms.

## Potential Risks
- Open ports provide potential entry points for unauthorized access by hackers.
- Services on open ports may have unpatched vulnerabilities exploitable by attackers.
- Malware infections and botnet recruitment can occur through compromised open ports.
  
## Solutions
- Proper firewall rules and service management are critical to reducing vulnerability
- Regularly Update and Patch Services
- Continuous network monitoring and patching help maintain security posture



*For educational purposes as part of the Cybersecurity Internship.
