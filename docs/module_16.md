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

# Telnet
    Before desktop computers with sophisticated graphical interfaces existed, people used text-based systems which were often just displays terminals physically attached to a central computer. After networks became available, people needed a way to remotely access the computer systems in the same manner that they did with the directly-attached terminals.
    Telnet was developed to meet that need. Telnet dates back to the early 1970s and is among the oldest of the application layer protocols and servces in the TCP/IP suite. Telnet provies a standard method of emulating text-based terminal devices over the data network. Both the protocol itself and the client software that implements the protocol are commonly referred to as Telnet. Telnet servers listen for client requests on TCP port 23.
    Appropriately enough, a connection using Telnet is called a virtual terminal (vty) session, or connection. Rather than using a physical device to connect to the server, Telnet uses software to create a virtual device that provides the same feature of a terminal session with access to the server's command line interface (CLI).

# Security Issues with Telnet
    Although the Telnet protocol can requre a user to login, it does not support transporting encrypted data. All data exchanged during Telnet sessions is transported as plaintext across the network. This means that the data can be easily intercepted and understood.
    The Secure Shell (SSH) protocol offers an alternate and secure mthod for server access. SSH provides the structure for secure remote login and other secure network services. It also provides stronger authentication that Telnet and supports transporting session data using encryption. As a best practice, network professionals should always use SSH in place of Telnet, whenever possible.

## Email and Messaging
# Email Clients and Servers
    Email is one of the most popuar client/server applications on the internet. Email servers run server software that enables them to interact with clients and with other email servers over the network.
    Each mail server receives and stores mail for users who have mailboxes configured on the mail server. Each user with a mailbox must then use an email client to acces the mail server and read these messages. Many internet messageing systems use a web-based client to access email. For examples, Microsoft 365, Yahoo, and Gmail.
    Mailboxes are identified by the format: user@company.domain
    Various application protocols used in processing email include SMTP (Simple Mail Transfer Protocol), POP3 (Post Office Protocol version 3), and IMAP4 (Internet Message Access Protocol version4).

# Email Protocols
    Simple Mail Transfer Protocol (SMTP)
        SMTP is used by an email client to send messages to its local email server. The local server then decides if the message is destined for a local mailbox or if the message is addressed to a mailbox on another server.
        If the server has to send the message to a different server, SMTP is used between those two servers as well. SMTP requests are sent to port 25.

    Post Office Protocol version 3 (POP3)
        A server that supports POP clients receives and stores messages addressed to its users. When the client connects to the email server, the messages are downloaded to the client. By default, messages are not kept on the server after they have been accessed by the client. Clients contact POP3 servers on port 110.

    Internet Message Access Protocol version4 (IMAP4)
        A server that supports IMAP clients also receives and stores messages addressed to its users. However, unlike POP, IMAP keeps the messages in the maiboxes on the server, unless they are deleted by the user. The most current version of IMAP is IMAP4 which listens for client requests on port 143.
        Many different email servers exist for the various network operating system platforms.

# Text Messaging
    Text messaging is one of the most popular communication tools in use today. In addition, text messaging software is built into many online applications, smartphone apps, and social media sites.
    Text messages may also be called instant messages, direct messages, private messages, and chat messages. Text messaging enables users to communicate or chat over the internet in real-time. Text messaging services on a computer are usually accessed through a web-based client that is intergrated into social media or information sharing site. These clients usually only connect to other users of the same site.
    There are also a number of standalone text message clients such as Cisco Webex Teams, Microsoft Teams, Whatsapp, Facebook Messenger, and many others. These applications are available for a wide variety of operating systems and devices. A mobile version is typically offered. In addition to text messages, these client support the transfer of documents, video, music, and audio files.

# Internet Phone Calls
    Making telephone calls over the internet is becoming increasingly popular. An internet telephony client uses-peer-to-peer technology similar to that used by instant messaging. IP telephony makes use of Voice over IP (VoIP) technology, which converts analog voice signals into digital data. The voice data is encapsulated into IP packets which carry the phone call through the network.
    When the IP phone software has been installed, the user seletcs a unique name. This is so that calls can be received from other users. Speakers and a microphone, built-in or separate, are required. A headset is frequently plugged into the computer to serve as a phone.
    Calls are made to other users of the same service on the internet, by selecting the username from a list. A call to a regular telephone (landline or cell phone) requires a gateway to access the Public Switched Telephone Network (PSTN). Depending on the service, there may be charges associated with this type of call. The protocols and destination ports used by internet telephony applications can vary based on the software.

