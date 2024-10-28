# 🔍 Detection Rules

The **Detection Rules** folder is an essential collection of **KQL (Kusto Query Language) queries** aimed at strengthening an organization’s cybersecurity posture by enabling proactive monitoring and threat detection. Each query in this folder is designed to address specific risk areas, helping identify potentially malicious or unauthorized activities across various cloud and network environments.

These detection rules target critical security concerns, such as unauthorized access, privileged account misuse, and policy violations. Implementing these queries allows security teams to maintain robust visibility over their operational environments, enabling swift anomaly detection and effective response to emerging threats.

---

## 🛠️ How to Create a Detection Rule

1. **Navigate to Advanced Hunting**  
   In the **Microsoft Defender** portal, go to:  
   **Investigation & Response > Hunting > Advanced Hunting**  
   ![Advanced Hunting](https://github.com/user-attachments/assets/bba81448-0446-45ae-ba63-7efed98d646d)

2. **Paste the Query**  
   Insert your query in the **Advanced Hunting** search bar and adjust any relevant details.

3. **Create Detection Rule**  
   Click the **Create Detection Rule** button on the right side.  
   ![Create Detection Rule](https://github.com/user-attachments/assets/947bbc7b-5169-42ec-b662-0cc7396adf75)

4. **Set Alert Details**  
   Customize your alert details, including naming and alert priority.  
   ![Alert Details](https://github.com/user-attachments/assets/18d1ca0b-5110-4829-80ad-a8fbe3f10773)  
   > **Tip:** Select the **Continuous (NRT)** frequency for near real-time alerts, which ensures notifications appear immediately after data ingestion. Note that certain query structures may not support this option and may require additional data waiting time.

5. **Define Impacted Entities**  
   Specify the entities impacted by this detection rule.  
   ![Impacted Entities](https://github.com/user-attachments/assets/57a873ff-cbd0-444e-aa0f-570e1131dcb3)

6. **Set Alert Scope**  
   Choose the alert scope according to your monitoring needs.  
   ![Scope](https://github.com/user-attachments/assets/27f0309e-c438-48dc-a0a3-9b57676469ac)

7. **Submit**  
   Click **Submit** to activate your detection rule.

---

## 🚀 Benefits of Detection Rules
- **Enhanced Visibility**: Continuous monitoring across multiple security domains.
- **Proactive Defense**: Early detection of anomalies and potential threats.
- **Customizable Alerts**: Tailor alerts to meet specific organizational needs.

Implementing these detection rules allows your team to stay ahead of threats, respond quickly, and safeguard your organization's environment more effectively.
