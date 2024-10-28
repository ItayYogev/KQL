# Detection Rules 
The Detection Rules folder is a comprehensive collection of KQL (Kusto Query Language) queries designed to enhance an organization's cybersecurity posture by providing proactive monitoring and threat detection capabilities. Each query within this folder addresses specific risk areas and helps identify potentially malicious or unauthorized activities in various cloud and network environments.

These detection rules focus on key areas of concern such as unauthorized access, privileged account misuse, and policy violations. By implementing these queries, security teams can maintain heightened visibility into their operational environments, allowing them to detect anomalies and respond effectively to potential threats before they escalate into serious incidents.

### How To Create Detection Rule: 
1. In the microsoft defender portal, click on: invrstigation & response > hunting > advanced hunting:
<img width="182" alt="advanced hunting" src="https://github.com/user-attachments/assets/bba81448-0446-45ae-ba63-7efed98d646d">
2. Paste the query in the "Advanced hunting" category and insert the relevant details into the query
3. Click on the "Create Detection Rule" button on the right side of the screen:
<img width="929" alt="create Detection rule" src="https://github.com/user-attachments/assets/947bbc7b-5169-42ec-b662-0cc7396adf75">
4. Fill in the Alert details as you want:
<img width="222" alt="alert details" src="https://github.com/user-attachments/assets/18d1ca0b-5110-4829-80ad-a8fbe3f10773">
> **Note:** My recommendation is to choose the frequency of "Continuous (NRT)." This near real-time option allows an alert to pop up right after the data is ingested into the XDR. Sometimes it may not be possible to choose this option if the queries are structured in a way that requires waiting for additional data.
5. Choose the impacted entities:
<img width="503" alt="Impacted entities" src="https://github.com/user-attachments/assets/57a873ff-cbd0-444e-aa0f-570e1131dcb3">
6. choose the scope that you want that the alert will be:
<img width="145" alt="scope" src="https://github.com/user-attachments/assets/27f0309e-c438-48dc-a0a3-9b57676469ac">
7. click submit