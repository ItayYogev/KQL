# Conditional Access App Control

A feature that monitors and blocks user activities within cloud applications in real time. The system allows for the management of access policies based on certain conditions, such as device type, location, and user, to protect sensitive data and prevent information leaks. With Conditional Access App Control, organizations can block access to applications or restrict certain actions, such as downloading sensitive files, if the user is on an unmanaged device or in a risky location.

## How It Works
There are reverse proxy endpoints that track requests made to cloud applications connected to it. These reverse proxy endpoints are appended to the end of the domains of those applications.

![1](https://github.com/user-attachments/assets/012d0618-b07a-482a-bc90-e5bcbf583de3)

## Conditional Access App Control Tutorial

### Step 1
We need to create a Conditional Access policy in Entra ID.  
In this guide, I won't go through the entire process of creating a Conditional Access policy (I have a dedicated guide for that). 

For Conditional Access App Control to work, when creating the policy, make sure that the "Use Conditional Access App Control" button is checked in the session category. This button activates the transmission of information to the reverse proxy endpoints mentioned earlier.

![2](https://github.com/user-attachments/assets/723dd908-0899-4bae-a167-0d140a72bc8a)

### Step 2
Log out and log back into the application for which we are defining monitoring.

### Step 3
Check that the application appears in the list of Conditional Access App Control apps. You can find it in:  
- Microsoft Defender XDR  
- Settings  
- Cloud Apps  
- Conditional Access App Control apps

![3](https://github.com/user-attachments/assets/6b7d0488-577b-478e-8f0a-3e282475505e)

If the application has SSO with Entra ID, the applications should automatically be added to this category.

### Step 4
Remove the notification stating, "Access to Microsoft OneDrive for Business is monitored."  
It's important to understand that from now on, anyone who logs into this application will see a notification that looks like this:

![4](https://github.com/user-attachments/assets/55627a32-5127-4e52-9774-e925fafe4181)

To remove this notification, go to:  
- Microsoft Defender XDR  
- Settings  
- Cloud Apps  
- User Monitoring  

And uncheck the option, "Notify users that their activity is being monitored."

![5](https://github.com/user-attachments/assets/3d67bc11-41f3-4ab9-abd6-dead99d9c0bb)

### Step 5
Define a policy for what we want to monitor in:  
- Microsoft Defender for Cloud Apps  
- Policies  
- Policy Management  
- Click the "Create Policy" button. In this case, we need to create a session policy since we want to monitor activities during the session.

You can use the policy templates provided by Microsoft:

![6](https://github.com/user-attachments/assets/c1fdc577-dc37-403a-931c-1c5a73fb891a)

And that’s it. From now on, anyone specified in the policy who logs into the application will be monitored, and they will be prevented from performing the actions defined in the policy.
