---
title: "2. EC2 - Elastic Compute Cloud"
datePublished: Sun Oct 29 2023 11:35:30 GMT+0000 (Coordinated Universal Time)
cuid: clobe9zco000309kz85vsfhkb
slug: 2-ec2-elastic-compute-cloud
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698578003851/a6231ccf-b10b-471e-b094-f3e67c29bdf7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698579286696/8d8011b6-21dc-4793-b7ef-bb03e216f3e7.png
tags: cloud, ec2, aws, scalability, ec2-instance

---

## **Lecture - 4  Elastic Compute Cloud**

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>EC2 - Elastic Compute Cloud</strong></div>
</div>

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>EC2 - This is a Virtual Server/Machine</strong></div>
</div>

* **Scalability**
    
* **Have 2 Storage options EBS and Instance Storage**
    
* **Preconfigured Template**
    
* **20 Instances per region**
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Compute - has the understanding to execute and run applications and software.</strong>&nbsp;</div>
</div>

 

## **Types of EC2 Instances**

1. **General Purpose:- Balanced Memory & CPU**
    
2. **Compute Optimized -: More CPU than RAM**
    
3. **Memory Optimized -: More RAM**
    
4. **High Memory Optimized -: High RAM, Nitro System**
    
5. **Accelerated Computing /GPU-: Graphic Optimized, ex - PUBG**
    
6. **Storage Optimized -: Low latency**
    

---

## **Questions:-**

* **What is the Stand for EC2?**
    
* **what is EC2?**
    
* **What is Scalability?**
    
* **In the EC2 instance have preconfigured templates available?**
    
* **How many instances can you launch in one region?**
    
* **What is Compute?**
    
* **How many Types of Instance?**
    

---

## **Lecture - 5  Type of Instances**

> **Types of Instances:-**

1. General Purpose
    
2. Compute Optimized
    
3. Memory Optimized
    
4. High Memory
    
5. Accelerated Computing
    
6. Storage Optimized
    
7. Previous generation
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>General Purpose Instance</strong></div>
</div>

> **General-purpose instances:- Provide a balance of computing memory and networking resources and can be used for a variety of workloads.**

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">3 Series in General Purpose</div>
</div>

| **A - Series** | **A1 medium** |
| --- | --- |
| **T - Series** | **T2, t2 micro, t3, t3a** |
| **M - Series** | **M4, M5, M5d** |

> **A1- Instances**

* **Web server**
    
* **Containerized microservices**
    
* **Caching  fleets**
    
* **Distributed data stores**
    

> **T2 - Instances**

* **Generally for Development**
    
* **Very Cheap**
    
* **Baseline CPU performance**
    
* **5 to 32 GB**
    

> **M4 instance**

* **Nitro Hypervisor**
    
* **RAM 8 to 64 GB**
    
* **EBS Storage**
    

---

## **Questions:-**

* **What is a General Purpose instance?**
    
* **How many types of series in general purpose?**
    

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Compute Optimized Instances</strong></div>
</div>

**Compute Optimized:- Ek Sath bahut sari process (Batch Process /Parrallel Processing )ko execute karne ke liya ham Cpmpute Optimized Instances ka use karte hain.**

* **High Performance Processor**
    
* **Cost Effective**
    
* **C - Series (c3,c4,c5)**
    
* **Good Speed**
    
* **Only EBS Storage**
    

**User Cases - High Performance, Webserver, Gaming, Video, Encoding**

* **C5 Support max 25 EBS Volumes**
    
* **C5 use Elastic network Adapter**
    
* **C5 uses new EC2 Hypervisor**
    

**ENA - for improving your network is used ENA.**

---

### Questions:-

* **What is compute optimized?**
    
* **What is batch processing?**
    
* **What is Parrallel processing?**
    
* **How many types of Series in compute optimized?**
    

* **How many EBS volume support -25 EBS volume?**
    
* **Which hypervisor use this - nitro hypervisor?**
    

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Memory Optimized Instances</strong></div>
</div>

**Note -: where you need high memory instances so use this instances**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Ex -</strong></p></td><td colspan="1" rowspan="1"><p><strong>&nbsp;for using space monitoring</strong></p></td></tr></tbody></table>

**Designing for fast performance**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>R= R4,R5, R5ad, R5d</strong></p></td><td colspan="1" rowspan="1"><p><strong>X = x1, x1e</strong></p></td><td colspan="1" rowspan="1"><p><strong>Z -z1d</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>High Performance</strong></p></td><td colspan="1" rowspan="1"><p><strong>High performance database</strong></p></td><td colspan="1" rowspan="1"><p><strong>1.8 tb</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>RAM is enough</strong></p></td><td colspan="1" rowspan="1"><p><strong>This is use for scientific reason</strong></p></td><td colspan="1" rowspan="1"><p><strong>SSD storage</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Use in relational database</strong></p></td><td colspan="1" rowspan="1"><p><strong>Use in relational database mysql</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Use in-memory caching</strong></p></td><td colspan="1" rowspan="1"><p><strong>Nasa me iska use kiya jata hai</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Instance storage - EBS, Only and NVM, SSD</strong></p></td><td colspan="1" rowspan="1"><p><strong>Nvm, SSD</strong></p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody></table>

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Storage Optimized Instances</strong></div>
</div>

**What is SOI?**

* **Use design for workload for hight and**
    
* **Sequential read and write access to very large data .**
    
* **At the same time are using upload and download**
    

> Types of Series

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>I=i3 and i3en</strong></p></td><td colspan="1" rowspan="1"><p><strong>D</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>&lt;</strong></p></td><td colspan="1" rowspan="1"><p><strong>&lt;</strong></p></td><td colspan="1" rowspan="1"><p><strong>&lt;</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Advanced</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p><strong>16 HDD Based local storage</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Nvme , SSD</strong></p></td><td colspan="1" rowspan="1"><p><strong>SSD</strong></p></td><td colspan="1" rowspan="1"><p><strong>HDD</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Sequential throughput</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr></tbody></table>

* **Direct Attach Storage - which storage attach with your system is called direct attach storage.**
    
* **Network Attach Storage - EBS , Jo kahi or rakhi hoti hain or hamare system ke sath attach hoti hai .**
    
* **Nitro System - A kind of hypervisor.**
    

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Acelerating Computing&nbsp; Instance</strong></div>
</div>

* **Using for live processing**
    
* **Live streaming**
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">To be continued....</div>
</div>