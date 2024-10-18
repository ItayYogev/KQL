# Detection Rules
The Detection Rules folder is a comprehensive collection of KQL (Kusto Query Language) queries designed to enhance an organization's cybersecurity posture by providing proactive monitoring and threat detection capabilities. Each query within this folder addresses specific risk areas and helps identify potentially malicious or unauthorized activities in various cloud and network environments.

These detection rules focus on key areas of concern such as unauthorized access, privileged account misuse, and policy violations. By implementing these queries, security teams can maintain heightened visibility into their operational environments, allowing them to detect anomalies and respond effectively to potential threats before they escalate into serious incidents.

### How To Create Detection Rule: 
1. Paste the query in the "Advanced hunting" category and insert the relevant details into the query
2. Click on the "Create Detection Rule" button on the right side of the screen.
3. Fill in the Alert details
> **Note:** My recommendation is to choose the frequency of "Continuous (NRT)." This near real-time option allows an alert to pop up right after the data is ingested into the XDR. Sometimes it may not be possible to choose this option if the queries are structured in a way that requires waiting for additional data.
4. Choose the impacted entities.

