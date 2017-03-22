---
permalink: firewall-manager-v2-port-groups/
audit_date:
title: Firewall Manager v2 - Port-groups
type: product
created_date: '2017-03-22'
created_by: Trevor Becker
last_modified_date: '2017-03-22'
last_modified_by: Trevor Becker
product: Dedicated Hosting
product_url: dedicated-hosting
---

<!-- IMAGE "FWCPv2 Article 3 Image Logo" -->
The Firewall Manager v2 is a new tool within the MyRackspace portal. This article describes the port-group feature within this tool. 

Click here to learn more about the [Firewall Manager v2](https://support.rackspace.com/how-to/firewall-manager-v2).

### What is a port-group?
Before a port-group can be explained, an object-group must be defined. Object-groups are used to group like items together, such as IP addresses, ports, or protocols. Object-groups are commonly used to make the configuration of a firewall's access-list more easily readable and controlled, which assists in support and troubleshooting. 

As stated above, _a port-group is a form of an object-group_. A port-group is a single configuration item that logically groups ports together. The benefit to using a port-group is that you can reference a port-group in access-list entries that have object-groups as well! This is better than the alternative of having to create individual access-list entries for each component of the port-group. A powerful example of efficient use of port-groups is if you had a single access-list entry references an object-group of 100 source IPs, an object-group of 10 destination IPs, and a port-group of 5 TCP ports. Using the object-group and port-group strategy, your firewall's running configuration only requires one access-list entry. If you did not use object and port-groups, this would require **5,000 access-list entries** in the running configuration, individually specifying each unique source IP, destination IP, and TCP port. 

**Note:** The Firewall Manager v2 only allows you to create port-groups using TCP or UDP ports.

### Why should I use a port-group?

With the example above, you can easily see the organizational and readability impact port-groups can have on a Cisco firewall's running configuration. Remember, the easier a firewall's running configuration is to read and modify, the chances for a misconfiguration are reduced, and the quicker it can be troubleshot when issues arise.

### Port-groups in the Firewall Manager v2

In the Firewall Manager v2, you now have the ability to view, modify, or delete any port-group on your firewall. In the previous version of the Firewall Manager, the user was restricted to only modifying port-groups that began with the string "_FWCP-_". In this new version of the Firewall Manager, this restriction has been lifted, which enables you to more powerfully control and modify your environment.

**Location of Port-groups**

1. Log in to the Firewall Manager v2 using the steps in the [Firewall Manager v2](https://support.rackspace.com/how-to/firewall-manager-v2) "How do I find the Firewall Manager v2?" section.

2. Select the correct firewall from the list on the left by clicking on it.

3. Click the **Port Groups** tab on the left drop down menu.

<!-- Image "FWCPv2 Article 3 Image Port Group" --->

### Viewing Port-groups

Navigate to the **_Port Groups_** tab. Scroll or search through the port-group list and select the appropriate port-group by clicking on it. The contents of the port-group will automatically display in the next column to the right. You may need to scroll to the top depending on the amount of port-groups configured on your firewall.

The Firewall Manager v2 organizes the port-groups that exist on your firewall in case-sensitive, alphabetical order. This means that oport-groups titled in uppercase are displayed before the lowercase port-groups. If you are having a difficult time locating the port-group, perform a find within your browser, and search for the port-group.

The Firewall Manager v2 also now allows you to search through the contents of a port-group. This feature enables you to quickly identify if a TCP or UDP port exists within the specified port-group. To use this feature, type a TCP or UDP port number into the search bar that automatically displays in the right column once you click on the port-group to select it.
