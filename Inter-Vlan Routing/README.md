Inter-VLAN Routing Network Topology
Overview
This project demonstrates a basic Inter-VLAN routing setup using a core router/switch and two distribution layer switches (SW-1 and SW-2). Multiple VLANs are configured to segment the network for better security and management.

Components
Core Router/Switch

2 Layer 2 Switches (SW-1, SW-2)

Samba Server (Internet and File Sharing Access)

DHCP Server (Dynamic IP assignment)

8 End Devices (PC-1 to PC-8 and XP machine)

VLAN Configuration
VLAN 10: PC-1, PC-2 (SW-1) and PC-5, PC-6 (SW-2)

VLAN 20: PC-3, PC-4 (SW-1) and PC-7, PC-8 (SW-2)

VLAN 30: Samba and DHCP Servers

Key Points
Core device handles Inter-VLAN routing.

SW-1 and SW-2 connect end devices to their respective VLANs.

Red lines indicate VLAN segmentation at the access layer.

DHCP server assigns IPs dynamically to clients across VLANs.

Samba server provides network file sharing and internet access.
