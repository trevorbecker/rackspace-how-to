---
permalink: firewall-manager-v2-access-list-rules./
audit_date:
title: Firewall Manager v2 - Access-list rules
type: product
created_date: '2017-03-23'
created_by: Trevor Becker
last_modified_date: '2017-03-23'
last_modified_by: Trevor Becker
product: Dedicated Hosting
product_url: dedicated-hosting
---

<!-- IMAGE "FWCPv2 Article 5 Image Logo" -->
Firewall Manager v2 is a new tool within the MyRackspace portal. This article describes the Access Control List (ACL) rule feature within this tool. 

To learn more about the tool, see [Firewall Manager v2](https://support.rackspace.com/how-to/firewall-manager-v2).

### What is an Access Control List?

Access control lists, or ACLs, give Cisco firewalls basic traffic filtering capabilities. Access-lists have the potential to be configured to filter traffic for all routed protocols as the packets pass through the firewall. One of the key functions to access-lists is to provide security for a network. If access-lists are not used, the Cisco firewall's default security policy of security-levels is active, which does not provide the highest level of network security. Access-lists are the tool that provide environments with Network Access Control, or NAC. They do this by filtering network traffic and controlling if packets are forwarded or blocked at the firewall's interfaces. As an aspect of the deep packet inspection process, Cisco firewalls perform this access control lookup for each packet attempting to traverse one of its interfaces. The primary function of access-lists is to control the traffic that attempts to enter the internal networks from an external, unsecured network. 

### What is an Access Control Entry?

An Access Control Entry (ACE) is an individual entry in an Access Control List (ACL). Access Control Entries are referred to as **Rules** in the Firewall Manager v2. The Cisco firewall only allow you to configure one access-list, per interface, per direction. This access-list can be composed of as many ACEs that you need. The Firewall Manager v2 enables you

### Location of access-list rules

1. Access Firewall Manager v2 by following the steps in the [Firewall Manager v2](https://support.rackspace.com/how-to/firewall-manager-v2) article.

2. In the navigation pane on the left side of the panel, click the firewall for which you want to see the access-lists rules.

3. Click **Rules**

  **Example 1.1:** Example location of the access-list rules in Firewall Manager v2
  <!-- Image "FWCPv2 Article 5 Image Rules" --->

### Access-list Rules

Each environment at Rackspace is unique in its own way. However, there are standards we have implemented in each firewall environment to make some aspects of the access-list configuration uniform.

- **101 ACL**: The 101 access-list is the ACL that is applied to the outside interface for traffic ingressing (coming toward) from the internet. The 101 access-list defines what traffic from the internet is allowed to enter into the environment. The 101 access-list is your Rackspace environment's first line of defense. If traffic is not explicitly permitted on it, traffic is implicitly denied by default.

  **Warning:** The 101 access-list is the gatekeeper for network security to your environment. Do not open more access than is required. The potential for compromise increases as more access is opened. Think of this access-list as a wall in front of your infrastrcuture, as you poke more holes in it with acces-list entries, the higher the potential is for a breach. 
  
  **Warning:** Never configure source traffic of any to destination traffic of any over the protocol IP. IP is the entire IP suite
