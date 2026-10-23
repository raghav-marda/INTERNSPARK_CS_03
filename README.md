# InternSpark Cybersecurity Internship – Task 3
## Wireshark Packet Analysis

![Wireshark](https://img.shields.io/badge/Tool-Wireshark-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)
![Task](https://img.shields.io/badge/Task-03-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This repository contains the practical work completed for **Task 3: Wireshark Packet Analysis** as part of the InternSpark Cybersecurity Internship.

The objective of this task was to capture live network traffic and analyze different network protocols using Wireshark. The analysis focused on DNS queries and responses, TCP connection flags, and packets identified by Wireshark as retransmissions.

## 🎯 Objectives

- Capture live network traffic using Wireshark.
- Identify DNS queries and responses.
- Analyze TCP SYN, SYN-ACK, and ACK packets.
- Observe TCP retransmissions and understand their possible causes.
- Apply Wireshark display filters for packet analysis.
- Document observations using screenshots and a packet capture file.

## 🛠️ Tools & Technologies

- **Wireshark 4.6.9** – Network traffic capture and protocol analysis.
- **Npcap 1.88** – Packet capture support for Windows.
- **Operating System:** Windows.
- **Interface:** Wi-Fi.

## 🔍 Methodology

### 1. Live Traffic Capture
Selected the Wi-Fi network interface in Wireshark and captured live network packets.

### 2. DNS Analysis
Applied the display filter `dns` to inspect DNS queries and responses and observe domain name resolution traffic.

### 3. TCP SYN Analysis
Applied the filter `tcp.flags.syn == 1 && tcp.flags.ack == 0` to identify initial TCP SYN packets.

### 4. TCP SYN-ACK Analysis
Applied the filter `tcp.flags.syn == 1 && tcp.flags.ack == 1` to identify TCP SYN-ACK packets.

### 5. TCP ACK Analysis
Applied the filter `tcp.flags.syn == 0 && tcp.flags.ack == 1 && tcp.len == 0` to inspect TCP ACK packets with no payload.

### 6. Retransmission Analysis
Applied the filter `tcp.analysis.retransmission` to identify packets labelled as TCP retransmissions by Wireshark.

## 📊 Findings & Observations

### 1. DNS Queries and Responses
DNS packets were observed, including queries and responses associated with domain lookups. DNS helps translate domain names into IP addresses and other DNS records.

### 2. TCP Connection Establishment
TCP SYN and SYN-ACK packets were observed. These packets represent key stages of TCP connection establishment. ACK packets were also captured as part of TCP communication.

### 3. TCP Retransmissions
Wireshark identified packets as TCP retransmissions. Such retransmissions may be associated with packet loss, network delays, or acknowledgements that were not received as expected. These observations alone do not confirm a network attack or security vulnerability.

## 📸 Screenshots & Evidence

The `screenshots/` directory contains the following evidence:

| Screenshot | Description |
|---|---|
| `01_dns_query_response.png` | DNS query and response traffic |
| `02_tcp_syn.png` | Initial TCP SYN packets |
| `03_tcp_syn_ack.png` | TCP SYN-ACK packets |
| `04_tcp_ack.png` | TCP ACK packets |
| `05_tcp_retransmission.png` | Packets labelled as TCP retransmissions |

## 📁 Repository Structure

```text
INTERNSPARK_CS_03/
├── README.md
├── screenshots/
│   ├── 01_dns_query_response.png
│   ├── 02_tcp_syn.png
│   ├── 03_tcp_syn_ack.png
│   ├── 04_tcp_ack.png
│   └── 05_tcp_retransmission.png
├── capture/
│   └── internspark_task3_capture.pcapng
└── report/
    └── Wireshark_Packet_Analysis_Report.pdf
```

*The structure above is the planned organization; include files and folders as they are actually uploaded.*

## 🛡️ Security Considerations

- The capture was performed on the author's own Wi-Fi interface for educational purposes.
- Retransmissions are network observations and are not, by themselves, evidence of a vulnerability or malicious activity.
- The capture file may contain network metadata and should be shared carefully.
- No confirmed security vulnerability or attack is claimed based solely on this analysis.

## 📚 Learning Outcomes

- Learned to capture live network traffic using Wireshark.
- Practiced display filters for DNS and TCP packets.
- Understood TCP SYN, SYN-ACK, and ACK flags.
- Observed Wireshark retransmission indicators.
- Gained practical experience in network traffic analysis and technical documentation.

## ⚠️ Disclaimer

This project was conducted for educational purposes as part of the InternSpark Cybersecurity Internship. Analysis is limited to the packets captured during this session. Findings should not be interpreted as proof of a security incident without further investigation.

---

**InternSpark Cybersecurity Internship | Task 3 – Wireshark Packet Analysis**
