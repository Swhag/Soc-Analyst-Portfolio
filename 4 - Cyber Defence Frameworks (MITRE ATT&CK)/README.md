# Cyber Defence Frameworks (MITRE ATT&CK)

## Overview
This project explores the MITRE ATT&CK framework and its role in modern SOC operations. It covers how ATT&CK organizes adversary behavior into tactics and techniques and why this framework is widely used across defensive security teams.

---

## 1. Objective
Demonstrate the ability to analyze attacker activity and map observed behavior to MITRE ATT&CK tactics and techniques during a security investigation.

---

## 2. MITRE and ATT&CK Background

### MITRE
MITRE is a non for-profit organization that develops research based frameworks and tools used across the cyber security industry. Many of these resources are widely adopted by SOCs, threat intelligence teams, and security vendors.

### MITRE ATT&CK
MITRE ATT&CK is a globally accessible knowledge base of adversary tactics and techniques based on real-world attacks. It provides a consistent way to describe how attackers operate and is commonly used to:
- Add context to alerts and incidents
- Map attacker behavior during investigations
- Improve detection coverage and response planning

---

## 3. Core ATT&CK Concepts

### Tactics
Tactics represent the **goal** an attacker is trying to achieve at a given stage of an attack (the “why”), such as Initial Access, Persistence, or Defense Evasion.

### Techniques
Techniques describe **how** the attacker accomplishes that goal.  
Each technique has a unique ID (for example, `T1566`) and may include multiple sub-techniques.

### Procedures
Procedures are the real-world implementation of a technique, often tied to specific tools, malware, or threat groups.

---

## 4. ATT&CK Matrix and Navigator

### ATT&CK Matrix
The ATT&CK Matrix visually organizes tactics across the top and techniques underneath each tactic. This layout makes it easier to understand how attacks progress and where activity fits in the broader lifecycle.

### ATT&CK Navigator
The ATT&CK Navigator is commonly used to:
- Highlight techniques used by a threat group
- Visualize attack paths
- Review detection coverage across tactics

SOC teams often use the Navigator during investigations, threat research, and post-incident reviews.

---
