# DNS
DNS (Domain Name System) is a protocol that translates human-readable domain names (E.g. google.com) into IP addresses (E.g. 142.250.190.78), allowing computers to locate and communicate with each other over the Internet or a private network.

## DNS Server
A DNS Server is a computer or network device that stores and manages domain name records and responds to DNS queries by resolving domain names into IP addresses.

## Installing DNS Server
1. Go to **Server Manager**  
2. On the top, click on **Manage** → **Add Roles & Features**  
3. Click **Next** before you begin  
4. **Role-based or feature-based installation** → **Next**  
5. **Server Selection** → **Next**  
6. **Server Roles** (click on **DNS Server**) → Add role and click **Next**  
7. Click **Next** and **Install**

## Navigating to DNS Zones
1. Navigate to **Tools** on the Server Manager and click on **DNS**  
2. Under **STLab**, expand →  
   - **Forward Lookup Zones**  
   - **Reverse Lookup Zones**

## Forward Lookup Zones (FLZ)

- A **DNS Zone** that translates a **domain name** (e.g., `SamuelITLab.com`) into an **IP address**  
- It allows users to access websites and network resources using domain names instead of IP addresses

## Reverse Lookup Zones (RLZ)

- Performs the **opposite function** of FLZ  
- Translates an **IP address**  back into a **domain name** 
- It is used for **security**, **logging**, and **troubleshooting**

## Forward Lookup Zone

1. Right-click on **Forward Lookup Zones** → **New Zone** → **Next**
2. **Zone Type** → Select **Primary Zone**, uncheck **Store the zone in Active Directory** → **Next**
3. **Zone Name**: `SamuelT.com` → **Zone File** (leave as default) → **Next**
4. **Dynamic Update**: Select **Do not allow** → **Finish**

## Reverse Lookup Zone

1. Right-click on **Reverse Lookup Zones** → **New Zone** → **Next**
2. **Zone Wizard** → Select **Primary Zone** → **Next**
3. Skip **Active Directory Zone Replication** → **Next**
4. Choose **IPv4 Reverse Lookup Zone** → **Next**
5. **Network ID**: `10.0.0` → **Next**
6. Select **Do not allow dynamic updates** → **Next** → **Finish**

## Creating a New Host (Forward Lookup Zone)

1. Right-click on the zone (`SamuelT.com`) → **New Host (A or AAAA)**  
2. Enter **Name**: `Test`  
3. Enter **IP Address**: `10.0.0.20` (or any IP address for your organization)

## Creating a PTR Record (Reverse Lookup Zone)

1. Right-click on the reverse zone → **New Pointer**
2. Enter **Host Name** → **Browse**  
3. Navigate: `STLab` → `Forward Lookup` → `Test` (click on it) → **OK**
