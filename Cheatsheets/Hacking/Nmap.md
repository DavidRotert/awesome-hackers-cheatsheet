A **port scanner**.
# Quick examples
## Basic usage (in my opionion best setting for **Hack The Box**):
It is blazingly fast, but not stealthy and only scans important ports:
```
sudo nmap --stats-every 3s -sVC -oN nmap-common-tcp.nmap -T5 127.0.0.1
```
## With specific port range:
```
sudo nmap --stats-every 3s -p 1-1024 -T5 127.0.0.1
```
#### Without service scan:
```
sudo nmap -p80,22,21,8000-9999 -T5 127.0.0.1
```
## For UDP (only 100 most used ports, because UDP scans are slow and error prone):
```
sudo nmap -sU -F -T5 127.0.0.1
```
# Common flags and arguments

| Flag  | Description                                                                                                                                                                                                                                                         |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-p`  | Ports to scan. If you want to specify which protocol to use for which ports, you can prefix them with `U:` for **UDP** and `T:` for **TCP**, but, for this to work you need to provide the `-sU` and one of the **TCP scan types**. Example: `-p80,22,21,8000-9999` |
| `-F`  | Fast port scan. Scans only the top 100 ports                                                                                                                                                                                                                        |
| `-oN` | Save output to file (text)                                                                                                                                                                                                                                          |
| `-oX` | Save output to file (XML)                                                                                                                                                                                                                                           |
| `-oS` | **A joke parameter**. Saves output as a text file, but in *Script Kiddie* Language, for example `S3rv\|ce Unr3c0gn!z3d Desp1te rEtUrNing dAta`. **Please don't use this!**                                                                                          |
