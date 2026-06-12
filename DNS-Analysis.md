# DNS Traffic Analysis using Wireshark (kali Linux)

## Objective 
To capture and analyze DNS traffic using Wireshark and understand how domain names are resolved into IP addresses.

## Environment 
- Operation System: Kali Linux
- Tool: Wireshark
- Interface: eth0

  ## Procedure
  1. Started packets capture on eth0.
  2. Generated DNS traffic using:
 
  '''bash
  nslookup google.com
  '''

 3. Stopped the capture.
 4. Applied the filter:

'''text
dns
'''

## Observation

### DNS Query
- Query Name: google.com
- Query type: A Record
- Protocol: DNS

### DNS Response

-Domain: google.com
-Returned IP Address: [Captured IP]
-Protocol: DNS

## Analysis
DNS converts human-readable domain names into IP addresses. The captured traffic showed a DNS query requesting the IP address for google.com and a DNS response containing the resolved IP address.

## Security Relevance
SOC Analysts  monitor DNS traffic to:

- Detect malicious domains
- Tnvestigate malware communication
- Identify DNS tunneling
- Track suspicious network activity

  ## findings

  - DNS query sucessfully captured.
  - DNS response successfully captured.
  - Domain resolution completed successfully.
  - no  suspicious activity detected.
 
    ## Verdict
    Normal DNS Activty

    ## Conclusion

  DNS traffic was successfully analyzed using wireshrk. The capture demonstrated how domain name are resolved into IP addresses through DNS queries and responses.


  
