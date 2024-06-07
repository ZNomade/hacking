
**# NMAP Cheat Sheet 🔺**

## 1. Nmap Basic Scanning

- `nmap -sV [host]` - Version Detection, default scan
- `nmap -sS [host]` - SYN Stealth Scan
- `nmap -sU [host]` - UDP Scan
- `nmap -sT [host]` - TCP Connect() Scan
- `nmap -sN [host]` - TCP Null Scan
- `nmap -sF [host]` - TCP FIN Scan

## 2. Nmap Host Discovery

- `nmap -sL [host/network]` - List Scan - Discover targets by querying DNS or the targets in a network
- `nmap -sn [host/network]` - Ping Scan - Determine if hosts are alive
- `nmap -Pn [host/network]` - Skip host discovery

## 3. Nmap Port Scanning

- `nmap -sC [host]` - Script Scan - Execute default nmap scripts
- `nmap -p [ports] [host]` - Scan specific ports
- `nmap -F [host]` - Fast Scan - Scan for the most commonly used ports

## 4. Nmap Advertising Scanning

- `nmap -oA [filename] [host]` - Output scan in all formats
- `nmap -O [host]` - Probe Operating System fingerprints
- `nmap [host] --traceroute` - Trace host hops

## 5. Nmap Version Detection

- `nmap -sV [host]` - Show versions of services and OS
- `nmap -A [host]` - Advanced Scan - OS and service version and script scanning
- `nmap --script [name] [host]` - Execute a custom script

## 6. Nmap Timing Options

- `nmap -T[0-5] [host]` - Timing for scans

## 7. Nmap Firewall/IDS Evasion

- `nmap --spoof-mac [address]` - Changes source MAC address
- `nmap -D RND:10 [host]` - Decoy Scan - Appear to scan from multiple hosts
- `nmap -f` - Fragmented Packets - Fragment Packets
- `nmap -Pn [host]` - Skip host discovery
- `nmap --data-length [length]` - Append random data to packet
