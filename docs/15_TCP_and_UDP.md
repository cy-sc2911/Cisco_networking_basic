## TCP and UDP
    UDP is a 'best effort' delivery system that does not require acknowledgement of receipt. UDP is a perferable with applications such as streaming audio and VoIP (Voice over Internet Protocol). Acknowledgement would slow down delivery and retransmissions are undesirable. Packets take a path from the source to a destination. A few packets may be lost but it is usually not noticeable.
    TCP packets take a path from the source to the destination. However, each of the packets has a sequence number. TCP breaks up a message into small pieces known as segments. The segments are numbered in sequence and passed to the IP process for assemnly into packets. TCP keeps track of the number of segments that have been sent to a specific host from a specific application. If the sender does not receive an acknowledgement within a certain period of time, it assumes that the segments were lost and retransmits them. Only the portion of the message that is lost is resent, not the entire message.

## Port Numbers
# TCP and UDP Port Numbers
    There are many services that we access through the internet in the course of a day. DNS, web, email, FTP, IM and VoIP are just some of these services that are provided by client/server systems around the world. These services may be provided by a single server or by several servers in large data centers.
    When a message is delivered using either TCP or UDP, the protocols and services requested are identified by a port. A port is a numeric identifier within each segment that is used to keep track of specific conversations between a client and a server. Every message that a host sends contains both a source and destination port.
    When a message is received by a server, it is necessary for the server to be able to determine which service is being requested by the client. Clients are preconfigured to use a destination port that is registered on the internet for each service. An example of this is web browser clients which are preconfigured to send requests to web servers using port 80, the well-known port for HTTP web services.
    Ports are assigned and managed by an organization known as the Internet Corporation for Assigned Names and Numbers (ICANN). Ports are broken into three categories and range in number from 1 to 65,535:

        Well-known Ports
            Destination ports that are associated with common network applications are identified as well-known ports. These ports are in the range of 1 to 1023.
        Registered Ports
           Ports 1024 through 49151 can be used as either source or destination ports. These can be used by organizations to register specific applications such as IM applications.
        Private Ports
            Ports 49152 through 65535 are often used as source ports. These ports can be used by any application.

    Below are some commom well-known port numbers and their associated applications.
        TCP       Port 20   File Transfer Protocol (FTP) - Data
        TCP       Port 32   FTP - Control
        TCP       Port 22   Secure Shell (SSH)
        TCP       Port 23   Telnet
        TCP       Port 25   Simple Mail Transfer Protocol (SMTP)
        UDP/TCP   Port 53   Domain Name Service (DNS)
        UDP       Port 67   Dynamic Host Configuration Protocol (DHCP) - Server
        UDP       Port 68   DHCP - Client
        UDP       Port 69   Trivial File Transfer Protocol (TFTP)
        TCP       Port 80   HyperText Transfer Protocol (HTTP)
        TCP       Port 110  Post Office Protocol version 3 (POP3)
        TCP       Port 143  Internet Message Access Protocol (IMAP)
        UDP       Port 161  Simple Network Management Protocol (SNMP)
        TCP       Port 443  Hypertext Transfer Protocol Secure (HTTPS)

    Some applications may use both TCP and UDP. For example, DNS uses UDP when clients send requests to a DNS server. However, communication between two DNS servers always uses TCP.

# Socket Pairs
    The source and destination ports are placed within the segment. The segments are then encapsulated within an IP packet. The IP packet contains the IP address of the source and destination. The combination of the source IP address and source port number, or the destination IP address and destination port number is known as a socket.
    Sockets enable multiple processes, running on a client, to distinguish themselves from each other, and mutiple connections to a server process to be distinguished from each other.
    The source port number acts as a return address for the requesting application. The transport layer keeps track of this port and the application that initiated the request so that when a response is returned, it can be forwarded to the correct application.

# The netstat Command
    Unexplained TCP connections can pose a major security threat. They can indicate that something or someone is connected to the local host. Sometimes it is necessary to know which active TCP connections are open and running on a networked host. Netsat is an important network utility that can be used to verify those connections.
    By default, the netstat command will attempt to resolve IP addresses to domain names and port numbers to well-known applications. The -n option can be used to display IP addresses and port numbers in their numerical form.
