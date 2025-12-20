Capture-and-Analyze-Network-Traffic-Using-Wireshark
===================================================

Objective
---------
Capture live network packets and analyze basic traffic types using Wireshark.

Tools
-----
Wireshark (free and open-source packet analyzer)

Commands (Linux examples)
-------------------------
sudo apt update
sudo apt install wireshark -y

ifconfig
ip a

Start Wireshark
---------------
Open Wireshark
Select active network interface
Start packet capture
Generate traffic by browsing, pinging, SSH, etc.

Useful Filters
--------------
DNS traffic:
dns

HTTP traffic:
http

TCP packets:
tcp

UDP packets:
udp

Filter by IP:
ip.addr == 192.168.1.10

Filter by port:
tcp.port == 443

Filter by protocol errors:
tcp.analysis.flags

Save Capture
------------
File → Save As → example.pcapng

Analysis
--------
1. Identify top protocols in use (TCP, UDP, DNS, TLS, HTTP, ARP, etc.)
2. View packet details and payloads
3. Track client/server communication
4. Review packet source/destination IPs
5. Confirm connection-state and flags
6. Check response codes and latency

Example Observations
--------------------
DNS queries resolve domain names
TCP handshake: SYN → SYN/ACK → ACK
HTTP traffic shows GET/POST requests
ICMP traffic from ping tests
TLS encrypted packets show no payload content

Exporting Data
--------------
File → Export Packet Dissections
Formats: CSV, JSON, TXT

Screenshot Suggestion (Not included)
------------------------------------
- Interface selection page
- Live capture graph
- Filtered packet list view

Outcome
-------
You should see multiple traffic types including DNS, TCP, UDP, and ICMP. 
Packet inspection reveals communication patterns, response codes, latency, 
and device behavior across the network.

Notes
-----
Avoid capturing traffic on networks you do not own or have permission to scan.

Summary
-------
Wireshark is an effective tool for:
- Capturing live traffic
- Applying protocol filters
- Inspecting packets deeply
- Troubleshooting connectivity
- Understanding client/server behavior
- Exporting packet data for reporting
