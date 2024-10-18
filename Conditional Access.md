# Conditional Access (CA)

Conditional Access, or CA for short, is a feature that provides access to resources through policies. In the policy, we define conditions such as group membership, specific locations, and more. After setting the condition, we specify the action that will occur (decision) such as blocking, granting, or limiting access.

## Create CA Policy

This guide is based on Microsoft's explanation. Note that within this explanation, there is a more detailed guide for each individual value.

1. Navigate to the Security category in Entra ID, then select Conditional Access.
2. Click the "Create New Policy" button and fill in the details.

![1](https://github.com/user-attachments/assets/00fdb544-172b-4f70-a73a-f7340187b1a0)

**Assignments:** Applies to:  
- **Users:** Users  
- **Target Resources:** Cloud applications

It consists of include and exclude, which are the users/applications to which this policy will apply/not apply. This explanation is applicable to both Users and Target Resources:

![2](https://github.com/user-attachments/assets/8f27acc6-fb76-44d3-bddf-1293fb33086a)

### Users
- **None:** Does not apply to anyone.  
- **All Users:** All users in this tenant. If this category is used, it is mandatory to set the Global Admin as excluded from this policy; otherwise, there is no way to circumvent it.  
- **Select Users and Groups:** Includes several options:  
  - **All Guest and External Users:** All types of users under the guest value.  
  - **Directory Roles:** Associate the CA with the roles created by Microsoft.  
  - **Users and Groups:** Manual selection of users/groups.  

### Target Resources
The applications to which this policy will apply:  

![3](https://github.com/user-attachments/assets/67dd4a63-8d2d-409c-80f7-b208e2a2ef69)

- **Cloud Apps:** Applications  
- **User Actions:** Monitoring activities such as when a large amount of information is recorded under a user (email, phone number, MFA configuration, etc.) and when we configure certain devices.  
- **Authentication Context:** Limiting access to specific information within an application, for example: a document in SharePoint.

### Conditions
The conditions that will cause this policy to take effect:

![4](https://github.com/user-attachments/assets/e54ef6aa-d133-4915-896a-975f5b6f9ea7)

- **User Risk:** The likelihood that this user is compromised.  
- **Sign-in Risk:** When there is suspicion that the authentication request was not made by the user.  
- **Insider Risk:** Takes data from Purview (which is a data management tool) and assesses if there is suspicious behavior of an employee related to internal organizational data, for example: accessing data at unusual hours or from an unusual location, etc.  
- **Device Platforms:** The condition is based on the operating system type.  
- **Locations:** Based on location.  
- **Client Apps:** The condition is based on the type of application the user is working with.  
- **Filter for Devices:** Filtering based on specific device criteria (manufacturer, device owner, etc.).

### Grant / Block
Blocking/granting access depending on the execution of a certain action:

![5](https://github.com/user-attachments/assets/5ef63e26-6ff4-4864-a9ce-7863858de56c)

- **Require Multifactor Authentication:** Requires MFA.  
- **Require Authentication Strength:** Selecting authentication strengths, which is a combination of several authentication methods.  
- **Require Device to be Marked as Compliant:** Integration with Intune, requiring that to access the resource, the device must be compliant.  
- **Require Microsoft Entra Hybrid Joined Device:** Allows only devices that have completed the hybrid join process, which is a feature connecting devices with Entra ID and the on-prem AD.  
- **Require Approved Client App:** Restriction only to authorized applications in the organization (via Intune).  
- **Require App Protection Policy:** Requires the presence of an Intune protection policy before access is granted.  
- **Require Password Change:** Forces a password change.

### Session
Control actions within the session such as:  
- **Use Application Enforced Restrictions:** Limits access to Microsoft applications.  
- **Use Conditional Access App Control:** Activates the Conditional Access App Control feature in conjunction with Defender for Cloud Apps. It has several options:  
  - **Use Custom Policy:** When wanting to perform monitoring and blocking actions in conjunction with MCAS.  
  - **Monitor Only:** When only wanting to perform monitoring actions with MCAS.  
  - **Block Downloads:** Blocks downloads.  
  - **Sign-in Frequency:** Determines how often the session will be disconnected.  
  - **Persistent Browser Session:** Allows the session to continue even when the browser is closed.  
  - **Customize Continuous Access Evaluation:** Requests authentication details again if something unusual is detected.  
  - **Disable Resilience Default:** Option to implement a disaster recovery script.

**Enable Policy:** Yes, No, or Reporting only without enforcement.
