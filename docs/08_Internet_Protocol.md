## Purpose of an IPv4 address
# The IPv4 address
    The IPv4 address is a logical network address that identifies a particular host. It must be properly configured and unique within the LAN, for local communication. It must also be properly configured and unique in the world, for remote communication. This is how a host is able to communicate with other devices on the internet.

    An IPv4 address is assigned to the network interface connection for a host. This connection is usually a network interface card (NIC) installed in the device. Some servers can have  more than one NIC and each of these has its own IPv4 address. Router interfaces that provide connections to an IP network will aso have an IPv4 address.

    Every packet sent across the internet has a source and destination IPv4 address. This information is required by networking devices to ensure the information gets to the destination and any replies are returned to the source.

# Octets and Dotted-Decimal Notation
    IPv4 addresses are 32 bits in length. Below is an IPv4 address in binary:
        11010001101001011100100000000001

     Notice how difficult this address is to read. For this reason, the 32 bits are grouped into four 8-bit bytes called octets like this:
        11010001.10100101.11001000.00000001

    It's better but still difficult to read. That is why each octet is converted into its decimal value, separated by a decimal point or period. The above binary IPv4 becomes the below dotted-decimal representation:
        209.165.200.1

# IPv4 Structure
    The logical 32-bit IPv4 address is hierarchical and is made up of two parts, the network, and the host.
        For example, there is a host with an IPv4 address 192.168.5.11 with a subnet mask of 255.255.255.0. The first three octets, (192.168.5), identify the network portion of the address, and the last octet, (11) identifies the host. This is know as a hierarchical addressing because the network portion indicates the network on which each unique host address is located.

    Routers only need to know how to reach each other, rather than needing to know the location of each individual host. With IPv4 addressing, multiple logical networks can exist on one physical network if the network portion of the logical network host addresses is different.
