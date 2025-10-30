# File Sharing
## Drive Mapping
A mapped drive is a shortcut that assigns a dive letter (like Z: or G:) to a network folder or location, making it appear as if it's a local drive on your computer
---
## How to Create a Shared Folder
1. Go to **Start menu** → Search for **Server Manager**
2. Navigate to **File and Storage Services**
3. Tap on **Shares** → **New Share**
4. Choose **SMB Share - Quick** → Click on it and click **Next**
5. Select **Share location** → Click **Next**
6. Enter **Share name** (e.g., `HR` or `Sales`) → Click **Next**
7. Configure **Other Settings** → Click **Next**
8. Set **Permissions** → Confirm and click **Create**
---
## How to Access the Shared Folder
1. Go to **File Explorer** → **This PC** → **Local Disk (C:)**
2. **HR** is in the shares folder (This is the shared folder we just created)
---
## Settings Permissions on the Folder
1. On the folder:
   - Right-click → **Properties** → **Security**
   - Tap **Advanced**
   - Click **Disable Inheritance**
   - Choose **Convert inherited permissions into explicit permissions on this object**
   - Remove existing users and add groups.
2. Add permissions:
   - Click **Add** → **Select Principal**
   - Enter the username or group → Click **Check Name** → Click **OK**
   - Set **Basic permissions** (e.g., Modify) and click **OK**
3. In the **Sharing** tab click on **Share**, and grant **Read/Write** permissions as needed
---
## Mapping the Drive on a Users PC
1. **Log into the user computer**
2. Navigate to **File Explorer** → **This PC**
3. Type in the search bar the UNC path:
- Log into the User Computer → Navigated to File Explorer → This PC → If the User has been mapped to a drive before, try to confirm the path `\\Server2022\hr`

- This PC → Right click on it → Select **Map network drive** and select a drive (Z: or any letter based on available drive in the Company) → Folder (Type the path, `\\Server2022\hr` and finish)
- The **Reconnect** automatically maps the drive as the user logins.
---
## Mapping the Drive with Active Directory
1. Find the User in AD
2. Go to Profile > Home Folder > Connect
3. Type in the network path \\Server2022\hr\%username%
4. This maps the drive based on the username
---
## Mapping Drives using Group Policy
1. Create a New Group
Example: Financial Group in Active Directory.
Add users to the group
2. **Navigate to the Server**
   - Go to: `File & Storage Services`.
   - Right-click on `Shares` → `New Share`.
   - Select `SMB Share - Quick`.
   - Share location: `C:\drive` → Click Next.
   - Share name: `FinanceNetworkDrive` → Click Next.
3. **Permissions**
   - Click on `Permissions` → `Customize permissions`.
   - Disable inheritance.
   - Convert inherited permissions into explicit permissions on this object.
   - Click on `Add` → `Select a Principal`.
   - Click `Advanced` → `Find Now` → Select and add `Financial Group`.
   - Click `Apply` and `OK` → Click `Next`.
   - **Drive is Now Created**
---
## Mapping Drive via Group Policy (cont.)

1. Open `Server Manager` → Go to `Tools` → `Group Policy Management`.
2. Navigate:
   - Forest → Domain
1. Right-click on `Finance` → Create a GPO linked to `Finance`.
---
### Domain GPO Configuration

- Right-click on the created GPO → **User Configuration** → **Preferences** → **Windows Settings** → Right-click on **Drive Maps** → **New** → **Mapped Drive**
- Enter the path (directory of the folder) and paste it in the location field.
- Check `Reconnect` box.
- Use the whichever available letter (e.g., F: drive).
---
### Item-Level Targeting
- Go to **Common** tab at the top → Enable **Item-Level Targeting** → Targeting → **Security Groups** → **Advanced**
- Add the **Financial Group** → Apply & OK. 
---
### Testing the GPO
- Login on a Users account
- Open Command Line and type:
gpupdate /force
- Opened **File Explorer**.
- The mapped drive will be there

  

