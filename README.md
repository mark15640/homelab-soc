# Home Lab-Soc
Home lab on Proxmox. Currently running OPNsense, Domain Controller on Windows 2025 server, Splunk SIEM, and W11 endpoints

# Creating the network infrastructure
For this homelab I wanted to do my best to simulate a real work environment for Windows 11 end points, and what would happen to the network if it were attacked by external threat actors. This meant creating an environment with a firewall, domain controller, SIEM, and active end points.

Building the Network
   -
   Starting the build in Proxmox I needed to build the firewall, which in this case was OPNsense. The primary issue was making sure that the homelab would be able to communicate with the internet, but prevent it from reaching any other part of the home network. 
   
Network Topology
   -
<img width="1092" height="802" alt="Homelab Network Topology drawio" src="https://github.com/user-attachments/assets/01297901-3830-4ff2-8d32-7d4853ca3435" />
