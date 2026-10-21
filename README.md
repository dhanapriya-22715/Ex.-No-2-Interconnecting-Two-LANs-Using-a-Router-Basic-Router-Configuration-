# Date :21-10-2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1917" height="1133" alt="image" src="https://github.com/user-attachments/assets/33d82bf7-8d8f-4d60-8035-1b805ac76256" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>

<img width="1915" height="1142" alt="image" src="https://github.com/user-attachments/assets/5c7a0c07-7913-4d26-8381-2532b6a9dff6" />

•	IP configurations on PCs<br>

<img width="1917" height="1131" alt="Screenshot 2026-10-21 180104" src="https://github.com/user-attachments/assets/dc59df3e-a6fb-41a9-a467-37477834a3df" />
<img width="1917" height="1137" alt="Screenshot 2026-10-21 180128" src="https://github.com/user-attachments/assets/92666cdf-29b6-49d5-a6de-7c6fb08ca8d9" />

•	Successful ping between PC0 and PC1<br>

<img width="1917" height="1135" alt="image" src="https://github.com/user-attachments/assets/7ec47870-c0e5-4ff5-94e7-d5ce2db88c60" />
<img width="1917" height="1132" alt="image" src="https://github.com/user-attachments/assets/07043907-2a2f-4ef4-bd5e-08f6cad5543c" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

