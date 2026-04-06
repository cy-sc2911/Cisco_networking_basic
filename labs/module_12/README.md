# Examine NAT on a Wireless Router
## Objectives
Examine NAT configuration on a wireless router
    Set up 4 PCs to connect to a wireless router using DHCP
    Examine traffic that crosses the network using NAT

## Topology
Describe the devices used:
- 4 PCs
- 1 Wireless Router

![Network Topology](images/topology.png)

## Configuration Summary
- Wireless router configured with DHCP IPs
- Four PCs are assigned IPv4 addresses
- Configured public IP

![public](images/public_IP.png)

- Configured local area network

![LAN](images/local_network.png)

Setting up simulation panel (http and tcp) to capture NAT

![setting](images/setUp_simulation.png)

![simulateON](images/simulationONgoing.png)

## Verification
Successful public and LAN network for the four PCs:
- **PC0**

![pc0](images/pc0.png)

- **PC1**

![pc1](images/pc1.png)

- **PC2**

![pc2](images/pc2.png)

- **PC3**

![pc3](images/pc3.png)

**Sucessful simulation**

![inbound](images/inboundPDU.png)

![outbound](images/outboundPDU.png)
