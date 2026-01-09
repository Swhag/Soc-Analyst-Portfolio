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
   - Identify anything noisy, repetitive, or unexpected

2. **Pivot**
   - Narrow focus to a specific host, protocol, or conversation

3. **Validation**
   - Inspect packet details and streams
   - Confirm whether behavior is expected or suspicious

4. **Summary**
   - Document what happened, who was involved, and why it matters

---