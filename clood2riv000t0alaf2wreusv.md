---
title: "3. VPC - Virtual Private Cloud"
datePublished: Tue Nov 07 2023 13:22:54 GMT+0000 (Coordinated Universal Time)
cuid: clood2riv000t0alaf2wreusv
slug: 3-vpc-virtual-private-cloud
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699362933144/3b728533-e93c-4d5e-8e60-92349a03b7b4.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1699363342345/babc4f1f-ec51-4847-bf29-c170230ebe55.png
tags: aws, vpc, vpc-peering, vpc-basics

---

##  **Private Cloud:-**

* **VPC is a virtual network or Data Center inside AWS for one client.**
    
* **It is logically isolated from other virtual N/W in the AWS cloud.**
    
* **5 VPC in one region and 200 subnets  each vpc**
    
* **Automatically created NACL, DHCP, and security group**
    
* **You can not change its CIDR block range.**
    
* **If you need a different CIDR size create a new VPC**
    

**Logical - you cannot touch**

**Physical - you can touch**

## **Component of VPC**

* **CIDR and IP address Subnets**
    
* **Implied Router and Routing Table         implied router = virtual router -- &gt;&gt; networking device**
    
* **Internet Gateway**
    
* **Security Group**
    
* **Network ACL**
    
* **Virtual Private gateway**
    
* **Peering Connection**
    
* **Elastic IP**
    

---

### **Brief:-**

* **VPC**
    
* **Component of VPC**
    

### **Questions:-**

* **What is VPC?**
    
* **How many VPC can be created in one region?**
    
* **How many subnets can be created in one VPC?**
    
* **When you create VPC what will create automatically?**
    
* **Once create vpc can you change CIDR block range ? Yes/Not**
    
* **What does it mean of Logical and Physical router?**
    
* **What is component of VPC?**
    

## **Private VPC** 

**VPC Type**

1. **Default VPC**
    
2. **Custom VPC**
    

> **Default VPC**

* **Created in each AWS Region when an AWS account is Created.**
    
* **Has Default CIDR, Security Group, NACL and Route table Settings.**
    
* **Internet Gateways by Default.**
    

> **Custom VPC**

* **Is a VPC on the AWS  account owner creates**
    
* **AWS users can decide on the CIDR**
    
* **Create Internet Gateways**
    

## **Step of creating of Vpc**

1. **Create VPC**
    
2. **Subnet**
    
3. **Internet Gateways**
    
4. **Route Table**
    

**Elastic Ip = Static IP**

**Public Subnet - which can go to the internet that is called to the public subnet / which are connect to the internet gateway**

**Private Subnet - this can not go to the internet is called a private subnet/ ----&gt; which are not connect to internet gateway**

**Take CIDR ---&gt; 16 to 24**

## Reserved IP Address

**Ex- 10.0.0.0/24 Reserved  Address**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>10.0.0.0</strong></p></td><td colspan="1" rowspan="1"><p><strong>Network Address</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>10.0.0.1</strong></p></td><td colspan="1" rowspan="1"><p><strong>Reserved by AWS for VPC Route</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>10.0.0.2</strong></p></td><td colspan="1" rowspan="1"><p><strong>Reserved for DNS</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>10.0.0.3</strong></p></td><td colspan="1" rowspan="1"><p><strong>Reserved for Future purpose</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>10.0.0.255</strong></p></td><td colspan="1" rowspan="1"><p><strong>Broadcast address</strong></p></td></tr></tbody></table>

> **Note:- AWS do not support Broadcast in a VPC But Reserved this address**

---

### **Brief:-**

* **VPC TYPE**
    
* **Steps Creating VPC**
    
* **Reserved IP Address**
    

### **Questions:-**

* **How many types of VPC?**
    
* **What is Default VPC?**
    
* **What is Custom VPC?**
    
* **Igw is not connected with custom VPC? --&gt; yes/NO**
    
* **What is Steps of Creating VPC?**
    
* **What is Elastic IP?**
    
* **What is Public Subnet?**
    
* **What is Private Subnet?**
    
* **How many ip are reserved by AWS?**
    

---

## **Implied Router and Route Table and Internet Gateway**

> **Implied Router = Logical Router**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699363119781/4ad82d47-57c6-4ea8-8909-103fe3b56542.png align="center")

> **Implied Router and Router Table**

* **It is the central routing function**
    
* **200 route table in per VPC**
    
* **You cannot delete main route table**
    
* **50 route entry per route table**
    
* **Each subnet must be associated with only one route table at any given time**
    

> **Internet Gateway**

* **An internet gateway is a virtual router that connects a VPC to the internet.**
    
* **Default VPC is already attached with on Internet Gateway**
    
* **If you create a new vpc then you must attach the internet gateway in order to access the internet**
    
* **Ensure that your subnet route table points to the internet gateway**
    
* **It supports IPv4 and IPv6**
    

---

### **Brief:-**

* **Implied Router**
    
* **Route Table**
    
* **Internet gateway**
    

### **Questions:-**

* **What is implied Router?**
    
* **What is route table?**
    
* **How many route table can be create in one VPC?**
    
* **Can you delete main route table?**
    
* **How many entry can you do in per route table?**
    
* **What is internet gateway?**
    
* **Is it supports IPv4 and IPv6?**
    

---

## **NAT (Network Address Transmission) Gateway** 

**NAT Gateways- Private subnet  to Public subnet (internet)**

**You charged for creating and using  a NAT Gateways**

### **Security Group**

**It is virtual firewall  works at ENI level**

**Up to 5 security group each instance**

**Can only have permit rules cannot  have deny rule**

**Statefull - ---------&gt; inbound , agar inbound rule laga hai to by default outbound rule allowd hoga**

**&lt;---------- outbound**

**Stateless ----------&gt;**

**Inbound &lt;-----------**

**Outbound --------&gt;**

### **Network ACL- all traffic (inbound , outbound ) are allowed, this working as firewall**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Security Group</strong></p></td><td colspan="1" rowspan="1"><p><strong>NACL</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Operate at instance&nbsp; level</strong></p></td><td colspan="1" rowspan="1"><p><strong>Operate at the subnet level</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Support allows rules only</strong></p></td><td colspan="1" rowspan="1"><p><strong>Permits allow as well as deny rules</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Stateful , return traffic is automatically allowed</strong></p></td><td colspan="1" rowspan="1"><p><strong>Stateless /allowed&nbsp; by rules</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Applies to an instance only</strong></p></td><td colspan="1" rowspan="1"><p><strong>Applies to all instances in the subnet</strong></p></td></tr></tbody></table>

---

## **VPC Peering**

**You can peer to Mumbai vpc to London vpc by VPC peering** 

**Using private ipv4 address**

**Own vpc and your other aws account you can vpc peering**

**Transitive Peering**

**VPC -A   --------------&gt;  VPC -B ------------&gt; VPC -C --------X-------VPC - A**

 **VPC DEMO**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>VPC Peering</strong></p></td><td colspan="1" rowspan="1"><p><strong>Two different vpc communicate with vpc peering</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p><strong>Cross-region peering</strong></p></td></tr></tbody></table>

**NACL= go with comparision** 

**VPC Endpoint**

**\===========**

* **Public instance se private instance ko access karenge and enpoint ke through aws ko access kar skte hain**
    

* **Aws ko privately access karna , access without internet**
    
* **Nat gateway ke through jitna data send karoge wo utna pasoa lega to ye mahga tha**
    
* **Isiliye vpc endpoint ka use karna sahi hoga**
    
* **This is virtual device**
    
* **Endpoint is specific**
    

**Command**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Aws configure</strong></p></td><td colspan="1" rowspan="1"><p><strong>It takes secret id of your aws account</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Aws s3 mb s3://bhupi</strong></p></td><td colspan="1" rowspan="1"><p><strong>Make bucket</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Aws s3 ls s3://bhupi</strong></p></td><td colspan="1" rowspan="1"><p><strong>List bucket</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Aws s3 rb s3://bhupi</strong></p></td><td colspan="1" rowspan="1"><p><strong>Remove bucket</strong></p></td></tr></tbody></table>

**VPN Connection**

* **Create vpc**
    
* **Create vpn**
    
* **Create EC2**
    
* **Establish VPN**
    
* **Connect to EC2 to VPN**
    

### **Question:-**

* **What is private cloud ?**
    
* **How many vpc can create in one region ?**
    
* **How many subnet can create in one region ?**
    
* **How many component of VPC ?**
    
* **How many type of VPC ?**
    
* **What Steps of Creating VPC ?**
    
* **What is Elastic IP ?**
    
* **What is public and private subnet ?**
    
* **What is internet Gateways ?**
    
* **What is NAT Gateway ?**
    
* **What is different between Security Group and NACL ?**
    
* **What is VPC Peering ?**
    
* **What is Transitive Peering ?**
    
* **What is VPC Endpoint ?**
    
* **What is VPN Connection ?**