# Phishing Analysis – Greenholt Scenario

## Overview
This project looks at a financial-themed email that claimed to reference a wire transfer.
It documents how the email was reviewed and why it was ultimately treated as phishing, using the same kind of evidence a SOC analyst would rely on during a real investigation.

---

## Objective
Analyze the email to determine whether it was real or a phishing attempt and decide whether it required action or could be safely ignored.

<img src="images/original_email.png" width="700">

---

## Phishing Analysis Approach

When reviewing a potentially malicious email, SOC analysts typically focus on a few core questions:

- Who does the sender claim to be and can that identity be trusted?
- Where are replies actually routed and does this match the sender’s domain?
- Where did the email originate from at the infrastructure level?
- What does the attachment or link actually contain, not just what it is labeled as?
- Does the message create false urgency or financial pressure to influence the recipient?

This approach helps separate legitimate business emails from impersonation and malware delivery attempts.

---

## Key Findings (red flags)
The following red flags were identified during review of the email and its attachment.

- The sender claimed to be from `mutawamarine.com`, but replies were redirected to a different domain, which is a strong sign of impersonation.

<img src="images/reply_to_mismatch.png" width="700">

- The originating IP resolved to a generic hosting provider rather than real corporate mail infrastructure.

<img src="images/originating_ip.png" width="700">

- The attachment looked like a PDF but was actually a compressed RAR archive, a common trick used to deliver malware.

<img src="images/attachment_filetype.png" width="700">

- The email used a fake wire transfer to create a sense of urgency and pressure the recipient to open the attachment

---

## Conclusion
This was confirmed to be a phishing email attempting to deliver malware.
The sender behavior, infrastructure mismatch and deceptive attachment format all point to malicious intent.

---

## Recommended Actions
- Block the sender domain and originating IP  
- Block the attachment hash and similar file patterns  
- Advise users to report unexpected financial transfer emails  

---

## Takeaway
This scenario shows how phishing emails can look real at first glance and how small details such as reply to behavior and attachment format are often what make the difference when reaching a confident conclusion.
