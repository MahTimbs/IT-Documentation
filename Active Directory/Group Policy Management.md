## Group Policy
Group Policy Objects are a collection of settings used to manage and configure users and computers in Active Directory. It enables admininstrators to configure and manage the settings of multiple computers without having to do so individually. 

---
## How it Works

- **GPO**s contain the rules and settings
- They are linked to AD and then are applied to users and computers
- When a user logs in or if the computer starts, it will scan for the policies and apply them
  
---
## Group Policy Management tool
1. From the **Server Manager** go to **Tools** and click on **Group Policy Management**
2. You can create a GPO by navigating to the desired domain or OU, right clicking on it, and selecting **Create a GPO in this domain**
3. You can also simply right click on the the **Group Policy Objects** container and select **New**

---
## Creating a GPO (e.g. for a Password Policy)
You would do this to enforce strong passwords to help prevent security breaches
1. Name the **GPO**
2. Right click and then click **Edit** to configure settings

---
## Computer configuration vs User configuration
- **Computer Configurations** apply to the computer itself, affecting ALL of the users who log in to it, and are processed DURING startup
- **User Configuration** settings apply to an INDIVIDUAL users profile and follow them across DIFFERENT computers and are processed during user LOGON.

---
## Policies vs Preferences
- **Policies** cannot be change by users they are set in stone.
- **Preferences** can be changed by users

---
## Configuring Password Policies
1. Go to **Computer Configuration** > **Windows Settings** > **Security Settings**
2. Cick on **Account Policies** > **Password Policy**
3. Configure:
  - **Minimum password length** - Define the policy and change
  - **Password must meet complexity requirements** - Enable
  - **Maximum password age** - Set to 90 days

---
## Configuring Account Lockout Policies
Prevents bruce force attacks
1. Click on **Account Policies** > **Account Lockout Policy**
2. Define:
   - **Account lockout duration** - Define this policy setting > Change > Apply > Ok

---
## Other Group Policy Examples (Drive Mapping & Desktop Wallpaper)
### Drive Mapping
- You map drives for users to they have access to them when they log in. This can be done with a GPO
1. Create the GPO from the domain or create a new GPO object (you will have to link to an OU)
2. Name it **Drive Mapping**
3. Right click on this new GPO and click **Edit**
4. Navigate to:
   - **User Configuration** > **Preferences** > **Drive Maps**
   - Right click and choose **New** > **Mapped Drive**
5. Configuration:
   - **Location**: (e.g., \\STLab\ShareFolder)
   - **Use**: Set to available (which ever drive letter you want)

---
### Desktop Wallpaper Policy
- This will set a default wallpaper for users
1. Create the GPO from the domain or create a new GPO object (you will have to link it to an OU)
   - Name it **Desktop Wallpaper**
2. Right click the GPO and select **Edit**
3. Go to **User Configuration** > **Policies** > **Administrative Templates** > **Desktop** > **Desktop**
   - double click on **Desktop Wallpaper**
4. Configure the policy:
   - Set to **Enabled**
   - **Wallpaper Name**: Provide full path to the wallpaper
   - **Wallpaper Style**: Choose **Center** or **Fill**

---
## More Group Policy examples (Control Panel & USB Storage Restrictions)
### Restricting access to the Control Panel
Prevents users from accessing the control panel
1. Create the GPO from the domain or create a new GPO object (you will have to link it to an OU)
   - Name it **Restrict Control Panel**
2. Right click on the GPO and click **Edit**
3. Go to **User Configuration** > **Policies** > **Administrative Templates** > **Control Panel**
4. Double click on:
   - **Prohibit access to Control Panel and PC Settings**
5. Set it to **Enabled**

---
### Disable USB Storage
Prevents users from using USB storage devices
1. Create the GPO from the domain or create a new GPO object (you will have to link it to an OU)
   - Name it **Disable USB Devices**
2. Right click on the GPO and click **Edit**
3. Go to **Computer Configuration** > **Policies** > **Administrative Templates** > **System** > **Removable Storage Access**
4. Double click on:
   - **All Removable Storage classes: Deny all access**
5. Set it to **Enabled**

---
## Group policy CMD commands
- gpresult /f > C:/results.txt
This creates a file containing the group policy of the computer

- gpupdate /help
Shows you everything you need to know about the gpupdate command

- gpresult /r
Shows applied policies for the user and Computer

- gpresult /h
Saves a detaieled report in HTML format

- gpupdate /force
forces group policies to apply on a device or set computers on the same network

---

