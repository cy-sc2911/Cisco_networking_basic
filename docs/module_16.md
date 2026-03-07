### Application Layer Services

## The Client Server Relationship
# Client and Server Interaction
    Most of the commonly used internet applications rely on complicated interactions between various servers and clients.
    The term server refers to a host running a software application that provides information or services to other hosts that are connected to the network. A well-known example of an application is a web server. There are millions of servers connected to the internet, providing services such as web sites, email, financial transactions, music downloads, etc. A crucial factor to enable these complex interactions to function is that they all use agreed upon standards and protocols.
    Below are the three common types of server software:

        Email
            The email server runs email server software. Clients use browser software such as mail client software, such as Microsoft Outlook, to access email on the server.
        Web
            The web server runs wen server software. Clients use browser software, such as Chrome or Firefox to access web pages on the server.
        File
            The file server stores corporate and user files in a central location. The client devices access these files with client software such as the Windows File Explorer.

# URI, URN, and URL
    Web resources and web services such as RESTful APIs are identified using a Uniform Resource Identifier (URI). A URI is a string of characters that identifies a specific network resource.

        Uniform Resource Name (URN)
            This identifies only the namespace of the resource (web page, document, image, etc.) without reference to the protocol
        Uniform Resource Locator (URL)
            This defines the network location of a specific resource on the network. HTTP or HTTPS URLs are typically used with web browsers. Other protocols such as FTP (File Transfer Protocol), SFTP (SSH File Transfer Protocol), SSH (Secure SHell), and others can be used as a URL. A URL using SFTP might look like: sftp://sftp.example.com.

        These are parts of a URI, as shown in the image below:

            Protocols/scheme   - HTTPS or other protocols such as FTP, SFTP, mailto and NNTP
            Hostname           - www.example.com
            Path and file name - /author/book.html
            Fragment           - #page155

            ![URI](images/uri.png)

## Network Application Services
# Common Network Application Services
    The image below is a brief description of each service shown in a table.
    ![Common Network Application Services](images/network_application_services.png)

    Domain Name System (DNS)
        Resolves internet names to IP address

    Secure Shell (SSH)
        Used to provide remote access to servers and networking devices

    Simple Mail Transfer Protocol (SMTP)
        Sends email messages and attachments from clients to servers and from servers to other email servers

    Post Office Protocol (POP)
        Used by email clients to retrieve email and attachments from a remote server

    Internet Message Access Protocol (IMAP)
        Used by email clients to retrieve email and attachments from a remote server

    Dynamic Host Configuration Protocol (DHCP)
        Used to automatically configure devices with IP addressing and other necessary information to enable them to communicate over the internet

    HyperText Transfer Protocol (HTTP)
        Used by web browsers to request web pages and web servers to transfers the files that make up web pages of the World Wide Web

    File Transfer Protocol
        Used for interactive file transfer between systems

## Domain Name System
# DNS Server
    DNS server is used to associate a domain name, or a host name, with an IP address.

# A Note ABout Syntax Checker Activites
    There are different simulation tools to help build your configuration and troubleshooting skills. Because these are simulation tools, they typically do not have all the functionality of real equipment. One such tool is the Syntax Checker.

# Syntax Checker - The nslookup Command
    For home networks the DNS server address is typically handled by DHCP running on the home router. ISP provides the DNS server address to home router, and then the home router uses DHCP to send the configuration to all devices connected to its network.
    Use the command nslookup to discover the IP addresses for any domain name.

## Web Clients and Servers
# HTTP and HTML
    When a web client receives the IP address of a web server, the client browser uses that IP address and port 80 to request web services. This request is sent to the server using the HyperText Transfer Protocol (HTTP).
    When the server receives a port 80 request, the server responds to the client request and sends the web page to the client. The information content of a web page is encoded using specialized 'mark-up' languages. The HyperText Markup Language (HTMl) coding tells the browser how to format the web page and what graphics and fonts to use. HTML is the most commonly used language.
    The HTTP protocol is not a secure protocol; information could easily be intercepted by other users as data is sent over the network. In order to provide security for the data, HTTP can be used with secure transport protocols. Requests for secure HTTP are sent to port 443. These request use https in the site address in the browser, rather than http.
    There are many different web servers and web clients available. The HTTP protocol and HTML standards make it possible for these servers and clients from many different manufacturers to work together seamlesssly.

## File Transfer Protocol (FTP)
    Another common service used across the internet is one that allows users to transfer files.
    The File Transfer Protocol (FTP) provides an easy method to transfer files from one computer to another. A host running FTP client software can access an FTP server to perform various file management functions including uploads and downloads.
    The FTP server enables a client to exchange files between devices. It also enables clients to manage files remotely by sending file management commands such as delete or rename. To accomplish this, the FTP service uses two different ports to communicate between client and server.
    FTP client software is built into computer operating systems and into most web browsers. Stand-alone FTP clients offer many options in an easy-to-use GUI-based interface.

## Virtual Terminals
# Remote Access with Telnet or SSH
    Telnet provides a standard  method of emulating text-based terminal devices over the data network. Both the protocol itseld the client software that implements the protocol are commonly referred to as Telnet. Telnet servers listen for client requests on TCP port 23. A connection using Telnet is called a vty session, or connection. Rather than using a physical device to connect to the server, Telnet uses software to create a virtual device that provides the same features of a terminal session with access to the server's CLI.
    Telnet is not considered to be a secure protocol. Although the Telnet protocol can require a user to login, it does not support transporting encrypted data. All data exchanged during Telnet sessions is transported as plaintext across the network. This means that the data can be easily intercepted and understood.
    SSh provides the structure for secure remote login and other secure network services. It also provides stronger authentication thatn Telnet and supports transporting session data using encryption. Network professionals should always use SSH in place of Telnet, whenever possible.
