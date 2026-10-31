# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Output
```
1. ipconfig
C:\> ipconfig

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   IPv4 Address. . . . . . . . . . . : 192.168.1.10
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1

C:\> ipconfig /all

Ethernet adapter Ethernet:

   Host Name . . . . . . . . . . . . : PC-A
   Physical Address. . . . . . . . . : 00-1A-2B-3C-4D-5E
   DHCP Enabled. . . . . . . . . . . : Yes
   IPv4 Address. . . . . . . . . . . : 192.168.1.10(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Lease Obtained. . . . . . . . . . : Saturday, October 17, 2026 9:00:12 AM
   Lease Expires . . . . . . . . . . : Sunday, October 18, 2026 9:00:12 AM
   Default Gateway . . . . . . . . . : 192.168.1.1
   DHCP Server . . . . . . . . . . . : 192.168.1.1
   DNS Servers . . . . . . . . . . . : 8.8.8.8
                                       8.8.4.4

C:\> ipconfig /release
C:\> ipconfig /renew
C:\> ipconfig /flushdns

Successfully flushed the DNS Resolver Cache.
2. ping
C:\> ping 127.0.0.1

Pinging 127.0.0.1 with 32 bytes of data:
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Ping statistics for 127.0.0.1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

C:\> ping 192.168.1.1

Pinging 192.168.1.1 with 32 bytes of data:
Reply from 192.168.1.1: bytes=32 time=2ms TTL=64
Reply from 192.168.1.1: bytes=32 time=1ms TTL=64
Reply from 192.168.1.1: bytes=32 time=2ms TTL=64
Reply from 192.168.1.1: bytes=32 time=1ms TTL=64

Ping statistics for 192.168.1.1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 1ms, Maximum = 2ms, Average = 1ms

C:\> ping 8.8.8.8

Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=21ms TTL=117
Reply from 8.8.8.8: bytes=32 time=20ms TTL=117
Reply from 8.8.8.8: bytes=32 time=22ms TTL=117
Reply from 8.8.8.8: bytes=32 time=20ms TTL=117

Ping statistics for 8.8.8.8:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 20ms, Maximum = 22ms, Average = 20ms

C:\> ping google.com

Pinging google.com [142.250.195.78] with 32 bytes of data:
Reply from 142.250.195.78: bytes=32 time=22ms TTL=116
Reply from 142.250.195.78: bytes=32 time=21ms TTL=116
Reply from 142.250.195.78: bytes=32 time=22ms TTL=116
Reply from 142.250.195.78: bytes=32 time=21ms TTL=116

C:\> ping 192.168.1.99

Pinging 192.168.1.99 with 32 bytes of data:
Reply from 192.168.1.10: Destination host unreachable.
Request timed out.

Ping statistics for 192.168.1.99:
    Packets: Sent = 4, Received = 1, Lost = 3 (75% loss),

C:\> ping -n 2 192.168.1.1
C:\> ping -t 192.168.1.1
C:\> ping -l 1000 192.168.1.1
3. tracert
C:\> tracert 8.8.8.8

Tracing route to dns.google [8.8.8.8]
over a maximum of 30 hops:

  1     1 ms     1 ms     1 ms  192.168.1.1
  2     8 ms     7 ms     8 ms  10.20.0.1
  3    12 ms    11 ms    12 ms  172.16.5.9
  4    18 ms    17 ms    18 ms  108.170.250.1
  5    20 ms    20 ms    21 ms  dns.google [8.8.8.8]

Trace complete.

C:\> tracert -d -h 10 8.8.8.8
4. pathping
C:\> pathping 8.8.8.8

Tracing route to dns.google [8.8.8.8]
over a maximum of 30 hops:
  0  PC-A [192.168.1.10]
  1  192.168.1.1
  2  10.20.0.1
  3  dns.google [8.8.8.8]

Computing statistics for 75 seconds...
            Source to Here   This Node/Link
Hop  RTT    Lost/Sent = Pct  Lost/Sent = Pct  Address
  0                                           PC-A [192.168.1.10]
                                0/ 100 =  0%   |
  1    1ms     0/ 100 =  0%     0/ 100 =  0%  192.168.1.1
                                0/ 100 =  0%   |
  2    8ms     0/ 100 =  0%     0/ 100 =  0%  10.20.0.1
                                0/ 100 =  0%   |
  3   20ms     0/ 100 =  0%     0/ 100 =  0%  dns.google [8.8.8.8]

Trace complete.
5. nslookup
C:\> nslookup google.com

Server:  dns.google
Address:  8.8.8.8

Non-authoritative answer:
Name:    google.com
Addresses:  142.250.195.78

C:\> nslookup google.com 8.8.4.4

Server:  dns.google
Address:  8.8.4.4

Non-authoritative answer:
Name:    google.com
Addresses:  142.250.195.78

C:\> nslookup -type=MX gmail.com

Non-authoritative answer:
gmail.com   MX preference = 5, mail exchanger = gmail-smtp-in.l.google.com

C:\> nslookup -type=NS example.com
6. arp
C:\> arp -a

Interface: 192.168.1.10 --- 0x4
  Internet Address      Physical Address      Type
  192.168.1.1           a4-2b-b0-11-22-33     dynamic
  192.168.1.20          3c-5a-b4-aa-bb-cc     dynamic
  192.168.1.255         ff-ff-ff-ff-ff-ff     static
  224.0.0.22            01-00-5e-00-00-16     static
  255.255.255.255       ff-ff-ff-ff-ff-ff     static

C:\> arp -a 192.168.1.1
7. netstat
C:\> netstat -an

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    0.0.0.0:135            0.0.0.0:0              LISTENING
  TCP    0.0.0.0:445            0.0.0.0:0              LISTENING
  TCP    192.168.1.10:50122     142.250.195.78:443     ESTABLISHED
  TCP    192.168.1.10:50130     52.96.100.10:443       TIME_WAIT
  UDP    0.0.0.0:5353           *:*
  UDP    192.168.1.10:137       *:*

C:\> netstat -e

Interface Statistics

                           Received            Sent
Bytes                    1285647390       214356789
Unicast packets             1054321          812345
Errors                            0               0
Discards                          0               0

C:\> netstat -s

IPv4 Statistics
  Packets Received                   = 1054321
  Received Address Errors            = 0
  Packets Forwarded                  = 0
  Output Requests                    = 812345

TCP Statistics for IPv4
  Active Opens                       = 4521
  Passive Opens                      = 312
  Failed Connection Attempts         = 14
  Current Connections                = 22

C:\> netstat -r
C:\> netstat -o
C:\> netstat -b
8. route
C:\> route print

IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
          0.0.0.0          0.0.0.0      192.168.1.1    192.168.1.10     25
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    331
      192.168.1.0    255.255.255.0         On-link      192.168.1.10    281
     192.168.1.10  255.255.255.255         On-link      192.168.1.10    281
    192.168.1.255  255.255.255.255         On-link      192.168.1.10    281
===========================================================================

C:\> route add 10.0.0.0 mask 255.255.255.0 192.168.1.1
 OK!

C:\> route delete 10.0.0.0
 OK!
9. getmac
C:\> getmac

Physical Address    Transport Name
=================== ==========================================================
00-1A-2B-3C-4D-5E   \Device\Tcpip_{3F2A9C1E-5B7D-4E8A-9C21-7D4E5F6A8B90}

C:\> getmac /v

Connection Name Network Adapter          Physical Address    Transport Name
=============== ======================== =================== ==============
Ethernet        Intel(R) Ethernet        00-1A-2B-3C-4D-5E   \Device\Tcpip_{...}
10. nbtstat
C:\> nbtstat -n

Ethernet:
Node IpAddress: [192.168.1.10] Scope Id: []

                NetBIOS Local Name Table

   Name               Type         Status
   ---------------------------------------------
   PC-A           <00>  UNIQUE      Registered
   WORKGROUP      <00>  GROUP       Registered

C:\> nbtstat -a 192.168.1.20
C:\> nbtstat -c
```

## Result
Thus Execution of Network commands Performed 
