# SOC Analysis Kit
The SOC Analysis Kit is a comprehensive folder designed to support Security Operations Center (SOC) teams in investigating and analyzing various security events. It contains three sub-folders, each focusing on different critical aspects of cybersecurity:

- Device Analysis: KQL queries for monitoring and investigating device activity, including logon events, software updates, and network interactions.
- Email Analysis: KQL queries for analyzing email traffic, phishing attempts, and suspicious email behavior to detect potential threats.
- IAM Analysis: KQL queries for monitoring identity and access management, tracking user account activity, and identifying abnormal access patterns.

This kit provides SOC analysts with targeted queries to streamline security investigations and improve incident response.

### Examples from existing projects

#### Who Has Local Admin
This query identifies local admin accounts on devices by analyzing logon events from the DeviceLogonEvents table:

![Screenshot](https://github.com/user-attachments/assets/a661bde0-1434-4ad4-a087-fd92d260ee55)

#### Search Process OR SHA256 In Organization
This query searches for specific processes or their associated SHA256 hash values within the organization by analyzing events recorded in the DeviceProcessEvents table:

![Screenshot](https://github.com/user-attachments/assets/f866d1ff-c7ec-4a09-bb66-39ea8d6ee4cc)

#### Search Malicious Attachment
This query searches for potentially malicious email attachments by analyzing records in the EmailAttachmentInfo table:

![image](https://github.com/user-attachments/assets/88adda79-eb76-43d8-8ee0-673b9390d255)