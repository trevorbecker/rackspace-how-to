---
permalink: remove-vpn-user-myrackspace-portal/
audit_date:
title: Remove a VPN user in the MyRackspace Portal
type: article
created_date: '2017-10-16'
created_by: Trevor Becker
last_modified_date: '2017-10-16'
last_modified_by: Trevor Becker
product: Dedicated Hosting
product_url: dedicated-hosting
---

Removing a client VPN user is now an automated task within the MyRackspace portal. This article describes how to remove a VPN user by using a ticket template.

### Overview

The **Delete contact** ticket template can be used to not only remove a user from the MyRackspace Portal account contacts list and phone support, but to now also automatically delete the client VPN user from all of your Rackspace dedicated firewalls. 

### Remove VPN User Location

1. Log in to the [MyRackspace customer portal](https://my.rackspace.com/portal/auth/login).

   You will need your Rackspace account number, as well as your username and password.

2. In the top navigation bar, click on the **Tickets** tab, and select **Create Ticket**.

3. On the **Create New Ticket** page, click the **Subject** text field, and in the drop down menu, select **Delete Contact**.

4. Complete the following fields:

    4a. Select the contact name in the drop-down field
    
    4b. Select the **MyRackspace Portal + Phone Support + Systems & Devices** option
    
    4c. Fill in the name of the VPN user to be deleted (Note: You can obtain a list of currently configured client VPN users by [downloading your firewall's configuration](https://community.rackspace.com/products/f/43/t/5892).)

5. Click Create Ticket
