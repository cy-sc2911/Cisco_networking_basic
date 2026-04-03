# IPv4 Unicast, broadcast and Multicast
## Unicast
    Unicast transmission refers to one device sending a message to one other device in one-to-one communications.
    A unicast packet has a destination IP address that is a unicast address which goes to a single recipient. A source IP address can only be a unicast address, because the packet can only originate from a single source. This is regardless of whether the destination IP address is a unicast, broadcast, or multicast.
    IPv4 unicast host addresses are in the address range of 1.1.1.1 to 223.255.255.255. However, within this range are many addresses that are reserved for special purposes.

# Broadcast
    Broadcast transmission refers to a device sending a message to all devices on a network in one-to-all communications.
    A broadcast packet has a destination IP address with all ones (1s) in the host portion, or 32 one (1) bits.

    Note: IPv4 uses broadcast packets. However, there are no broadcast packets with IPv6.

    A broadcast packet must be processed by all devices in the same broadcast domain. A broadcast domain identifies all hosts on the same network segment. A broadcast may be directed or limited. A directed broadcast is sent to all hosts on a specific network.
    Broadcast packets use resources on the network and make every receiving host on the network process the packet. Therefore, broadcast traffic should be limited so that it does not adversely affect the performance of the network or devices. Because routers separate broadcast domains, subdividing networks can improve network performance by eliminating excessive broadcast traffic.

# Multicast
    Multicast transmission reduces traffic by allowing a host to send a single packet to a selected set of hosts that subscribe to a multicast group.
    A multicast packet is a packet with a destination IP address that is a multicast address. IPv4 has reserved the 224.0.0.0 to 239.255.255.255 addresses as a multicast range.
    Hosts that receive particular multicast packets are called multicast clients. The multicast clients use services requested by a client program to subscribe to the multicast group.
    Each multicast group is presented by a single IPv4 multicast destination address. When an IPv4 host subscribes to a multicast group, the host processes packets addressed to this multicast address, and packets addressed to its uniquely allocated unicast address.
    Routing protocols such as OSPF use multicast transmission.
        Examples, routers enabled with OSPF communicate with each other using the reserved OSPF multicast address 224.0.0.5. Only devices enabled with OSPF will process these packets with 224.0.0.5 as the destination IPv4 address. ALl other devices will ignore these packets.

## Types of IPv4 addresses
# Public and Private IPv4 addresses
    Public IPV4 addresses are address which are globally routed between internet service provider (ISP) routers. However, not all available IPv4 addresses can be used on the internet. There are blocks of addressed called private addresses that are used by most organizations to assign IPv4 addresses to internal hosts.
    In the mid- 1990s, with the introduction of the World Wide Web (WWW), private IPv4 addresses were introduced because of the depletion of IPv4 address space. Private IPv4 addresses are not unique and can be used internally within any network.

    Note: The long-term solution to IPv4 address depletion was IPv6.

    Network Addresses and Prefix   |   RFC 1918 Private Address Range
    10.0.0.0/8                     |   10.0.0.0 - 10.255.255.255
    172.16.0.0/12                  |   171.16.0.0 - 172.31.255.255
    192.168.0.0/16                 |   192.168.0.0 - 192.168.255.255

    Note: Private addresses are defined in RFC 1918 and sometimes referred to as RFC 1918 address space.

# Routing to the Internet
    Private IPv4 Addresses and Network Address Translation (NAT)
        Most internal networks, from large enterprises to home networks, use private IPv4 addresses for addressing all internal devices (intranet) including hosts and routers. However, private addresses are not globally routable.
    Packets with a private address must be filtered(discarded) or translated to a public address before forwarding the packet to an ISP.
    Before the ISP can forward this packet, it must translate the source IPv4 address, which is a private address, to a public IPv4 address using Network Address Translation (NAT). NAT is used to translate between private IPv4 and public IPv4 addresses. This is usually done on the router that connects the internal network to the ISP network. Private IPv4 addresses in the organization's intranet will be translated to public IPv4 addresses before routing to the internet.

# Special Use IPv4 Addresses
    There are certain addresses, such as network address and broadcast address, that cannot be assigned to hosts. There are also special addresses that can be assigned to hosts, but with restrictions on how those hosts can interact within the network.

    Loopback addresses
     Loopback addresses (127.0.0.0 /8 or 127.0.0.1 to 127.255.255.254) are more commonly identifies as only 127.0.0.1. These are special addresses used by a host to direct traffic itself.
        Example, the ping command is commonly used to test connections to other hosts. But you can also use the ping command to test if the IP configuration on your own device

    Link-local addresses
        Link-local addresses (169.254.0.0/16 or 169.254.0.1 to 169.254.255.254) are more commomly knows as the Automate Private IP Addressing (APIPA) addresses or self-assigned addresses. They are used by a Windows client to self-configure in the event that the client cannot obtain an IP addressing through other methods. Link-local addresses can be used in a peer-to-peer connection but are not commonly used for this purpose.

# Legacy Classful Addressing
    In 1981, IPv4 addresses were assigned using classful addressing as defined in RFC 790, Assigned Numbers. Customers were allocated a network address based on one of three classes, A, B, or C. The RFC divided the unicast ranges into specific classes:
        Class A (0.0.0.0/8 to 127.0.0.0/8)
            Designed to support extremely large neworks with more than 16 million host addresses. Classes A used a fixed /8 prefix witt the first octet to indicate the network address and the remaining threee octets for host addresses (more than 16 million host addresses per network)
        Class B (128.0.0.0 /16 - 191.255.0.0 /16)
            Designed to support the needs of moderate to large size networks with up to approximately 65, 000 host addresses. Class B used a fixed /16 prefix with the two high-order octets to indicate the network address and the remaining two octets for host addresses (more than 65,000 host addresses per network)
        Class C (192.0.0.0 /24 to 223.255.255.0 /24)
            Designed to support small networks with maximum of 254 hosts. Class C used a fixed /24 prefix with the first three octets to indicate the network and the remaining octet for the host addresses (only 254 host addresses per network)

    Note: There is also a Class D multicast block consisting of 224.0.0.0 to 239.0.0.0 and a Class E experimental address block consisting of 240.0.0.0 - 255.0.0.0.

    At the time, with a limited number of computers using the internet, classful addressing was an effective means to allocate addresses.
    In the mid-1990s, with the introduction of the World Wide Web (WWW), classful addressing was deprecated to more efficiently allocate the limited IPv4 address space. Classful address allocation was replaced with classless addressing, which is used today. Classless addressing ignores the rules of classes (A, B, C). Public IPv4 network addresses (network addresses and subnet masks) are allocated based on the number of addresses that can be justified.

# Regional Internet Registries (RIR)
    Public IPv4 addresses are addresses which are globally routed over the internet. Public IPv4 addresses must be unique.
    Both IPv4 and IPv6 addresses are managed by the Internet Assigned Numbers Authority (IANA). The IANA manages and allocates blocks of IP addresses to the Regional Internet Registries (RIRs).
        The five RIRs are ![RIR](images/Regional_Internet_Reg.png)

    RIRs are responsible for allocating IP addresses to ISPs who provide IPv4 address blocks to organizations and smaller ISPs. Organizations can also get their addresses directly from an RIR(subject to the policies of that RIR).

        AfriNIC (African Network Information Centre) - Africa Region
        APNIC (Asia Pacific Network Information Centre) - Asia/Pacific Region
        ARIN (American Registry for Internet Numbers) - North America Region
        LACNIC (Regional Latin-American and Caribbean IP Address Registry) - Latin America and some Caribbean Islands
        RIPE NCC (Réseaux IP Européens Network Coordination Centre) - Europe, the Middle East, and Central Asia

## Network Segmentation
# Broadcast Domains and Segmentation
    In an Ethernet LAN, devices use broadcasts and the Address Resolution Protocol (ARP) to locate other devices. ARP sends Layer 2 broadcasts to a know IPv4 address on the local network to discover the associated MAC address. Devices on Ethernet LANs also locate other devices using services. A host typically acquires its IPv4 address configuration using the Dynamic Host Configuration Protocol (DHCP) which sends broadcasts on the local network to locate a DHCP server.
    Switches propagate broadcasts out all interfaces except the interface on it which it was received.

    Routers Segment Broadcast Domains
    Routers do not propagate broadcasts. When a router receives a broadcast, it does not forward it out other interfaces.
    Each router interface connects to a broadcast domain and broadcasts are only propagated within that specific broadcast domain.

# Problems with Large Broadcast Domains
    A large broadcast domain is a network that connects many hosts. A problem with a large broadcast domain is that these hosts can generate excessive broadcasts and negatively affect the network.

    Communicating between Networks
    The solution is to reduce the size of the network to create smaller broadcast domains in a process called subnetting. These smaller network spaces are called subnets.
    The prefix length has changed from a single /16 network to two /24 networks. This is the basis of subnetting: using host bits to create additional subnets.

    Note: The terms subnet and network are often used interchangeably. Most networks are a subnet of some larger address block.

# Reasons for Segmenting Networks
    Subnetting reduces overall network traffic and improves network performances. It also enables an administrator to implement security policies such as which subnets are allowed or not allowed to communicate together. Another reason is that it reduces the number of devices affected by abnormal broadcast traffic due to misconfigurations, hardware/software problems, or malicious intent.
    There are various ways of using subnets to help manage network devices:
        Subnetting by location
            ![location](images/subnet_by_location.png)
        Subnetting by Group or Function
            ![GroupOrFunc](images/func.png)
        Subnetting by Device Type
            ![DeviceType](images/deviceType.png)
    Network administratos can create subnets using any other division that makes sense for the network. Understanding how to subnet networks is a fundamental skill that all network administratos must develop.
