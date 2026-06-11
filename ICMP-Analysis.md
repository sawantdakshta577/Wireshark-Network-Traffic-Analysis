# ICMP Traffic Analysis using Wireshark (Kali Linux)

## Objective

To capture and analyze ICMP (Internet Control Message Protocol) traffic using Wireshark in Kali Linux and understand how network connectivity is verified through ping requests and replies.

## Environment

* Operating System: Kali Linux
* Tool: Wireshark
* Interface: eth0
* Target Host: 8.8.8.8 (Google DNS)

## Procedure

1. Opened Wireshark in Kali Linux.
2. Selected the network interface (eth0).
3. Started packet capture.
4. Opened a terminal and executed:

```bash
ping -c 4 8.8.8.8
```

5. Stopped packet capture after receiving replies.
6. Applied the display filter:

```text
icmp
```

## Observations

### Echo Request

* Source IP: Local Kali Linux Machine
* Destination IP: 8.8.8.8
* Protocol: ICMP
* Type: Echo Request

### Echo Reply

* Source IP: 8.8.8.8
* Destination IP: Local Kali Linux Machine
* Protocol: ICMP
* Type: Echo Reply

## Analysis

The Wireshark capture showed ICMP Echo Requests sent from the local system to Google's DNS server (8.8.8.8). Each request received a corresponding Echo Reply, confirming successful network communication and connectivity.

ICMP is commonly used for troubleshooting and network diagnostics. The ping command relies on ICMP Echo Request and Echo Reply messages to determine whether a host is reachable.

## Security Relevance

SOC Analysts use ICMP traffic analysis to:

* Verify network connectivity
* Detect host discovery scans
* Investigate reconnaissance activity
* Troubleshoot communication issues
* Identify abnormal network behavior

## Findings

* ICMP traffic was successfully captured.
* Echo Requests and Echo Replies were observed.
* No suspicious or malicious activity was detected.
* Communication with 8.8.8.8 was successful.

## Verdict

Normal Network Activity

## Conclusion

The ICMP analysis confirmed successful communication between the Kali Linux system and Google DNS. Wireshark effectively captured and displayed the ICMP packets, providing visibility into network connectivity and protocol behavior.

