# HTTPS/TLS Analysis using Wireshark

## Objective

To capture and analyze HTTPS traffic and understand how TLS establishes secure communication between a client and a server.

## Environment

- Operating System: Kali Linux
- Tool: Wireshark
- Interface: eth0
- Protocol: TLSv1.3

## Procedure

1. Started packet capture on eth0.
2. Opened a web browser.
3. Visited a secure HTTPS website.
4. Applied the filter:

```text
tls
```

5. Observed TLS handshake packets.

## Observations

### Client Information

- Client IP: 10.0.2.15

### Server Information

- Server IP: 151.101.209.91

### TLS Handshake

#### Client Hello

The client initiated the secure connection by sending a TLS Client Hello message containing supported TLS versions and cipher suites.

#### Server Hello

The server responded with a Server Hello message and selected the TLS configuration.

#### Change Cipher Spec

The communication switched to encrypted mode.

#### Application Data

Encrypted application data was exchanged between the client and server.

## Analysis

The TLS handshake successfully established a secure communication channel between the client and server.

Observed sequence:

```text
Client Hello
Server Hello
Change Cipher Spec
Encrypted Application Data
```

The traffic was encrypted using TLSv1.3, preventing unauthorized parties from viewing transmitted data.

## Security Relevance

SOC Analysts analyze TLS traffic to:

- Investigate encrypted communications
- Validate secure connections
- Review certificate information
- Detect suspicious domains
- Identify malware command-and-control traffic

## Findings

- TLSv1.3 traffic observed.
- Successful TLS handshake completed.
- Encrypted communication established.
- Application data exchanged securely.
- No suspicious activity detected.

## Verdict

Normal Secure HTTPS Communication

## Conclusion

The TLS handshake was successfully captured and analyzed using Wireshark. A secure encrypted connection was established between the client and server using TLSv1.3.
