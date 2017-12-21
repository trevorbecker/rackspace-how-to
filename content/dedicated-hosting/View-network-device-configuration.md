---
permalink: view-network-device-configuration/
audit_date: '2017-12-21'
title: How to View Your Network Device Configuration
type: article
created_date: '2017-12-21'
created_by: Trevor Becker
last_modified_date: '2017-12-21'
last_modified_by: Trevor Becker
product: Dedicated Hosting
product_url: dedicated-hosting
---

The MyRackspace portal contains a self-service feature that enables you to download a copy of your firewall or load balancer's running configuration. This feature is commonly utilized by our customers for documentation and auditing purposes.

### Viewing your Network Device's Configuration

1. Log in to the [MyRackspace customer portal](https://my.rackspace.com/portal/auth/login).

   You will need your Rackspace account number, as well as your username and password.

2. In the top navigation bar, click the **Products** drop down, and then select **Devices**.

   <IMAGE 1 FROM EMAIL ON 12-21-2017>

3. On the **Devices** page, hover over the gear icon to the left of the network device to view action options. 

   If you are having difficulty locating your network device, use the search field on the top right. Search for the term "Firewall" or "Load Balancer".

   <IMAGE 2 FROM EMAIL ON 12-21-2017>

4. Select the **Download Network Config** action option.

   Depending on the size of your network device's configuration, this may take up to a minute. Once complete, the configuration will be located in your browser's download folder as a .txt file. 
   
   Note: The network device's configuration will contain sections referred to as **<REMOVED>**. These fields have been sanitized as they contain Rackspace sensitive infrastructure settings.
   
   
### Viewing Client VPN Users Within Your Firewall's Configuration
   
Client VPN users are store in the firewall's running configuration. The structure of a client vpn user is the following:
   
    Syntax:  username <username> password <password>
    Example: username rackspace-test password Abc123
    
If you would like to perform a client VPN user audit of your firewall, perform the steps in the "Viewing your Network Device's Configuration" section, and search through the document for the client VPN syntax listed above.

   
