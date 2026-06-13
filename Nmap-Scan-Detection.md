# Nmap scan Detection using Wireshark

## Objective
Detect Nmap SYN scan traffic using Wireshark.

## Tools Used
- Kali Linux
- Nmap
- Wireshark

## Command Executed 
''''bash
nmap 10.0.2.2
'''

## Wireshark Filter

'''text
tcp.flags.synn == 1 && tcp.flags.ack == 0
'''
## Findings
Observed multiple TCP SYN packets from source IP 10.0.2.15 to destination IP 10.0.2.2
Nmap performed a SYN scan aganist the target host.

Open ports discovered:

- TCP 135 (MSRPC)
- TCP 445 (Microsoft-DS)

## Analysis 
The SYN packets indicates reconnaissance activity. Attackers commonly use Nmap to identify open ports and services before attempting exploitation.

The scan generated connection attempts to multiple ports without completing the TCP handshake.

## Conclusion 

Nmap SYN scan activity was successfully captured and analyzed using Wireshark. Open port 135 and 445 were identified on the target host.
