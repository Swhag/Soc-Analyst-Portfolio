Overview

This document explains how alerts are formed, prioritized, and triaged by SOC Level 1 analysts.
It covers the end-to-end workflow from event generation → alert creation → prioritisation → triage → final verdict.

This material sets the foundation for all technical projects in this portfolio (Splunk, Elastic, Wireshark, endpoint detection, phishing, etc.).

---

## 1. From Events to Alerts

Security alerts originate from routine system activity:

Event occurs
Examples: user login, process creation, file download.

The system logs the event
Windows, Linux, firewalls, email gateways, cloud services, etc.

Logs are shipped into a security solution
Typically a SIEM, EDR, NDR, or SOAR.

Detection rules evaluate the logs
When unusual or suspicious patterns match a rule → an alert is generated.

Alerts allow analysts to review dozens of items instead of millions of raw logs.

---