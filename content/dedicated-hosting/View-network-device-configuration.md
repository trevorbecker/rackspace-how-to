---
permalink: view-network-device-configuration/
audit_date: 
title: View Your Network Device Configuration
type: article
created_date: '2017-12-21'
created_by: Trevor Becker
last_modified_date: '2017-01-06'
last_modified_by: Nate Archer
product: Dedicated Hosting
product_url: dedicated-hosting
---

The MyRackspace portal contains a self-service feature that enables you to download a copy of your firewall or load balancer's running configuration. You can use this feature for your documentation and auditing purposes.

To access your Network Device's configuration:

1. Log in to the [MyRackspace customer portal](https://my.rackspace.com/portal/auth/login) using your account number, username, and password.


2. In the top navigation bar click **Products** > **Devices**.

   <IMAGE 1 FROM EMAIL ON 12-21-2017>

3. On the **Devices** pag, click the gear icon next to your chosen network device.  

   If you can not find your network device, use the search box on the top right of the page and enter either "Firewall" or "Load Balancer"

   <IMAGE 2 FROM EMAIL ON 12-21-2017>

4. Click **Download Network Config**.

   The length of the download depends on the size of your network device's configuration. 
   
5. After the configuration is download, you can find the configuration in your browser's download folder as a .txt file. 
   
   **Note:** The network device's configuration contains sections named **<REMOVED>**. These fields have been removed since they contain Rackspace specific infrastructure settings.
   
   
### Viewing Client VPN Users Within Your Firewall's Configuration
   
Client VPN users are stored in the firewall's running configuration:
   
    Syntax:  username <username> password <password>
    Example: username rackspace-test password Abc123
    
If you would like to perform a client VPN user audit of your firewall search through the document for the client VPN syntax listed above in your downloaded **.txt** Network device configuration file.

   
