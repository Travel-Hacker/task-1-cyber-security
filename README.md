Task 1: Cyber Security – Network Scanning
Overview
This repository contains the results and documentation for Task 1 of the Cyber Security module, focusing on scanning a local network to identify open ports and assess potential security risks.

Objective
The primary goal of this task is to:

Discover open ports on devices within the local network.

Understand the exposure of services running on these ports.

Identify potential security vulnerabilities associated with open ports.

Tools Used
Nmap: A free and open-source network scanner used to discover hosts and services on a computer network.

Wireshark (optional): A network protocol analyzer used to capture and interactively browse the traffic running on a computer network.

Methodology
Installation: Installed Nmap on Kali Linux using the command:

bash
Copy
Edit
sudo apt update && sudo apt install nmap
Identify Local IP Range: Determined the local IP range by running:

bash
Copy
Edit
ip a
Example output:

sql
Copy
Edit
inet 192.168.31.45/24 brd 192.168.31.255 scope global dynamic wlan0
This indicates the local network range is 192.168.31.0/24.

Network Scan: Performed a TCP SYN scan on the local network using Nmap:

bash
Copy
Edit
nmap -sS 192.168.31.0/24
This scan identifies open ports on devices within the specified IP range.

Packet Analysis (Optional): Captured network packets using Wireshark to analyze the traffic during the scan.

Service Identification: Researched common services associated with the identified open ports to understand their purpose and potential vulnerabilities.

Security Assessment: Evaluated the security implications of the open ports and services, identifying potential risks.

Findings
Open Ports Identified: List of IP addresses and their corresponding open ports.

Services Detected: Common services running on the identified open ports.

Security Risks: Potential vulnerabilities associated with the open ports and services.

Recommendations
Based on the findings, the following actions are recommended to mitigate potential security risks:

Close Unnecessary Ports: Disable services that are not required.

Update Services: Ensure all services are up-to-date with the latest security patches.

Implement Firewalls: Configure firewalls to restrict access to critical services.

Monitor Network Traffic: Regularly monitor network traffic for unusual activities.

Files Included
Cyber Security task 1.docx: Detailed report documenting the task's methodology, findings, and recommendations.

Nmap report.txt: Raw output from the Nmap scan for reference.

License
This project is licensed under the MIT License – see the LICENSE file for details.
