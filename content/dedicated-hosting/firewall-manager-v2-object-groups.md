---
permalink: firewall-manager-v2-object-groups/
audit_date:
title: Firewall Manager v2 - Object-groups
type: product
created_date: '2017-03-21'
created_by: Trevor Becker
last_modified_date: '2017-03-21'
last_modified_by: Trevor Becker
product: Dedicated Hosting
product_url: dedicated-hosting
---

<!-- IMAGE "Logo" -->
The Firewall Manager v2 Beta is a new tool within the MyRackspace portal. This article describes the object-group feature within this tool. 

Click here to learn more about the [Firewall Manager v2 Beta](https://support.rackspace.com/how-to/firewall-manager-v2-beta).

### What is an Object-group?

Object-groups are used to group like items together, such as IP addresses, ports, or protocols. Object-groups are commonly used to make the configuration of a firewall's access-list more easily readable and controlled, which assists in support and troubleshooting. The benefit to using an object-group is that you can reference an object-group in an access-list entry, instead of having to create individual access-list entries for each component of the object-group. An example of this is if there are 100 IP hosts in an object-group. You could create one access-list entry performing a required action and reference this object-group, or you could create one hundred access-list entries, individually specifying each unique IP host. 

### Why should I use an Object-group?

With the example above, you can easily see the organizational and readability impact object-groups can have on a Cisco firewall's configuration. Remember, the easier a firewall's configuration is to read and modify, the chances for a misconfiguration are reduced, and the quicker it can be troubleshot when issues arise.

### Object-groups in the Firewall Manager v2

In the Firewall Manager v2, object-groups are referred to as **IP Groups**. You also now have the ability to view, modify, or delete any object-group on your firewall. In the previous version of the Firewall Manager, the user was restricted to only modifying object-groups that began with the string "FWCP-". In this new version of the Firewall Manager, this restriction has been lifted, which enables you to more powerfully control and modify your environment.

**Location of Object-groups**

1. Log in to the Firewall Manager v2 using the steps in the [Firewall Manager v2](https://support.rackspace.com/how-to/firewall-manager-v2-beta) "How do I find the Firewall Manager v2 Beta?" section.

2. Select the correct firewall from the list on the left by clicking on it.

    If this is the first time you have attempted to modify this firewall, you will need to accept the Firewall User Agreement.

3. Click the **IP Groups** tab on the left drop down menu

<!-- Image IP Groups --->
