# Device Enrollment for Windows Machines

## Microsoft Intune and Admin Center

**Microsoft Intune** is a cloud-based service that focuses on **mobile device management (MDM)** and **mobile application management (MAM)**. It helps organizations control how devices such as **Windows PCs, Macs, iOS, and Android** access corporate data.

**Microsoft Intune Admin Center** is the web-based management interface for Intune, allowing IT administrators to manage devices, configure policies, deploy apps, and ensure compliance.

---
## Devices
- shows everything from all devices, monitor, device onboarding, manage, devices. It shows the **overview** of device info in Intune.
-  .
## Enrollment for Windows Machines
1. Navigation: **Devices > Enrollment > Windows autopilot > click on Deployment Profiles**
2. Click on **Create Profile** and select Windows PC
3. From there fill out all of the required prompts
- .
## Configuration
- **Configurations** → Create → New policy (**Windows 10 and later**) →
    
- **Profile type (Templates name: Device Restrictions)** →
    
- **Select the Restrictions you want the devices to have and go through the prompts** 
- .
## Compliance
- Compliance refers to the process of ensuring that devices should meet specific security and configuration requirements before they can access corporate resources.
1. **Manage Devices > Compliance > Create Policy**
Picture
2. Go through and fill out the prompts choosing which compliance settings you wish to implement
3. Picture

## Compliance Policies
- **These define the security requirements that devices must meet.**
    
    - Require **BitLocker encryption**
        
    - Enforce **password complexity**
        
    - Require a **specific OS version (Windows 10/11)**
        
    - Ensure **anti-virus/anti-malware is enabled**
picture

## Windows Updates
**Manage updates > Windows updates > Upate rings**
### Update Rings
(This is to make sure updates are created)
- **Basics:** Update ring settings (Update Windows 10 devices to latest Windows 11 release)
- **Assignments:** Add groups (users)
- **Review & Create**
### Why is this important?
- Helps IT admins control Windows updates across all managed devices.
- Ensures stability by delaying updates to test compatibility before deployment.
- Prevents disruptive updates from installing automatically.
- Allows gradual rollout of new Windows versions to avoid potential issues.

## Device Enrollment
1. Access work or school account and enter the email adress created in M365
2. enter the password and go through MFA (if needed)
3. device will automatically join Intune

