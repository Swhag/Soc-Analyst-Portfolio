# Wireshark Traffic Analysis

## Overview
This project analyzes network traffic captures (PCAP/PCAPNG) in Wireshark to identify suspicious patterns and potential malicious activity. The focus is on practical SOC style investigation: filtering, pivoting, validating findings, and summarizing what happened.

---

## Objective
- Identify suspicious patterns in network traffic  
- Correlate packet-level artifacts into clear findings  
- Practice a repeatable traffic-analysis workflow aligned with SOC operations  

---

## Tools
- Wireshark
- NetworkMiner

---

## Investigation Flow
1. **Initial triage**
   - Broad filters and protocol overview
   - Identify anything noisy, repetitive or unexpected

2. **Pivot**
   - Narrow focus to a specific host, protocol or conversation

3. **Validation**
   - Inspect packet details and streams
   - Confirm whether behavior is expected or suspicious

4. **Summary**
   - Document what happened, who was involved and why it matters

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
