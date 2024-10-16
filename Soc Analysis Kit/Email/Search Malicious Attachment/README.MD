# Search Malicious Attachment
This query searches for potentially malicious email attachments by analyzing records in the EmailAttachmentInfo table. It filters attachments based on a specific SHA-256 hash (representing the file's unique fingerprint)and narrows down results to those sent to email addresses within a particular domain.

This query is highly valuable for detecting and investigating email-based threats. By identifying whether a known malicious attachment has been delivered to users in the organization, security analysts can quickly assess the scope of a potential phishing or malware campaign.

![image](https://github.com/user-attachments/assets/88adda79-eb76-43d8-8ee0-673b9390d255)