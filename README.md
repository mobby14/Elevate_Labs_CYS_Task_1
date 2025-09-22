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
2. Determined the local IP subnet (e.g., 172.20.10.0/24)
3. Performed TCP SYN scan using `nmap -sS 172.20.10.0/24`
4. Documented IPs and open ports found during the scan
5. Researched services running on common and unknown ports
6. Evaluated security exposure of open ports

## Sample Results
| IP Address  | Open Ports           | Services Identified           |
|-------------|---------------------|------------------------------|
| 172.20.10.1 | 21, 53, 49152, 62078 | FTP, Domain (DNS), Unknown, iPhone-sync |
| 172.20.10.4 | 49152, 62078         | Unknown, iPhone-sync           |

## Key Learnings
- Open ports are necessary for network communication but pose security risks if unnecessary or unmonitored
- Nmap TCP SYN scans provide fast and stealthy detection of open ports
- Proper firewall rules and service management are critical to reducing vulnerability
- Continuous network monitoring and patching help maintain security posture

## How to Run
1. Install Nmap on your system
2. Identify your local subnet with commands like `ipconfig` or `ifconfig`
3. Run the scan:  nmap -sS <your-local-subnet>
4. Review open ports and services in the scan output

## Recommendations
- Close unnecessary ports and disable unused services
- Use firewalls to restrict port access based on IPs and protocols
- Regularly update and patch networked devices
- Implement ongoing monitoring with tools like Wireshark

## License
This project is licensed under the MIT License.

---

*For educational purposes as part of the Cybersecurity Internship.*


