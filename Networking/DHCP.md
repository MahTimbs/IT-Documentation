# DHCP
DHCP or Dynamic Host Configuration Protocol is the protocol that automatically assigns IP addresses and other network settings (the subnet mask, default gateway, and DNS) to devices on a network.

## DHCP Server
A DHCP Server is a device (usually a router or Windows Server) that manages IP address allocation dynamically. Instead of manually assinging static IP addresses to every device, the DHCP server automatically provides them based on predefined rules. 

## Installing DHCP
1. Go to **Server Manager** → **Manage** (click on it) → **Add Roles & Features**  
2. Before you begin → **Next** → **Role-based or Feature-based Installation** → **Next**  
3. Select **Destination Server** as default → **Next**  
5. Click on **DHCP Server** (Add Features) → **Next** → **Confirmation**  
6. Click **Install**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP1.png?raw=true" height="800" width="600" />

7. Go to **Flag icon** → **Post-deployment Configuration** → **Complete DHCP Configuration**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP2.png?raw=true" height="800" width="600" />

## Using DHCP
- Go to **Tools** and click on **DHCP**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP3.png?raw=true" height="800" width="600" />


## Configuring DHCP
Creating a scope:
1. Right click on **IPv4** and click on **New Scope**
2. enter the desired IP address range and subnetmask length.
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP4.png?raw=true" height="800" width="600" />


## Adding Exclusions
1. You can either exclude a range of address or a singular address (you do this by simply adding the desired adress in the **Start IP adress** box)
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP5.png?raw=true" height="800" width="600" />


## Lease Durations
- Specifies how long a client can use an IP adress from this scope you can set the days, hours, or minutes.
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP6.png?raw=true" height="800" width="600" />


## Activating the Scope (if you decided not to do so at the end of the configuration)
1. Simply right click on the **Scope** and click **Activate**
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP7.png?raw=true" height="800" width="600" />


## Reserving a printer (or any other network device)
1. Simply right click on **Reservations** and click on **New Reservation**
2. Add the desired name, ip address, MAC address, and description
3. you can choose between DHCP and BOOTP for the supported types
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP8.png?raw=true" height="800" width="600" />


## Enabling DHCP on a Windows machine
- Search → Control Panel → Network and Internet  
- View network status and tasks → Change adapter settings  
- Ethernet → Status → Details → DHCP Enabled  
- No → Click on Properties  
- Click on Internet Protocol Version 4 (TCP/IPv4)  
  → You can see it’s using a static IP address  
  → Change it to *Obtain an IP address automatically*  then
  → OK
<img src="https://github.com/MahTimbs/IT-Documentation/blob/main/Networking/images/DHCP9.png?raw=true" height="800" width="600" />

