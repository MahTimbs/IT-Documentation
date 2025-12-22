# PDQ Deploy

## What is PDQ Deploy?

PDQ Deploy is a remote software deployment tool for Windows environments. It allows you to push software, scripts, patches, and updates to multiple machines simultaneously or on a schedule.

You can see it as your "remote software installer."  
Instead of going from PC to PC, you send out one command and PDQ takes care of the rest.
As a  Helpdesk I might approval from management to install software application to client machine silently without interrupting their work.

![Screenshot](images/screenshot412.jpg)

---
## What Does It Do?

- Silently installs applications (e.g. Chrome, Zoom, Adobe Reader)
- Updates software and deploys custom scripts
- Schedules deployments (e.g. install at night)
---

## PDQ Dashboard Overview

- The Dashboard shows:
  - All deployments
  - All apps deployed to endpoints
  - All schedules
  - Retry queue
  - Package Library
![Screenshot](images/screenshot307.jpg)
### Package Library
- This is where all the apps are located
---
## Deploying Applications on Server 2022

- Go to **Package Library**
- Select the app (in my lab: Zoom)
- Right-click the app → Select **Download Selected**
- As app downloads, it gets added to local library
![Screenshot](images/screenshot322.jpg)
1. Go to **Package**
2. Select the app package
3. Right-click → Select **Deploy Once**
![Screenshot](images/screenshot323.jpg)
4. On the top right, click on **Targets**
5. Select **Active Directory** → **Computers**
- As you can see, I have two computers.
- Since I'm deploying Zoom to Windows Server 2022:
  - Select it
![Screenshot](images/screenshot324.jpg)
  - Click on the single arrow →
![Screenshot](images/screenshot325.jpg)
  - Click on **OK**
  - Then **Deploy Now**
![Screenshot](images/screenshot326.jpg)
![Screenshot](images/screenshot327.jpg)

> Now it's completed and fully deployed to my Server 2022.
![Screenshot](images/screenshot328.jpg)
## Deploying 7-Zip with PDQ Deploy on Windows Server 2022

### Deployment Procedure

- Same procedure as deploying Zoom.
- Right-click on the package → **Deploy Once**
- Select **Target** → **Active Directory** → **Containers or Computers**
- Select the computer
- Use the single arrow → **Server2022**
- Click **OK**
- Click **Deploy Now**
![Screenshot](images/screenshot329.jpg)
- Deployment finished
![Screenshot](images/screenshot330.jpg)
---
> **Note:**  
> This process allows IT administrators or helpdesk to deploy applications on the back-end without interrupting the users.
sfully
- On the lab/test machine, you can see the two apps installed silently on it
- This is how applications are installed on a client machine silently without disturbing them
