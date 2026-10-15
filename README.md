# Network Security Investigation

## About the Project

This project is about investigating the network services running on my own Windows computer. I used Nmap to identify open ports and selected Wireshark to learn how network traffic can be captured and analyzed.

The main goal was to understand how network services can be identified, how traffic can be observed, and how the findings can be documented as part of a basic security investigation.

## Tools Used

- **Nmap 7.99.1** — Port scanning and service detection
- **Wireshark** — Network packet capture and analysis
- **Windows** — Target operating system

## Investigation Process

1. Identified the local IP address of my Windows computer.
2. Scanned the computer using Nmap.
3. Identified the open TCP ports and their reported services.
4. Opened Wireshark and performed a short network capture.
5. Documented the scan results and the limitations of the available evidence.

## Nmap Results

The scan identified three open TCP ports.

| Port | Service | Purpose |
|---|---|---|
| 135/tcp | Microsoft RPC | Communication between Windows components and services |
| 139/tcp | NetBIOS-SSN | Legacy Windows network communication |
| 445/tcp | Microsoft-DS | Commonly associated with Windows SMB networking and file sharing |

Nmap also reported that the host was active and identified Windows as the operating system family.

### What I Learned

The scan helped me understand that different ports are associated with different network services. Open ports are not automatically vulnerabilities; their security depends on the service configuration, firewall rules, updates, and whether access is necessary.

## Wireshark Analysis

Wireshark was used to make a short initial capture. Detailed packet-level findings have not yet been confirmed, so this project does not claim specific DNS, SMB, TCP, or ICMP observations.

Useful display filters for further analysis include:

- `dns` — DNS traffic
- `tcp` — TCP packets
- `smb || smb2` — SMB traffic
- `icmp` — ICMP traffic, including some ping activity

Any final conclusions about captured traffic should be based on the actual packets observed.

## Project Structure

```text
Network-Security-Investigation/
├── README.md
├── evidence/
│   ├── lab-details.txt
│   ├── nmap-scan.txt
│   └── wireshark-capture.pcapng
├── analysis/
│   └── findings.md
└── report/
    └── Network_Security_Investigation_Report.pdf
```

## Limitations

- The Nmap scan covered the common TCP ports scanned by default.
- Service version identification may be incomplete.
- The initial Wireshark capture was short.
- This project is a basic network investigation, not a complete vulnerability assessment or penetration test.

## Conclusion

This project helped me understand how Nmap can identify open ports and how Wireshark can be used to inspect network traffic. It also taught me the importance of documenting evidence carefully and avoiding security conclusions that are not supported by the results.

## Safety and Privacy

The investigation was performed on my own computer in a controlled environment. Before publishing evidence, private IP addresses and sensitive packet information should be reviewed and removed where necessary.