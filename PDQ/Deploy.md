# PDQ Deploy

## What is PDQ Deploy?

PDQ Deploy is a remote software deployment tool for Windows environments. It allows you to push software, scripts, patches, and updates to multiple machines simultaneously or on a schedule.

You can see it as your "remote software installer."  
Instead of going from PC to PC, you send out one command and PDQ takes care of the rest.
As a  Helpdesk I might approval from management to install software application to client machine silently without interrupting their work.

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
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ1.png?raw=true" height="800" width="600" />

### Package Library
- This is where all the apps are located
---
## Deploying Applications on Server 2022

- Go to **Package Library**
- Select the app (in my lab: Zoom)
- Right-click the app → Select **Download Selected**
- As app downloads, it gets added to local library
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ2.png?raw=true" height="800" width="600" />

1. Go to **Package**
2. Select the app package
3. Right-click → Select **Deploy Once**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ3.png?raw=true" height="800" width="600" />

4. On the top right, click on **Targets**
5. Select **Active Directory** → **Computers**
- As you can see, I have two computers.
- Since I'm deploying Zoom to Windows Server 2022:
  - Select it
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ4.png?raw=true" height="800" width="600" />

  - Click on the single arrow →
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ5.png?raw=true" height="800" width="600" />

  - Click on **OK**
  - Then **Deploy Now**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ6.png?raw=true" height="800" width="600" />

<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ7.png?raw=true" height="800" width="600" />

> Now it's completed and fully deployed to my Server 2022.
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ6.png?raw=true" height="800" width="600" />

## Deploying 7-Zip with PDQ Deploy on Windows Server 2022

### Deployment Procedure

- Same procedure as deploying Zoom.
- Right-click on the package → **Deploy Once**
- Select **Target** → **Active Directory** → **Containers or Computers**
- Select the computer
- Use the single arrow → **Server2022**
- Click **OK**
- Click **Deploy Now**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ9.png?raw=true" height="800" width="600" />

- Deployment finished
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/PDQ/images/PDQ10.png?raw=true" height="800" width="600" />

---
> **Note:**  
> This process allows IT administrators or helpdesk to deploy applications on the back-end without interrupting the users.
sfully
- On the lab/test machine, you can see the two apps installed silently on it
- This is how applications are installed on a client machine silently without disturbing them
