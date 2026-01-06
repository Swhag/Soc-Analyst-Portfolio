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
MITRE ATT&CK is a globally accessible knowledge base of adversary tactics and techniques based on real world attacks. It provides a consistent way to describe how attackers operate and is commonly used to:
- Add context to alerts and incidents
- Map attacker behavior during investigations
- Improve detection coverage and response planning

---

## 3. Core ATT&CK Concepts

MITRE ATT&CK organizes adversary behavior using three core concepts:

- **Tactics**  
  The adversary’s objective or goal at a specific stage of an attack.

- **Techniques**  
  The methods used to achieve that objective. Each technique is assigned a unique ID.

- **Procedures**  
  The real-world execution of a technique, often tied to specific tools, malware, or threat groups.

This structure allows analysts to describe attacks in a clear and consistent way.

---

## 4. ATT&CK Matrix and Navigator

### ATT&CK Matrix
The ATT&CK Matrix visually organizes tactics across the top and techniques underneath each tactic. This layout makes it easier to understand how attacks progress and where activity fits in the broader lifecycle.

### ATT&CK Navigator
The ATT&CK Navigator is commonly used to:
- Highlight techniques used by a threat group
- Visualize attack paths
- Review detection coverage across tactics

SOC teams often use the Navigator during investigations, threat research, and post incident reviews.

---

## 5. Mapping Threat Intelligence to ATT&CK

### Why Mapping Matters
Threat intelligence reports often describe attacker activity in narrative form. Mapping that activity to ATT&CK techniques allows defenders to:
- Standardize how attacks are described
- Add meaningful context to alerts
- Translate intelligence into detections and response actions

### Example Use Case
When analyzing a known threat group, analysts can map observed behavior such as:
- Initial access via phishing
- Persistence mechanisms
- Defense evasion techniques
- Command-and-control methods

This structured approach helps identify defensive gaps and improve future readiness.

---


## 6. ATT&CK in SOC Operations

ATT&CK is used across multiple security roles:

- **SOC Analysts**  
  Map alerts and events to tactics and techniques to improve triage and prioritization.

- **Threat Intelligence Teams**  
  Build threat profiles by mapping observed behavior to ATT&CK.

- **Detection Engineers**  
  Align SIEM and EDR rules with ATT&CK techniques to ensure meaningful coverage.

- **Incident Responders**  
  Use ATT&CK to visualize attack progression during investigations.

---

## 7. MITRE CAR (Cyber Analytics Repository)

### CAR Overview
MITRE CAR is a collection of detection analytics mapped to ATT&CK techniques. Each analytic explains:
- What behavior to detect
- Why it matters
- How it maps back to ATT&CK

### Defensive Value
CAR helps bridge the gap between ATT&CK theory and real detections.  
Many analytics include example queries for tools like Splunk, allowing ATT&CK techniques to be turned into practical SIEM detections.

---

## 8. MITRE D3FEND (Defensive View)

### D3FEND Overview
MITRE D3FEND focuses on defensive techniques and countermeasures. It provides a structured way to describe how security controls detect, deny, or disrupt attacker activity.

### ATT&CK and D3FEND Together
Using both frameworks together allows defenders to understand:
- What the attacker is doing (ATT&CK)
- How defenders can respond or mitigate it (D3FEND)

---

## 9. Key Takeaways
- MITRE ATT&CK provides a common language for describing attacker behavior  
- Mapping activity to ATT&CK adds clarity and context to SOC investigations  
- ATT&CK is widely used across SOC, CTI, detection engineering, and incident response  
- MITRE CAR helps translate ATT&CK techniques into real detections  
- MITRE D3FEND complements ATT&CK by focusing on defensive controls  