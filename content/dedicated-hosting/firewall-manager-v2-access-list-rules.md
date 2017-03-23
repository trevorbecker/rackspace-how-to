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

### Access-list best practices and recommendations

The security of your Rackspace environment begins at your Cisco firewall. Because of this, misconfigurations in network access policies on your firewall can lead to unwanted network exposure and potential compromise. The integrity and network security of your environment is highly important to Rackspace. 

The following points are some best practices and recommendations you should always follow in order to remain secure and not break any compliances you may need to follow. 

- Always minimize the size of the source and destination traffic in your access-list entry when possible. Be as specific as possible. Do not define the destination as any (your entire Rackspace environment) when only one destination server needs to be accessed.

- Do not allow traffic from any source to any destination of the IP, TCP, or UDP protocols. (permit ip any any, permit tcp any any, or permit udp any any) This will effective turn your security platform into a switch, as it will not block any packets to your entire environment over those protocols.

- Do not allow all traffic to a destination or group of destinations. (permit ip any [host], or permit ip any [object-group])

- Do not globally open up ports (defining source of any over a port) that are not considered a generally accepted best practice. Examples of these ports are, but not limited to, 22 - SSH, 1433 - Microsoft SQL, 3306 MySQL, and 3389 - RDP.

### Access-list line numbers
execution order, line numbers
Always be aware of what lies above your access control entry you just added. If you place an entry below a deny that encompasses your target traffic, understand that your new access control entry will never be hit. In situation like this, the use of the line number is required.

### Access-list Rules

Each environment at Rackspace is unique in its own way. However, there are standards we have implemented in each firewall environment to make some aspects of the access-list configuration uniform.

- **101 ACL**: The 101 access-list is the ACL that is applied to the outside interface for traffic ingressing (coming toward) from the internet. The 101 access-list defines what traffic from the internet is allowed to enter into the environment. The 101 access-list is your Rackspace environment's first line of defense. If traffic is not explicitly permitted on it, traffic is implicitly denied by default.

  **Warning:** The 101 access-list is the gatekeeper for network security to your environment. Do not open more access than is required. 
 
