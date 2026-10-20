# homelab-soc
Home lab on Proxmox. Currently running OPNsense, Domain Controller on Windows 2025 server, Splunk SIEM, and W11 endpoints

# Creating the network infrastructure
For this homelab I wanted to do my best to simulate a real work environment for Windows 11 end points. To do this I have set up an OPNsense firewall that monitors all traffic flowing between my WAN (home network) and the LAN (internal lab). From here all endpoints on the VM must connect to a domain controller setup on Windows 2025 server. The domain controller handles all user based privileges, and acts as the DNS resolver for all endpoints. All logs from OPNsense, the DC, and endpoints flow through Splunk which has been set up on an Ubuntu server to monitor all traffic flowing in this network.  

1) Network Topology
   - OPNsense: 
