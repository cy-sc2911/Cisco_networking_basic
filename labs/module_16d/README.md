# Packet Tracer - Use Telnet and SSH

## Objectives
Establish a remote connections to a router using Telnet and SSH.
- Verify connectivity
- Access a remote device

|DEVICE | INTERFACE | IP Address | Subnet Mask |
|-------|-----------|------------|-------------|
| HQ | G0/0/1 | 64.100.1.1 | 255.255.255.0 |
| PC0 | NIC | N/A | DHCP |
| PC1 | NIC | N/A | DHCP |

## Topology
Describe the devices used:
- 2 PCs (PC0 and PC1)
- 1 Router (HQ)

## Configuration and Verification Summary
### Step 1:
Verify that the PC has IP addressing and can ping the remote router by typing 'ipconfig' on the Command Prompt under "Desktop". Below is the output of the command:

    C:\>ipconfig
    FastEthernet0 Connection:(default port)
    Connection-specific DNS Suffix..:
    Link-local IPv6 Address.........: FE80::201:C7FF:FE9A:30C1
    IPv6 Address....................: ::
    IPv4 Address....................: 192.168.1.12
    Subnet Mask.....................: 255.255.255.0
    Default Gateway.................: ::
                                        192.168.1.1
    Bluetooth Connection:
    Connection-specific DNS Suffix..:
    Link-local IPv6 Address.........: ::
    IPv6 Address....................: ::
    IPv4 Address....................: 0.0.0.0
    Subnet Mask.....................: 0.0.0.0
    Default Gateway.................: ::
                                        0.0.0.0

### Step 2:
Verify connectivity to HQ by typing 'ping 64.100.1.1' in the Command Prompt. Below is the output of the prompt:

    C:\>ping 64.100.1.1
    Pinging 64.100.1.1 with 32 bytes of data:
    Request timed out.
    Reply from 64.100.1.1: bytes=32 time<1ms TTL=253
    Reply from 64.100.1.1: bytes=32 time<1ms TTL=253
    Reply from 64.100.1.1: bytes=32 time<1ms TTL=253
    Ping statistics for 64.100.1.1:
        Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),
    Approximate round trip times in milli-seconds:
        Minimum = 0ms, Maximum = 0ms, Average = 0ms

### Step 3:
Attempting to establish a remote connection using Telnet by typing 'Telnet 64.100.1.1'. Below is the output of the prompt:

    C:\>telnet 64.100.1.1
    Trying 64.100.1.1 ...Open

    [Connection to 64.100.1.1 closed by foreign host]

The connection is not successful because the router is configured to not allow insecure Telnet access.

Attempting to establish a remote connection using SSH by typing ssh -l admin 64.100.1.1. The password is 'class'. Below is the output of the prompt:

    C:\>ssh -l admin 64.100.1.1

    Password:

    HQ#
