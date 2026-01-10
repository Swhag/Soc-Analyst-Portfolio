# Wireshark Traffic Analysis

## Overview
This project focuses on analyzing network traffic in Wireshark to identify suspicious activity from a SOC analyst perspective. The goal is to demonstrate practical PCAP triage, anomaly detection, and clear documentation of findings.

---

## Objective
- Identify abnormal network behavior in packet captures
- Correlate packet-level artifacts into a clear investigation narrative
- Practice explaining findings the way a SOC analyst would

---

## Tools
- Wireshark

---

## Investigation Flow
1. **Initial triage**
   - Triage traffic to find what stands out

2. **Pivot**
   - Pivot on suspicious hosts or protocols

3. **Validation**
   - Validate behavior using packet details and streams

4. **Summary**
   - Summarize findings and next steps

---


## Traffic Analysis Notes

### 1) Nmap Scan Detection (TCP / UDP)
**Purpose:** Recognize common scanning behavior in network traffic.

#### What stands out
- SYN-only attempts without completed handshakes  
  → Repeated SYN packets from a single source strongly indicate scanning activity

- Window size differences between scan types  
  → Larger window sizes often align with TCP connect scans  
  → Smaller window sizes are commonly seen in SYN scans

- ICMP responses indicating closed UDP ports  
  → ICMP *Destination Unreachable (Port Unreachable)* messages often map back to UDP scan attempts

#### Useful filters
tcp.flags.syn==1 and tcp.flags.ack==0 and tcp.window_size > 1024   
tcp.flags.syn==1 and tcp.flags.ack==0 and tcp.window_size <= 1024   
icmp.type==3 and icmp.code==3   
