# Initial Nmap Findings

## Objective
Identify open TCP ports and the services running on my own Windows PC.

## Tool
Nmap 7.99.1

## Results
- **135/tcp:** Microsoft Windows RPC
- **139/tcp:** NetBIOS Session Service
- **445/tcp:** Microsoft SMB-related service

## Initial Assessment
Three TCP ports were reported as open. These services support Windows system communication and network sharing. Their presence alone does not establish a security vulnerability.