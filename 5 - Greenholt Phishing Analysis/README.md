# Phishing Analysis – Greenholt Scenario

## Summary
A financial-themed email claiming to reference a wire transfer was investigated to determine legitimacy.
The message was confirmed as a phishing attempt designed to deliver a malicious attachment.

---

## Key Findings (red flags)

- The sender claimed to be from `mutawamarine.com`, but replies were redirected to a different domain, indicating impersonation.

<img src="images/reply_to_mismatch.png" width="700">

- The originating IP resolved to a generic hosting provider rather than corporate mail infrastructure.

<img src="images/originating_ip.png" width="700">

- The attachment appeared to be a PDF but was actually a compressed RAR archive, a common malware delivery tactic.

<img src="images/attachment_filetype.png" width="700">

- The financial pretext was designed to pressure the recipient into opening the attachment quickly.


---

## Verdict
**True Positive – Phishing (Malware Delivery)**

The combination of sender impersonation, infrastructure mismatch, and deceptive attachment formatting confirms malicious intent.

---

## Recommended Actions
- Block the sender domain and originating IP
- Block the attachment hash and similar file patterns
- Advise users to report unexpected financial transfer emails

---

## Takeaway
This case highlights how phishing emails can appear legitimate at first glance and why small inconsistencies such as reply-to behavior and attachment format are critical in reaching a confident verdict.
