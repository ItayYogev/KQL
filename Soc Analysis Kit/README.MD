# 🛠️ SOC Analysis Kit

The **SOC Analysis Kit** is a robust resource designed to aid **Security Operations Center (SOC)** teams in investigating and analyzing diverse security events. This kit is structured into three essential sub-folders, each dedicated to a critical area of cybersecurity:

- **Device Analysis**: KQL queries for tracking device activity, including logon events, software updates, and network interactions.
- **Email Analysis**: KQL queries for assessing email traffic, detecting phishing attempts, and analyzing suspicious email behaviors.
- **IAM Analysis**: KQL queries focused on monitoring identity and access management, tracking user account activities, and detecting abnormal access patterns.

This collection empowers SOC analysts with targeted tools to streamline investigations and enhance incident response capabilities.

---

## 🎯 Highlights from Existing Projects

### 🔍 Who Has Local Admin
Identifies local admin accounts on devices by analyzing logon events from the **DeviceLogonEvents** table.

![Local Admin Screenshot](https://github.com/user-attachments/assets/a661bde0-1434-4ad4-a087-fd92d260ee55)

---

### 🔍 Search Process or SHA256 in Organization
Searches for specific processes or their associated **SHA256** hash values within the organization, leveraging the **DeviceProcessEvents** table.

![Process Search Screenshot](https://github.com/user-attachments/assets/f866d1ff-c7ec-4a09-bb66-39ea8d6ee4cc)

---

### 🔍 Search Malicious Attachment
Analyzes email records in the **EmailAttachmentInfo** table to identify potentially malicious email attachments.

![Malicious Attachment Screenshot](https://github.com/user-attachments/assets/88adda79-eb76-43d8-8ee0-673b9390d255)

---


