# TCP Three-Way Handshake Analysis using Wireshark

## Objective

To capture and analyze the TCP Three-Way Handshake process using Wireshark in Kali Linux.

## Environment

- Operating System: Kali Linux
- Tool: Wireshark
- Interface: eth0

## Procedure

1. Started packet capture on eth0.
2. Opened a web browser and visited a website.
3. Applied the display filter:

```text
tcp
```

4. Identified the TCP Three-Way Handshake packets.

## Observations

### Client IP

```text
10.0.2.15
```

### Server IP

```text
34.160.144.191
```

### Step 1 - SYN

```text
10.0.2.15 → 34.160.144.191
[SYN]
```

The client initiated a connection request to the server.

### Step 2 - SYN ACK

```text
34.160.144.191 → 10.0.2.15
[SYN, ACK]
```

The server acknowledged the request and agreed to establish the connection.

### Step 3 - ACK

```text
10.0.2.15 → 34.160.144.191
[ACK]
```

The client acknowledged the server's response.

## Analysis

The TCP Three-Way Handshake successfully established a connection between the client and the server.

Sequence:

```text
SYN → SYN-ACK → ACK
```

After the handshake completed, encrypted TLS communication began.

## Security Relevance

SOC Analysts monitor TCP handshakes to:

- Detect connection attempts
- Identify port scanning activity
- Investigate suspicious communications
- Troubleshoot network connectivity issues

## Findings

- Successful TCP connection established.
- Handshake completed without errors.
- TLS communication started after connection establishment.
- No suspicious activity observed.

## Verdict

Normal TCP Communication

## Conclusion

The TCP Three-Way Handshake was successfully captured and analyzed using Wireshark. The connection was established correctly and was followed by secure TLS communication.
