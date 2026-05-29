# internship-day-1

Task 1: Scan Your Local Network for Open Ports

Objective: Learn to discover open ports on devices in your local network to understand network exposure.


Find your local IP range
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/97373806-c21e-4952-ab54-68b96d344b22" />

IP  is = 10.33.80.169



nmap -sS 10.33.80.169/24


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0caf838e-b9ce-48ae-acca-1cb661b84d57" />

Port 53 is open.


.Optiona ly analyze packet capture with Wireshark




<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6fd943f5-ece1-432f-b9a9-9552960daa87" />


1.What is an open port?
An open port is a network port on a computer or server that is actively accepting connections from other devices.
Example:
Port 80 is open on a web server to allow HTTP website traffic.


2.How does Nmap perform a TCP SYN scan?
A TCP SYN scan is a port scanning technique used by Nmap to discover open ports on a target system by sending a SYN (synchronize) packet to the target port. If the target responds with a SYN-ACK packet, the port is considered open. The scanner then immediately ends the connection instead of completing the full TCP handshake, making the scan faster and less detectable.
Example:
nmap -sS 192.168.1.10

3.What risks are associated with open ports?
Open ports can create security risks because they allow external devices to communicate with services running on a system. If an open port is connected to a vulnerable or misconfigured service, attackers may exploit it to gain unauthorized access, steal data, spread malware, or perform cyberattacks on the target system.
Example:
An open Telnet port (23) with weak credentials can allow an attacker to remotely access a computer.


4.Explain the difference between TCP and UDP scanning.
TCP scanning checks ports that use the Transmission Control Protocol (TCP), which establishes a reliable connection between devices before data transfer. It is commonly used to detect services like HTTP, SSH, and FTP. UDP scanning checks ports that use the User Datagram Protocol (UDP), which sends data without creating a connection, making it faster but often less reliable and harder to detect accurately.
Example:
    • TCP Scan: Detecting an open web server on port 80. 
    • UDP Scan: Detecting a DNS service running on port 53.

5.How can open ports be secured?Open ports can be secured by closing unused ports, using firewalls to restrict unauthorized access, keeping services updated, and using strong authentication methods. Network administrators should regularly monitor and scan systems to identify unnecessary open ports and reduce possible attack points.
Example:
Blocking port 23 (Telnet) with a firewall and using SSH on port 22 instead improves security.

6.What is a firewa l's role regarding ports?
A firewall controls network traffic by allowing or blocking access to specific ports based on security rules. It helps protect a system from unauthorized access by preventing unwanted connections to open ports while allowing trusted communication.
Example:
A firewall may block port 445 to prevent unauthorized SMB access from external networks.


7.What is a port scan and why do attackers perform it?
A port scan is a technique used to identify open ports and services running on a target system or network. It helps determine which applications are accepting connections and may reveal possible security weaknesses. Attackers perform port scans to find vulnerable services, gather information about the target, and identify entry points for further attacks.
Example:
An attacker may scan a server and discover that port 22 (SSH) is open, then attempt to gain unauthorized remote access.




8.How does Wireshark complement port scanning?
Wireshark complements port scanning by capturing and analyzing network packets during a scan. While a port scanner identifies open ports and services, Wireshark helps examine the actual network traffic, responses, and communication patterns in detail for troubleshooting and forensic analysis.
Example:
During an Nmap scan, Wireshark can capture SYN and SYN-ACK packets to verify which ports are responding as open.



