# Configure DHCP on a Wireless Router
## Overview
A home user wants to use a wireless router to connect 3 PCs. All 3 PCs should obtain their address automatically from the wireless router.

## Objectives
- Connect 3 PCs to a wireless router
- Change the DHCP setting to a specific network range
- Configure the clients to obtain their address via DHCP

## Topology
Describe the devices used:
- 3 PCs
- DHCP Enabled Router

![Network Topology](images/topology.png)

## Configuration Summary
The three PCs are configured to receive DHCP IP addresses

![DHCPconfig](images/assignDHCP.png)

Changing the IP address to : 192.168.5.1

![IPchange](images/changingDefaultAddr.png)

Sucessful login on new IP: 192.168.5.1

![Success](images/NewIP.png)

## Verification
Successful connection
