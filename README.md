# Home Lab-Soc
Home lab on Proxmox. Currently running OPNsense, Domain Controller on Windows 2025 server, Splunk SIEM, and W11 endpoints

# Creating the network infrastructure
For this homelab I wanted to do my best to simulate a real work environment for Windows 11 end points, and what would happen to the network if it were attacked by external/internal threat actors. This meant creating an environment with a firewall, domain controller, SIEM, and active end points.

Building the Network
   -
   1) Starting the build in Proxmox I needed to build the firewall, which in this case was OPNsense. The primary issue was making sure that the homelab would be able to communicate with the internet, but prevent it from reaching any other part of the home network. Simulating attacks meant that I wanted to keep the lab as segmented as possible, so the firewall acted as a bridge between the WAN (home network) and the LAN (lab network). Communicating between bridge 0 (vmbr0) meant that the OPNsense firewall could communicate with the router to send and receive traffic from the internet. Communicating over bridge 1 (vmbr1) meant that the OPNsense firewall was collecting all traffic coming from inside the lab. Like any good build issues popped up immediately! I had originally planned on giving the lab network a private IP address, but that private address was already taken by certain devices on my home network, so the plan deviated into creating a new set of IP addresses  
   
Network Topology
   -
<img width="1540" height="803" alt="Homelab Network Topology drawio" src="https://github.com/user-attachments/assets/28566e50-8020-4bca-b6de-b173d085d916" />

