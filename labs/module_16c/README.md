### Packet Tracer - Use FTP Services

## Overview
    The server is configured to run the service where clients connect, login, and transfer files. FTP uses port 21 as the server where clients connect, login, and transfer files. FTP uses port 21 as the server command port to create the connection. FTP then uses port 20 for data transfer.
        TFP Server (ftp.pka) - Interface (NIC)
        IP Address           - 209.165.200.226
        Subnet Mask          - 255.255.255.244

## Objectives
    Upload a file to an FTP server
    Download a file from an FTP server

## Topology
    Describe the devices used:
        One PC
        One Router
        FTP Server (ftp.pka)
        ![Network Topology](images/topology.png)

## Configuration Summary
    Step 1:
        The Command Prompt (under Desktop tab), '?' was entered into the command to list the available commands. Later 'dir' command is entered in the prompt to see the files on the PC. It is observed that there is a "sampleFile.txt" file in the C:\directory.

            ![Commands used](images/dir_?.png)
                The output of the command 'dir':
                    C:\> dir
                    Volume in drive C has no label
                    Volume Serial Number is 5E12-4AF3
                    Directory of C:\
                    12/31/1969 17:0 PM 26 sampleFile.txt
                    26 bytes 1 File(s)

    Step 2:
        Connecting to the FTP server at 209.165.200.226 (or with its DNS ftp.pka).
            The output of the command is as follow:
                C:\> ftp 209.165.200.226
                    Trying to connect...209.165.200.226
                    Connected to 209.165.200.226

        Connection successful. Entering username 'student' and password 'class' to gain access.
            220- Welcome to PT Ftp server
                Username:student
                331- Username ok, need password
                Password:
                230- Logged in
                (passive mode On)

    Step 3:
        Entering '?' command in the prompt to list the commands available in the ftp client and 'dir' to see the files available on the server.
        
## Verification

