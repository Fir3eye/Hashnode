---
title: "Networking Introduction"
seoTitle: "Networking Introduction"
datePublished: Sun Oct 01 2023 19:12:04 GMT+0000 (Coordinated Universal Time)
cuid: cln7u9ah6000209mjaff0czuj
slug: networking-introduction
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/40XgDxBfYXM/upload/c5f4b7fcd0551ea489d6b5f7c4832f60.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696187474699/f88c0645-b884-4c2e-8fc8-b11e89ab36d8.png
tags: networking, networking-for-beginners

---

### Differences b/w **Hardware, Firmware, and Software**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong><mark>Hardware</mark></strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Firmware</mark></strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Software</mark></strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>This is hard</strong></p></td><td colspan="1" rowspan="1"><p><strong>This is soft</strong></p></td><td colspan="1" rowspan="1"><p><strong>This is soft</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>You can touch</strong></p></td><td colspan="1" rowspan="1"><p><strong>You cant touch</strong></p></td><td colspan="1" rowspan="1"><p><strong>You can't touch</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>It is a complete unit or device</strong></p></td><td colspan="1" rowspan="1"><p><strong>Is is stored in hardware</strong></p></td><td colspan="1" rowspan="1"><p><strong>Software is changed constantly</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody></table>

### System and Application Software

| System Software | Application Software |
| --- | --- |
| OS , Firmware, Hardware | MS office, Excel, etc... |

---

### **Transmission Mode in Computer Network**

> **Transmission:- Mode means transferring of data between two device.**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Simplex Mode</strong></p></td><td colspan="1" rowspan="1"><p><strong>Half Duplex</strong></p></td><td colspan="1" rowspan="1"><p><strong>Full Duplex</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>One way</strong></p></td><td colspan="1" rowspan="1"><p><strong>Send and receive but not at the same time</strong></p></td><td colspan="1" rowspan="1"><p><strong>Send and receive at same time</strong></p></td></tr></tbody></table>

---

### OSI Model

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">OSI - open system interconnection</div>
</div>

* **Open System Interconnection**
    
* **Developed by ISO**
    
* <details data-node-type="hn-details-summary"><summary>ISO</summary><div data-type="detailsContent">International Organization for Standardization</div></details>
* **Use as a reference model**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696185551759/e7c39054-ca66-4537-b789-6d41ed0f4db8.png align="center")

| Application Layer | **HTTP, FTP, HTTPS, DNS, DHCP, SMTP** |
| --- | --- |
| **Presentation Layer** | Encryption / Decryption |
| **Session Layer** | End-to-end Layer Logical Port  Pop3, SMTP |
| **Transport Layer** | Segmentation |
| **Network Layer** | Source and Dest. Packet Router, Ip Address/ICMP/IP/ARP |
| **Data Link Layer** | Frame, Error Correction seal |
| **Physical Layer** | Bits |

---

## TCP/IP Model

**IP - Internet Protocol**

**TCP - Transmission Control Protocol**

* **Non real time**
    
* **Connection Oriented**
    
* **Slow in Comparison to UDP**
    
* **Reliable**
    
* **How data is transmitted across a network**
    
* **Dynamic Routing**
    
* **Nd node verification**
    

**UDP-  Real Time**

* **Streaming**
    
* **Video calling**
    
* **Calling**
    

**Network Issue**

* **Addressing**
    
* **Routing**
    
* **Name Resolution**
    
* **Flow and Error control**
    

---

## Network Devices

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Application Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong>Gateways</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Presentation Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong>Gateways</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Session</strong></p></td><td colspan="1" rowspan="1"><p><strong>Gateways</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Transport Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong>Gateways</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Network Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Router</mark></strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Data Link Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Bridge, Switch</mark></strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Physical Layer</strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Hub, Repeater</mark></strong></p></td></tr></tbody></table>

### **Layer -1 Device :- (HUB, Repeater)**

**HUB:-**

* **LAN**
    

* **First Layer Device**
    
* **Not intelligent Device**
    
* **Half Duplex**
    
* **Always Broadcast**
    
* **Cannot Store MAC**
    
* **LAN Device**
    

**Active HUB**

*  **Regenrate signal**
    
* **Required electricity**
    

**Passive HUB**

* **Same signal send to further**
    

**Repeater:- Regenrate your signal**

### **Layer -2 Device :- (Bridge)**

**Bridge:-**

* **LAN Device**
    

* **Intelligent Device**
    
* **First-time broadcast and the second time unicast**
    
* **Filter data traffic**
    
* **Have Two Collision Domain**
    

* **Networking Device**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696185797866/f2cb6cf4-819b-4423-9c16-d29ce1e08223.png align="center")

**Switch:-**

* **LAN Device**
    

* **Layer**
    
* **Maintain CAM Table (CAM= Content Addresable Memory)**
    
* **First time Broadcast and second time unicast**
    
* **Slow**
    

* **Networking Device**
    

**Types of Switch**

* **Store and Forward Switch --&gt;most uses**
    
* **Cut through Switch**
    
* **Fragment Switch**
    

### **Layer -3 Device :- (Router)**

![](data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODwwQFxQYGBcUFhYaHSUfGhsjHBYWICwgIyYnKSopGR8tMC0oMCUoKSj/2wBDAQcHBwoIChMKChMoGhYaKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCj/wgARCAExAiYDASIAAhEBAxEB/8QAHAABAAIDAQEBAAAAAAAAAAAAAAMEAgUGBwEI/8QAGgEBAAMBAQEAAAAAAAAAAAAAAAECAwQFBv/aAAwDAQACEAMQAAAB9UAAAOOOxh4f7aNhsk8xtBSwAAAAAAABBRyttWiixv0TnModC0di8bRDNvmFgAAAAAAqFtwsUx1/N/OgtFu1Su0sAAAAAAB84reeP75eoY8ttPR8u/c5iHl6fU1azw+gAAAAAAA1W15nl0xyxy87p2OGGXVlSuQ2M7fauMVZ+7XUyHSD1+QAAAAABo9554b2HzzovY8roKsHP0p6bseJ7TyvXyCQAAAAAIPFPcvLtM8tfytXflu5T3eTt1+6uUU+q7PDMAAAAAERLodlr+XWrYYcW2GGeNJxnh+RNupjgSYxZZ265Tn97glEgAAAAHN9JEeK9Fymp7uDodFjtOLsgy3usi++9V4PvAAAAAABUtjy/if0NqTxTW9BKWvQOgonN9Vj9NTltPheAAABjU+XhpdxS59KGOeHDtjjljS2GOWNLY4Z4UnGTHcXrtqNx7fFkqW5AAAAAAaPzH2qA8Eh9Z8hMfVo+3Jnn3Sm8aXXnVKtoAAAAAAfPoQT/D6hmAAAAFWaEmkDCGzhSaVbZR8+mrj2mON9V82v2k6ubYSXiGxlJ1ZfJDalSxnRleAAAAAIzGXCQfPoYZipQ3QravegAAARkjm+kAAAAIJ/kRMAAAUj5exyAAAOSs1q+len1em+w6SfjuwhsBWwCGYV7FKQstaNk1o2TWjZNaNhHhZAAAADVZGzABX5bHbWroPm+x2zw6Tj+wzsGegADnbGjKGN4UV4UV4UV4Vet5yE79jkAAAAAAAAAa3ks8yun+EKcQJhCm+mfa8RsTqAANHu/PpixF0kW2dDe6u0jeDDYDySOxH6nnXrPzm5473q3532Xn+x728o7bLXoXyImQjQ8r03OFansKgnwnIaWxpm4+hRuUbx6HJHIAAAAAAAAAefc/0HPluSOQhr2K5ezwzLdDYUCxv9D0J0SYQ554Gk8v8AV/H+rn6DYx1vR8eXdeZ1fN9X9FPFeq5uv0BANF5J735rpnwWWGzzv92fObVOr9Sk7EilADnOe9EHnPz0fA87+9pmjh/npGuTxmPeyHnePpYjkAAAAAAAAADh/ncjhnc6M0Tq4pjmXTQGg+drnE8Rtt7MAAfPHfY+ftXyLVbmsZXK2FbbehtPXQnAGt8o9pH5e9t6PYgAAACCaM1XI+kLR5rB6itHmm07dAKWAAAAAAAAAAAc50ZHm0Pp7SOBz7tDnuhKTh8kiTKwzAAHC90Pzbtfc8xOAAHGw9jAScT3FMo9FDMAAEeiN3NDMAAAAAAAAAAAAAAAAAAAAQyRckdphw+No66/o95UCeA2nQ1SblO21JfWgAAAAr2OKJam++bZ8/uZKV6db9ObcAAAAAAAAAAAAAAAAAAAa84brvNrnocXoMPI/dObrN9w3c+f6QZ6AAAAAAAY+Seu+RzGOypbP3/n8tVrOf8AM9D9ESeC9Hxej6u0G/AAAAAAAAAAAAAAAAAAFS2PB+qq6T0fO63kNFf496vWai7l1dr2H5891NoAAAAAABy/URnglHv+D0zzv46/PTp+b2npBj1oAAAAAAAAAAAAAAAAAAAaPyD3sfnm56B5UX9xy3vh82wAAAAAAAANdsfh4zw/6bpmj6z5iZgAAAAAAAAAAAAAAAAAAAAVbWJr9lgM2GJKAAAAAAABTuYnnfQ9FWNbH0VMsSfMESIxIjEiMSIxIjEiMSIxIjEiMSIxIjEiMSIxIjEiMSIxIjEiP6ZhIDnOjiOF6na1DnthuZAAAAAAAAAAADGldpWpq59NDLofnI4nZfeM+HR2NPTOq+8nZOm1dbWnW/dTpjo7HKznTOZ1x1/3R0zr9TDAbmzzdI7CXkYTqqfMynU/aGmOw+8hcN1Y476dxarWSyKXAAAAAAAAAAAAAAAxrW0xUWyKi2Ki2Ki2Ki2Ki2Ki2Ki2Ki2Ki2Ki2Ki2KmN0aDaWxUWxUWxUWxUknJCJI4C2AQkxULaGYIpQAAAAAAAAAAAAAAAAAAAAAAAAAAAADW53YipjsozUR7vIho7aI1VjY4Gjk3AlfQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAB//EAC8QAAICAgECBAQHAAMBAAAAAAIDAQQABRIREwYUMEAQICFQFSIjMTIzNBZDYDX/2gAIAQEAAQUC9FrAULt9VgtbafZ+32blerE7zvTVMm1vXfvkQyWbi3i9MmSUoEjW/wBHsjaIYVrJsMnO6eczzunkWGRg2sBgn7G1YXVRO8ZYya+zt5X1FNGRlL/H6+vIUlN+vGfiC8PYxGah5WGexsOnrkT0nkucYrrkxMTCPpwBeMOC+Fd3WfX3gdzUjaVFf8QRn4gGM2UxmunrQ9bbSwalYybYUOCvLRrRmm3NdDEPU8PYF++REzkIyY7Qr6TJrnJEoj4L/s9fxM1yoo/VKwyFZctLVmp3NMq0TBR6rg5rJfY2gEIDY2c4Z9SUmBwilM1/EdqvmutjeqesUdcmOmQ6YgjIviLJGJd1jJnFz1d6+9r96nrf4TYWiLV5tjJ/VwFiMLtuqMp+Jz7nq+JUymxFjukoGMJaxCEKN7r9KtVXotPN9gxAj6hmIR5lefv8OmdM6fHr8V/RnenFnDB9Vg8wvyyjaNnJSkTMRGa6id2douuvPD2l8pHq2K67AbHw1MZ3DUbHR08xKj1NB20Lbtmsldm1J11MVl6y2tRovbbpehMwMJiTLJ/f0U/3Yf6TfWvayvdjYaSzQwHxONbirblZodPNefYbDX1769torVPPD2km6UAMAxEPm3WGyFZJKxtcW2EV4S70C/WZ8Gh1yfQiJmayeHwKIIUTMev/ADLaaKvcnYa61Td4d0kUxbPRVXYO7VNdoh2THqSRWaw14ZC/V/b4H+WfTcU4sIAMnJwo65IZI50zpnGc7c4KYwB6ZGR8HjOCUGPqHPWYjpHxOOQIQKqlalKCsqh9dWv/AD+xX6TDgASM/J0zjnHOGcM4ZwzhkDnHOnyD+k30zLpgjxj3TPp6Q/rM+d1u152vtEzTiwiTHaVitjfqEVa0i18zQ7gJPmPozPSAj2JmKx/Gqc2PSX9I+d0yZRHSPnbqosXa9a+k0a23TlGusqxWreKdemUUfmb+mbXqTnnq2eerZ56tnnq2eerZ56tnnq2eerYP6npWthUqZr7q7yfi5y0i7xBWgpdt7eDp1kXaWlfobC7IkVZY52FZ2FZ2FZ2FZ2FZ2FZ2FYsZSWuct6faXrQVlQvrnEc4jnEc4jnEc4jnEc4hlWxNIhmCH5be1pVc/GLVnJp37WVtZUr5T/l8d4hbry1rQHmERk20RjbqiP59s869RauyHbLOBZwLOBZwLOBZwLOBZ2yxvKvIz1H2fXncLjJdAzoGdAzoGdAzoGdAzoGRAZpZkT+SY6xo6deKpNWOeZRh3a45q3Q8fju9i2bEcmEC87WFYSq2tgMH5t9/j2JMBlUmEpDXk20xwuMmRTpGwz7tjuH9Dd9FyU9LH+Zf9fs/+wEWYZcU42QtvkqanA5yLEstraY0wYAJ/rb/ACV/LVRPmvz5yLO5GCQlm3tHVRWssbigwV4/ioPDtpJL+PimtxZW/MBOUgbd9j8ke7KOVfKviN68123qX5memdwM7kZyLN5y8nsHyg61iWqTdJjbNsktOxI1Kdknn58+Zz+o/wDrn9rP+Zf9fs/+0GWu5cN4sgneSpm8nOZZhlsnCNMmkCfotv8AJX8tR/q+JCJZfriytTHt2k5Z2S1DYcZGqvidpapZW8TV5lLQcreV+/TC92lWjYJAs2DEZWpnYXbrypuh0o0VQsI+TexM0zYBlzCM5BnIJzmHSDCM5BncjJMZzqvHnySv+HsyrWhd2Ledi3nYt52Ledi3nYt52Ledi1nZtRnYt5qkuWz5J+sbcfJ7ObJ2RUbTNaoDAGTO5rpUGn1R7N6VAlRjyHZ+HCMoGaroIZhreWfjNpidFqPJx6BzxG3aCmmtY704q0B5YbCEKPuL9zZumF1L+S7dqEoVdQ2zZvrXizFglHWBmevzbTWrvr2WnsUcS0Jhh8Mq7BtJ1JFjfPSoEK+N6ki6raaKzTyINp+H9MNAPRn8zNrCZQXmMp17EuqoiBBY+QoImve9zswhjJ193tO11kql2m83PreZDW1yRbwh5QE9fQ2nh5L8vIs026PUM2TkqBCvmGlWG36Mz0hcfT7OY9cEuUfPZrqsqSoEK+Xar7u0roM3pVCU2Kpnf1I86/zs+s/aSjpMT1jDIQGtcr2i+Nrusv1lMttctk1lQxt1C5WPw7Qd+1VTahCVoVYoV7DVLBK/lMxAfximVlf1n7S1q0i3e1QbL9vayNOthUFLS/4rQC3Popc0BgAnXq7vpOctIu39WCl+3t4OnWZdlaVxHSPtNfXIs3VKBIchjCeocoOB1r2O6rKdtFrUgPMJjJtIjCuqN32m6/y6F7Fp3I5MwVYS88PMWVj2BftuNi0rccmSC87WDZQq8sxYP2i0vuoFfZ2KYx1pVfLVs7GLWRGjb3KsVfEdRmKYDQ9bxPX4Or/WCequNu+yxkj3SRJVsq+JHLzXbapsJ+z+IFeXv+dJk90pYKpmcbrnSqtSbft62kuhV9bf1+9SG9wXaJgmCyOOmV6RPTZrEL9DqA1y/s+0ojeTf1NrX5XJcCZQEV7hIszatbuxraKtfX9dgwY7Lw2RzAzUdBjMNbyz8XuWR0mpGgH2rZ+Hkvy8mxTZr6T9jZ11FVCv7K7SRdVtNDZqYsGWG6LUBrlfbLCFWVUaSKKfaCYngV642s5D1+1zMDAkJZBROEQjgmBexuf5KtR0UdemhCtsDBrJqa6VLCFh9q8Q/wDx7VQ0BWRSUzco/JXpj7GYgoEYAQqoBuLqoUzOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjOcZzjIKJ+ZgA0MTWQiTAT9uX8csXO2+bALUdlC481X7Y2EmoHpYuxs6qgVYlloLVdgrsoabnKRGx2AVVd4AUuwloOv111U2UuyLCZDzCe864kAq2gclNhL8PaJg6d1VlS7KGYFlBh3V8ovVZZrdiu3XvW/LFUuC8RtVyUywleVbyH1PMo7azBoL/AJe/L+OMW+rtGw38Qqa9ymDSbzt0Hsw6LGIvCdivcqPsk6s2waapg62tgbRdBy6e4QT03qDnM8mTq11dhtepQNGwXSseVRT6Br6rqo6dblS5LRsqqGLVa5n/AB5lVtp3Fplqv0bFak0dbtq52HHSs+VsU3WpSDn7CatlmsKjJrERAV/y9/P7cJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOcJzhOErmNfWVq7OE5wnOE5wnOE5wnOE5wnAGYn/w5mID3x6fGGR8PMLwWRLMUcMD71Z+li4fGuMSVqt+YIZPlm/nW4Z8vLZCm05A+nbev8tf9Vn3qYgohS4HpHWFhB9oOXAekRAx2lyfSOoLBeQoIKVhJf8Ahv/EACoRAAEEAAUEAAYDAAAAAAAAAAEAAgMRBBIwMUAQEyAhFCJBUFFgMjNx/9oACAEDAQE/AfC1ekGErtFdkoxnTzaMzsjMyOMesK+V5t22jE2z0/xEoBPbY0ZcU5rqCZPNIaboyNzMIUOCa32/3pRrfpVoNpEetF2DzyEu2TGNYKbxGGvF7qHOtByzruIyIu+we1ZQvgk0jK38pjg4euYUZAPqmSNcaB646/SigfLtsoYhE2hzMV/WaTWOkNNWHw3a9nfq+Nr/AOS25F+Lm5hRTWBgoalLKq1sqr7PemXgLutvfjT4kRnKvjT+FES5oJ0TsjmcaCw+DIOZ/GxOHdJJ8qhwrI/f102RtZt+2HVrxHBpUqVKlSpUqVKlSpUqVKlSr9P/AP/EACkRAAEEAQMDAgcBAAAAAAAAAAEAAgMREgQwMRATQCAhBRQiMlBRYEH/2gAIAQIBAT8B9AaUW0Np0zG8lHVtXzY/SGpYUCDxs1aw2dMwSSBpTtPG1ajtBlN52dU8tFDp7kfUExo55Tnf5VKJ5Y7ZbpWYBxKxhb7lHYhdg8OU+p7h+na1I4Xu3hG0HEcJ0hPKBtw2Tq6jDRyiSefEnbYR6FFQxl7vOITorRhXYKbpwmsr8BTSsWpwaOPBa20Ij+lKwtPv5gFoRKSMtbddfhzgA5S6nAqaUymz5miIEotTzYKbUmQY9WSOZ9uxW+BapUfS1xYbCc8vNncDqXcWe6DS7hWZRN/hg0lHaES7Tq48aDS5sztfLN/alADyG7LTRtTSYhSaskYjxoJ2shop8pdtvlc/7v4qlSpUqVKlSpUqVKlSpUq8JvS1fqv0Wr6WrR48G1kslkslkslkslkslkslkrWSyWSv+P8A/8QARhAAAgECAwQFCAcGBAYDAAAAAQIDABEEEiETMUFRIjJhcZEQMDNAQlKBkgUgI1BiodEUNHKiscEkQ4LhFVNgc7LiJWPC/9oACAEBAAY/AvM5pXVF5sbVkw4kxMnKJak/acPsLWyre5t93/4iZE7Cday/R+FlxB97qrUTuLMygkD1Ax4WKXESjgor/Kwcfi1Z8XJLipOcjVliRUXkotUv8K/39T1NdFfGt9dY11m8a6xrfeukvhWh9RaaZssa7zVvo7ByS/jbQV/isYIE9yH9avsto/vSdKgKh/gHqGORiFC4hj8DrWjFu4V1HroxH4msQzADqjT1LKnj5L1wroWqxFanWulrWi+TK2/1DFL+Anw1qJ3dVzKDatM5+FejeuhF4msMeca/08+xi31IZOsdfLZ+sdyjealGIumc6EC4FZoZFdfwn1E+TStTXWaukxvXRY+NXI8q9/qHRPQOhpfKwj6bDfyFQwvJs5FUL09BVwbjzzLTJzvWZyAo4msmGBF9zWux7hRB6ch3re/zHjVzqaDxEpJ7ym1ATBZ17dD40k6KyhuDeo20rU+XS1WI8qd/qDcxTLyahnOp3KNSaZRZYxvAOn+pv7CrLqB7R08B5P8ACyPH2X08KEeKgz8M0W/w88mIQbt9XmcLb2iL27hzonMwB3txNWUUI4VzueH9zWWZruNWk7eQr9oxAIwg3D36CqAFGgA870jXtfKfNrx1r0MvhVx+fniKmVRbMdKJz9NvZ3k95obUnLvy1pRPUgHWk/SgIVIkbRUXW9DEYoXxJ3D3P9/PZZVDCtpgGv8A/U39jRinQqy71IsRXQ31nR2EnNTrS4jHlv2VTp+OsKI5GgQyhCY1vYWO4WoQJI9pZcsc0sdmyhbnSm2k7TDhmAuPCpDI6RSvJs42J0FzofDWsO6SjOr5ZStiDbf4+ZJO4VtW49Uch5xO/wAmf2G0b9fP/bLrzG8UZIft4d9wOkO8VrbvFWXRayYd36XsjcfhX7Vjeni25+x/v6jlxCX5MN4ovHeeDmN47xQnxIIww/n/ANqyAAJa1qhzsc0Mmfv0P60oYsrKcyuu9TTbSeSZjxa39qhlYn7K9l4XNTupNpSGy8AbW8zl/wAtd/aeXluPM2FZm63kIO40Y36y/mPP/hH50ZI/scR7y7j3igk8ZNzZWGobuoYjEi+IO4e5/vTkbwKhn20+IAjLzq0WVV6N9DYcaimmxV83SaMIMvcONTSRaIkDtf8AFw/vWGmOJaZHZUdHVfa4iwr7ZszZjr2X0/L1AP8AA+cCJ12/LtoKu7zetaD6gkTrr+Y5UGG4+dyr8Tyqw3fUK8xao8P1kVAmvEUgXFTGFOrEbeF7XqWFjYSKVv31EcRiJJxFqisAADz09SKnePNFjRd+u35dnqWX2H1HYfOabzurt4+th+W/u81n/wAter2nn5jFxRNhUSAKbyg8R31BLiysDyC+Q/17qyLIpbJtNPd51HCpvnXMHtTBZ0JUE+G+j+zyB7b7fWy+B5V0uuND5q5rM3W/p6jmkYKvMmkgicyuzZegNB8fN5eW7zGyX/UeQqw3eYxzzohWVVEbcVNq25jilleIRuGfcRxqPY7KQ/s5hOZrZTmJv3a1htF/dzA/S6tzvoRNDHmjRlWXbNxHBeFQRMAGRADbn9fajduf9aG1dVvzr06eNenTxr06eNenTxr06eNenTxr06eNenTxoP7Hs9vb5r7edFPLefCjJCHChsvSFvqZppFRebG1ZMKsmJk5ItdFYsHH26tWfGSy4p/xnSlWFFQZ06ot7Q8zsMNrMd592rMXZ+OtbpPmrdJ81bpPmrdJ81bpPmrdJ81bpPmraYUtnXep9oUWQ9P2777+q3fUncvOtriRdrWCcq9FH4V6OPwr0cfhXo4/CvRx+Fejj8K9HH4V6KPwoAkthW/loFTcH632s65vdXU1/wDHYFyP+ZLoK/x2OKr/AMuDSrpCC3vPqan/AI//AMr9T6O2yZkLMh8NP6VaNUjTs0r0qeNekFRxpmJaRNbfiHmM0fWJy3ohSNod7Gt6+Nb08a3p41vTxrenjW9PGt6eNb08a3r40MTEQHHWA3GgfVMRJMblHyr2VfOflr0h+WvSH5a9Iflr0h+WvSH5a9Iflr0h+WvSH5aILXB3gisTFc5EIy/n9WxoNsUMysyliL7jXTkUd5r0q1179wqd1BA2nH+FfqInV2cgcGryMWPb5YgzjSRSx93Ws0bKy81N/rr/AB/rX2Q48r1IZB0hu0pA46PHo0RGOj/DSsB9p3U21GluVbtL+7SDo61pR1qT4Uvd6pi/+9+tAm9r+9QMV7W51k12nfV5L5bc6Yre1/epNne436021vfvodb/AFVJUnfWMsbaj+9eyfyrVD8K1uO8V0SD3VnQVKM5Cs5fKO3y5pCFXtqVA6iQyXyE67h9TaDjSnmKvK1uQ4mmSPoIN4B/8jwoBD0R2WFZoZXjPvKatiEWZfeHRNZYXtJ7jCxrWusK0DeFdQ/GlzAdfnRsAbmnYgdGlUqNayACllsLmiCALVlyrvtUev5UaNSfCl7vVMX/AN79aF81r8qGyva3AVm12vdVpc2W3EU2XNa+mlJsr346U21vehoR31JUnfWN7x/f6nSUHvpx/epUPkOxs5949UfrWaVm2nD3v/Wun4UAk5dfck6VBcWjRH3hqKWSJgyNuIpuYpEGjbrkbq6Vwzjibsf0pdrog3IKsKMtykC7359i0IoztHfcBvraTgNiG/l7K0VfD6i2BPTokxTfLXo5/lFeim+UVrFP8oq2zn+UVpHP8or0U3yiupiPAVrHOf8ASK9DN8oplWOW55il7vVJ8sAZXcnU9tfui/NX7ovzV+6L81fui/NX7ovzV+6L81fui/NX7ovzUP8ACr81fui/NWIaZMue3Hv+tnt0WBprdUalb2Ud541dN/vW6vdV97cSaCKCzNuUbzX2koEi6sPZFZmuuGTrNz7BSxxKFRRYAUQaaXCOM59huNFJ4ikg4Nvq4NWG6kwyhZD1UyrW3xPTxb7z7vmb0hkzMWIRQouWNODDNEV/5g8kQYPFJLcqjizaVJK1yqLmNqVxezC/rS4WCESSlNocz5QBX2wWKQC7JnBy1nj2bta6qZAt/jUsCuNpHvqHZlJQ8ojNn6tZo2DLzBvVjWVt/wDX6+ViR2ii7rtYPfXh3igN1dvKjLGVuRY5hWaS8eFU9M+8aWOJQqLoAPqZMRGGHA8RRfD/AG8P8woIt2Y6ACtrNZsUf5PNAe7rS/tEMsiZt8Y1Q89KaaP9plw+HdHjMi9NveA7KggmDlXcYt2+HV8bV9FSYiFz0XDHITrfS9YgTxYg/SOWTMSra7/hasHkEgEkH2t76nTf60olwDYiO2joRmBqLMGLSgwvdrlI8wPx41ilMRJjVYIfxLnvf+lfSSRQm84UpILW0Go+NYZU+jjComTOCF1Gv5Vjvs8kTOCnLd5bHrDzBkwdoJuXsmtniIzGf61me64des3PsFLHEoVF0AH1ziVhQTnTN5q5q53nX7ouOsPMmOdA6HgaWOJQqLoAPrQqcO2IGxY5FfLxGu+osHjWbIsRk2ec69LdfjYWrZxk2G65valhMQxJjwyDpSmPidaw8xkdmSMxHNzvr/TzAXnv+6sy7+XOrjyFnYKo4mnXDyrJk62X6n0gka4x3GXZ7KXKqHL31OMVNLeEiPLG5TXKCW0762cUln06TVirx4qULPYMmIyhRYcL02Zi13Landr5RNb7QLlv2UBOmbLuN7EfGhHEuVBwraSq2e2W4dl0+FLHEoVF3AfWzOwVRxNJBHLtJGNugLii3Pd91ZpnVF5sbVlwokxDn2Y1roJFg05t0mrPjZpsU/4m0qVYY1Rci6KO1vqSyKOlLbN8K2hzq50Jjcrm77UqrooFhTyK86F2zELKQCfN5ppFRebG1ZMMsmJk5RrXQSLBpzbpNWbGzTYp/wATaUqwIsYzr1R21YfdWMfFZ5HSYgBm0tvFZYkVF/CLVqy+Nayp41PszcBE/q3qWA26ZkYOv9xVo1SJOzSvSp416QVFGmYkyLrbt+6i9r2rEtEcm1sT8NKu7M3efLicjA6L/f1KNeqYnuDV3JY9vlhzOOi4zHgKzRsGXmD90sppkPb5LN0pPcXf/tV2IEXL2f8A2NZ7kdu6vSiVPdl3+NAYgNA3bqKzxOrqeKm/n9oONA0DIdTuUak0yr0IxvAP/k39hQyk5R2WHwrNBK8R5qd9WxKCZfeHRNZYHO035GFj90RzeyTWSDNfkvWP6VlyBtep+vOs8xzNy4CtdKDN0GOqow1t28qEEI1HWbgKWCLvJ5nz7cxSIOibam16ynRmGvSu3xpdt1RuQbvIZmJSD3uLHs/Whh4jtZH3Ab6zvZsS288uwfdGQ6HnRZgWh4vH/erDSrmlmyI2Xcrbq2WHXJfrtwAoRQj+JuLH1AqaaTCOMx9huNGOaIpIODb6verblpMMlpH3LYVtJenin6zcuwfdZkwZEEvL2TWzxEZRuHI91CKL4sdyihFCO9uLH1PJiYww4HiKL4b7eL+YUscYLu2gArM9mxLdZuXYPu0xzoHQ8DWzw62G88z6r0WB7jTzJHGJyOkRv8h1Gm/7suTYV0SD3UbEG1dIgd9dFlPcfUZ/4D/SsPiYIIIXjw5YNHq8hKaX0/WsNLCIi51WT22NtfjvqeeBm2iwsoA/r30ggWDpoQrC12FvzpUXcosPuvEfD/yFTYjZxYWMqsbLhz7OYZm3DhSnDJArlNMltVoN6TazxDZv1d9LmwuHgyvnAh46dw5+okEXBoKgAUaADhRlSCISn2wov5C8UESOd7KoB+5tPrFJFV1PBhfyEwQxxk78igUM6hrG4uOPq58ggiieafLmyLYWHaTSPiWWDNwdhSmSaNQwuLsNaV9vFkbc2cWNGVZozGN7BtBRkSWNoxvYNoKibaxuskmzurjTtqRBszCEDBxICdeynZJ4mVOsQw0rJFPE7b7KwNXmkSMH3jaoirRM0rALmew/i7qRppI1zW1zaE9lM8csbqu8q26pJ1ljkRPdYb+VJs5ULMLgBr0rCWPKxyqc288q2W2j2vuZtakySxtKoayZtSQN1QFmRZZIxJkvwo7GWOS2/K16xkaFTJh1vbN19L6VGdpHtSgdkDajSvs5om0zaMN3OmdJ4mResQw0pFzrmcZlF94pUWeN3ZsoCHN/Somd4kme/wBlm131CqxGV5WygAgVNnUwtCcsgfh8aaRZ4jGu9gwsKOeRAQuexPDnQxGdFT2rsOj30r7eLIxsGzCxoPGwdDuKm/3CfJJio4WnhmQBgnWUio8W2DkliMOz2emZDflX0WJI7iMys/EJfcKUGDof8QaS1tMlYzYxkD9oSQLoM4A1qZoosQXaSN3TEZRtAOGlQSRYR12OIWQxkAFgN9fSGyjaPbQx5c2neKkljwhw4XDPFl06ZI3acK+hyIbbKNhIQN3R4/Go8T+znEQ7HZ5VtdTfka+j0aPpLihIyjXIutYdUjz2nQkdlfSYhjyiTZFeAe2+sbljxImkjy/bZBfutWFxGGgdMTFdMh4Ai16EQU/scR2qHmxAH61DhDhrTJNnOJuLWvvvvvX0o7QDavJJszbUgjhRjmheaOeCxPtKQvU7qkVkkGHAAj2qqH7tK+kwMOzDER9B1tvyWr6HIhtsomEhA3dDj8a2SwquKPWB0LdLdesTLHhv2dWwphCtYFmqBp8PLFFHhWidiQOFYBsUsyHLs4vsQq68zfWvo1dhaZMQHfTUC5rBZNoFWS7MhsV0rEYYR7UJOJQW/wA9eRPOsbLHAYBJCI1jawLm971tHw8kSHCbHp2616wiCCRHwzjOvR6XaKhtBOQ2LWSQTBd1tTYUFRQqjcAPvwqwBU6EGs8MCq3A3vb/AKRuxsKNg5I9nLr9Q3utjbpcfJvNudjbxpk4r5Aw3ffeHLdS58afK1mtUt2ay2sL0kjO2c/i/K1QXc5jJbf21JmLaTW391OqXvl0pZISmVV3EViWXQ2XXlUIR2ObeC1/jUbq5z57Wv27rVKwIUq1rmQi3w++rMLiiBGoB4Wq9tTWcIubnar5FvztRGUWO/TfVlFhWbZpm52omwud9dBFXuFZgi352rMUUtzt/wBD/wD/xAArEAEAAgAFAgUEAwEBAAAAAAABABEhMUFRYXGhgZGx0fAQIDBAweHxUGD/2gAIAQEAAT8h/CvINAJtfFj39rmdRZmRefl/z74rnmHhnLrJ653H+oId1mApifoOkyrYX69puK8r50g3eAV5f3OCvAdp8pv+n3q2J7pGgDoRXPz5/tIDLNB1E90jLq9v0cCEMBc2jLljzp/J/nUmZQ08en+mMdaW3ll2hqgoMg0nym358pfL2LWSI5XUOba+B7wTF+DKC7QbMff9K0aqz+hiGZL9PmJSsCWgDtLjgdERWHqmRBzDBszjl0zv+gOvVev9Eqxj2xxNo/xX3x018vebp7/xRHM1Pk/OqVEivXQvDCW1LyGCXlO/C/mYD8ZNN0/gqci2s/R1Wd/RGivSXFoO1Q9yyCYqXd/cXizhi+IOfqq6P9CmsDAXeK8pdLDKGUMChx+XV4I/xurZRVjl5sIiTJHP8wOakVjAwI7zKJRKpqGfJ9WJio4X9z4MJ/SITTKS1PKfHlvB7S9P2Bjhh4/nNcxM0wqjMCtoq5q/SvYHSWY8dn6AROh+v6GBjAuYWZsRsZyr4MhuxTRAGE9tUPSO7KXQ73rMrDmLLxYQ90qDMfyfE/NdNE9kesOIVRt65mSEiMMBrneZ/wBWKgNzQ58oppUE020NoDQuNg/13fA4HAlBQG35TTVeWFr4Tl+PiWYjJjEOkR9VxhWMVmmhwNcZ/kPeY4jGkzDs/mJfUmY0Tq/KVDRKTY9Xb4JXwOC+EoAFGxBI5Ho5m95yIkmws+JesEkxuafmGTDgjLm8NX4ePnDAwqEAai7QFGMmnmi3VAZK9rzfgCYxKyexsaTdS8mPgNSizfaVBJVzbmIL8ogaIailOnYm4oghngoJW5+Fy6C1iA6RSfC36YVcfoxjGMYwXRt+mAOjwOn8PL89U4WF0GOBQ+Ej19IlTtrkX81l9pyZXHM0Ba26cpuCAYv0SiNG26bCGFxrwfhj6RgjYGS9j1PgcAQiklAbVKAIhXAL8IADt2gancxgaoHJV0ABM4UdYFW9C/OWRxMFCxOtHl+Hq79IWWNXaCnH6MYxjGUpV2JfzNBtBgh2FJLRXkr4D+dytfHltMZexqxfhjM2FQq2W/GcAWLfD8ZxmFJR8JhpLjQe5qBrdxJCGDMTM2WY25RHDIbYQcLAqjwMwCBkuWMq+IuAM3R0fmAABQafTgh5P9e/5DdHcNYyEH2GoJtRCKltpZpBOJuDANEdIPqwAvFrzIYGws/KllS+A94RBQwD6IOZf0FpoSFRpTyCsZs4rkMaWIC8C9CKwVRmAqIJAwZaigLTS/0UERLGJP7SaPzb8WQid4bqbhp9hhhlh+mSfQkE19ernqh/Pn+SiAvCEwi7WK3f28XoPh5/izLN+8Kis5tSxMwTEglmNXWDzXOuwFfJtFDExKm0Ay5zihANOZob1xDGHW2i/uBE05hq0Y60padn8RumBFtzGmzb9F6DZ0giLJs1Y1bkrp+JlmXBbmnt+AC9WWXwthGFAoPwZ2YhkoptjUvS8kYgLU2JSm8xwpFCuhN5HhKJeFDVxFMMcI5vYju0xMLWXpnAWAeTBj3+/D8U49k4gq2f4da1rWtaYwbGPweX4rypb+yxibCapgNnGP2cHmIm1blV86DM2FrlvnSH+XE8B/c08ffhFxShkPeUWYTKT/KT/KT/ACk/yk/yk/yk/wApB5Gc7goSzYyPZ+qn0P8APlNYoKbpt8ynzfvPn/efP+8+f958/wC8+f8AefP+83kNij6x8SYOrgpBWJk/daCx/jGXjHCo8vh95mhcwp0v/ZXjnwmdj+ypiMi1a2ycx0OUDHOeGWZl4Qsp1SyA634LQ0Pgwce0vyZlzgHx+k+R9p8j7T5H2nyPtPkfafI+0+R9pkIaZJl7RuVqgeSC/wBQD6hZotqiWz89h2nwXtP9B7T4L2n+i9p8B7T4D2nwHtP9F7TGnh0QZZGrjpeL0+0myHBjPsRhamF5aZRmk9hGJfwNwTNwWNMNQzYfYZxW0Sf7OpTu5dHBlA2NqAFbfDKE3vKofH7+2+kOGxcdbROViK6RiNnNWMjwGVpjh1X/AFgdgsF1jcL5fTcRbHHgmL0gsQDZiHM8IvSGq957B+p6z1hhawvCMxwqwiTi+reWRxGd8Ynt6qCPiFIeqxwzRq7i4YwnifxO0+rGYu27jD/f7pR6gM90Aec7oi5iNTHt0Si80HaYMLCjWE+gAhlF14fZQlhmi4EYLxjIxXgigNpKHxUY6Rr418Dex/Liy/SeLRvqaxWstHs5ekGtUv8AzD4QBaA5m07sNzcXj/mXZeOI1QCmVtHiL2EOPQg7DkrpDmR1gxymAOLBjgGGkpHi8Ig/EXMoyFrhiud0es7U9J3P852D9T1HrDhy6+MIt+xMZeL1mc1YDQxg3h1glzxWi01n2FlQIHgLGdx/E7R6s+T3+z2QFwWjlgWryibCvv8A3BB6lwWxuurgmKqGf0GQ7wMEdI8KIauuZGUv4+Z5MDO1qwZhMwMJlPi1zwGsG5iLQudnHrBCm3J1eeYAUUGk2xIcXl/ZpMq4D68sJUEWOx2Pr8tCxPA+wUYpkXozHC8ckAUEPwygbZb8NIstDz7E2C2/omQLp7E+PfxPnX8Qegtn2Jdd4nyymJvBvb6Tsn6iWLVHdWs+A958h7z5D3nyHvPgPefIe8+Q958x7xQErwPhgD/A95e3pmB5ev2iwh3VoEzqnkE+SpgeqUIUOGkubX45q4ouKDcMO9ch0HfmY3mr4i/SbS5zEDLTMzQHI6HSZvSA8xvHeEMXiKHD1urApTQUN5GBnAuwWJjV0Od34/gtRi6G7MTPoj6BGqNrBLvZFHL6HkhyMLIfaIM1BpAPgJHMv9rXXMCazptviY4znUFuKmmF3FqrABNhdtMY4OgCzHC8N612liYTLMLbntlBidskFgsYbq47N/vdKfEIvRGnh6D0lFA8OD4wzWdYw9fFom3EzLkHPYOfSFfbRj7PA2R0XSDXzxyw+TXqdoWiNHdu1QWYPUGxzu/H8PBMTrp/PaCtAt50GseEsWK0jEqwC0ddoleyDQ2tehD0l+paEFxiMk5FWo0qo8ovsVSRis2uf7QxlfGiyxRNMRmsEXaBbsK+MPxU2WHpuyDbUiNRN2Zjxxly0pCksYOIvXeZDjxgtaHX6YRdJiJoxbDWYfz9+cRYjFp55p4eU2QDtyHWYwg516npDvtox94hQsTHr15z/ECJQYsYqU9vnb/kJTByH+IVhgmCOj+DQ789zaHfbRj7gwO4FHXI3rxlfx0NddLinjKZt2LfiY5HIgXTkvOoutXLQS2KYNb/AAea3QfD/lPRXq2PeESWP0zUELQRDBXUC7rHJyfso1cNEDnhM8cmAzExOoAu1VekwykJjXSXdbl+cSVIwvGsHe8tYUrlWNGwHH1WRjhu5kUrqEEzZZLoRiQFWQHMuR0u2WWmxebDI9Q6D7meahaCGC8fAOrlOq1dB8f+Vx+4iMNekpd7maj6B0/ohAY3g9D+5bk3gPsEnDJ3nSjtGlfC3BpYXDzog2CaKJNYxoa0Px8HGI7zbYjK8/8AZmQ+gfOCCjjeB0LvvLpcOGafOAAUGAf8oNFeNPOazjj4DtHLLqJkU8MWq6LVfpFFjQKmIGR4zgdBDHNQ5t4ds2N1AM2v/KcuAVwWGxsZJetG90KspWMAcEynOm9b5n6KRpnPImO0/mdZ9dy6ODKApxVvmsGo2Vof+SGpiNhK6TIg+JVZ6jZyw9v6gXj237U1tthxeFZQtfUzwDHzlgA19WfyEPZAiB8T89eeEI34GbYMHgyYENIIQFuDDt8g09WYWBi1PEZMwMz/ABcvSVgKWpB6Pg/8dyg5FQWOH5YAX09BzGiAzWUXdZxldNGg2CYBaAauRGdNaxuXo84UZTcHdZZyg289Z/PfAwLIt7GmKHQ95iBshi+Hp0wi4g2aP7hQoMCHk+FfBcf8TKNA/dMFocZ+GP8AyHCYGGyYMJq1lx0hQR76PjLIYacwV2thvq68wnfHN/x+s5aCeIf0MllJnDk5HQ6TMl4VdRvEpwGd6RCj3JTNdV430MGOEDb/AMGuv/KcTGOsHFr55p4eU3LwcQ5awkF18YGc3ZvEP6fhaI5R0gzU9K8818PKP9jdmYOk4D6Hr/zc9vw9+Osxl9sW05f1Fotyl9h+eJK+BhFjmXjWsGAZyLy6zP8A5bgQZrDbN3VzO2KacoJYpuqdEXM/R+L3TLpRKZRTVvlDsfaqysTm6h7QIvSGulGuSALJITqNueDO4FNE6R/y8eEO1hf4y5xXGoWMsljMmZJsMcMzLH3mmcjGStZODrnD2ZJCxCC/0YRYVImCQrqgFAMgllRLCd545/TOiEI8SLRc5e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e05e0QpfdngyIHwYllOJM/Tq161AwEGMUMnr+v2H0BgeK8giiP09HU7XrLiOEwNzeIJO4ygzpuZVp1eszLJij1HSAkgFBuWORZfUlpM8hmx0FawgQWmDu7TDwOKldCCX1QmF8ZRiMwR1OzeOAZxgMMk5zKhlqdTpM+qF69HVK5RuiTXLaINV6K2zq8T0VvbLzNqeImk1gQjsZ1tzGC5pVOtRgBChiGjVhVMK1bHbQuGeFxNFS69X8HMxfwrjrdIMB8AN7xuQF4Lot3LUc5TL0GHIjLPS4jTLFqF5sXramY6u6NVzMBIjrqOkz3pBH2rwuAiqvNuy0YOHUijYZpk4Q+Mzun/A7D6MYAw0ShSz51cmFZfUVNYm0BGKCqu/M7y4mlkKUKa2gRRhnQxeGeOO0YplWPbJh1M86i4fRyqA1qeUvqAYVkxzc6w2ljHpoqUTQ3ZgjqQXSV5kct8xDEr5DC4BVUADKq9i5QM1tgG7XiUTjkdBbecwwjyxGR/KxxaYCNmwOQ0wzBz28FfDH4xTbOcbGtrZCo1wtU5VtzbAE1FWGFO7Tw6xKz6QrVrDdmhq/AEhxsVmAkhBdBXmStx6kAl7dFR5thKWJgNUYFvEwhm1DnpFrLBZrLEtEaCfEG+8XzwMs3L4VD+wacNV6QLxCwOY6jJiyv+UIRYDRlWMGNDbmdFw61GOFWhqVa2Kcwku4MbDIamEAimDwmd0/4BtnE4ZwzhnDOGcM4ZwzhnDOGcM4ZwzhnDOGcM4ZwzhnDOGcM4Zwyp9XEBHSAiXULotw8JwzhnDOGcM4Zwzhlgdv/EVLQbc1vEH0GvsYMji8Hg+iK4waS3aqAocBdsfoLaK8/wDtow0AtyEYfzMojYppziNTGLC6lb3LYqrx4P8AIfBEWpxWS9hVjGUXALlcWbbrdlBMBseGeEbzYXmjSIvdXA3Zf3Hafh7fQZYxbhAAJMrpT4wui8/+y5AmYljM9NQNMCQBmNZxQA9IvzhaN9tptYq58UZOqGQBkBQRvKXvDvznXAKzl9jGdRcCAnIGyHzHJi/P/wAP/9oADAMBAAIAAwAAABDzzzjiXzzzzzzzzzT7HbPzzzzzzzzlrzzzzzzzzErPTzzzzzzwWs2FZ7zzzzzzyxHD/wA888888xetwc8888844pziVS68888888Cio0888888scU8AE88880K3DoVD60888888Yoc4488888888808888kcXuJz6G38888884M8scc88840888888888c88sGWb888w8888c8888488vIz888okMMM00888888888s0w84I88h8f885isw08IgIAsE8888888888AosA0g84K8t0857A0888In+Qs8888888888sKFNI088JYg0888E8888weIj888888888888v8JfI088M0888U40888U88888888888888888888UoX88kM88884Izc88888888888888888888/bY88888888GMQc08888888888888888884B7UQ88888884xEcc88888888888888888884U4888888888sE40888888888888888888888U08888888884IZzzzzzzzzzzzzzzzzz188ssE888888888883eo4BgwuQwM4k0N4cxK88888888888888888/wD/AP8A/wD/AP8A/wD/AP8Avf8A/wD/AM808440088888888888888888888888888888EUQc8g888888888888888888888888888888888888/8QAIxEBAQEAAgICAwADAQAAAAAAAREAITEwQBBBIFBRYGGRof/aAAgBAwEB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 align="left")

**Router:-**

* **WAN Device**
    
* **Networking Device**
    
* **Internetworking Device**
    
* **Maintain Routing Table**
    
* **Use Ip address for communication**
    
* **Send data in packet form**
    

**Layer - 7654 Device :- (Gateways)**

**Gateway:- Enter or Exit Point**

---

### **Lecture -6. Network Topology (Design of network)**

1. **Network Topology**
    
    1. **Physical Topology:- Actual Layout the Computer Cable**
        
    2. **Logical Topology:- the way actually devices communication internally**
        

**Types of Topology**

1. **Mesh**
    
2. **Bus**
    
3. **Ring**
    
4. **Tree**
    
5. **Hybrid**
    
6. **Star**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696185947949/ceb3ed62-a71e-4eaa-a3b5-111c97cabe74.png align="center")

---

### **Lecture -7. Types of Network**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>LAN</strong></p></td><td colspan="1" rowspan="1"><p><strong>Local Area Network</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>MAN</strong></p></td><td colspan="1" rowspan="1"><p><strong>Metropolitan Area Network</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>WAN</strong></p></td><td colspan="1" rowspan="1"><p><strong>Wide Area network</strong></p></td></tr></tbody></table>

---

### **Lecture -7. MAC Address**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>MAC -</strong></p></td><td colspan="1" rowspan="1"><p><strong>&nbsp;Media Access Control ---&gt;</strong></p></td><td colspan="1" rowspan="1"><p><strong>&nbsp;Mobile</strong></p></td></tr></tbody></table>

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Physical Address ---&gt;</strong></p></td><td colspan="1" rowspan="1"><p><strong>laptop/pc</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>BIA - Burnt in Address ---&gt;</strong></p></td><td colspan="1" rowspan="1"><p><strong>cisco router switch</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>NIC- Network Address Card</strong></p></td><td colspan="1" rowspan="1"><p><strong>Jitne nic card utne macaddress</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Mac Address</strong></p></td><td colspan="1" rowspan="1"><p><strong>48 bits</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Representation</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>43-Ab-53-23-54-23</strong></p></td><td colspan="1" rowspan="1"><p><strong>laptop</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>43:Ab:53:23:54:23</strong></p></td><td colspan="1" rowspan="1"><p><strong>mobile</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>43Ab:5323:5423</strong></p></td><td colspan="1" rowspan="1"><p><strong>Cisco Router</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>OUI = Organization Unique Identifier</strong></p></td><td colspan="1" rowspan="1"><p><strong>Given by IANA</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>IANA = Internet Assign Number Authority</strong></p></td><td colspan="1" rowspan="1"><p><strong>Internet Assigned number authority</strong></p></td></tr></tbody></table>

**<mark>MAC Address is globally unique</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Decimal</strong></p></td><td colspan="1" rowspan="1"><p><strong>Hexadecimal</strong></p></td><td colspan="1" rowspan="1"><p><strong>Binary</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0001</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>2</strong></p></td><td colspan="1" rowspan="1"><p><strong>2</strong></p></td><td colspan="1" rowspan="1"><p><strong>0010</strong></p></td></tr></tbody></table>

**<mark>Decimal Idea</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p><strong>8</strong></p></td><td colspan="1" rowspan="1"><p><strong>4</strong></p></td><td colspan="1" rowspan="1"><p><strong>2</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Value</strong></p></td><td colspan="1" rowspan="1"><p><strong>D</strong></p></td><td colspan="1" rowspan="1"><p><strong>E</strong></p></td><td colspan="1" rowspan="1"><p><strong>C</strong></p></td><td colspan="1" rowspan="1"><p><strong>ML</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>1-</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>2-</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>3-</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td></tr></tbody></table>

---

### **Lecture -7. IP Addressing**

**IP = Internet Protocol**

**Addressing**

* **Physical**
    
    * **MAC Address**
        
* **Logical**
    
    * **IPv4**
        
        * **Public**
            
        * **Private**
            
    * **IPv6**
        
        * **Public**
            
        * **Private**
            

**IPv4**

* **32 bit logical address**
    
* **4 octet = per octet 8 bits**
    
* **0-255**
    
* **Ip Address ---&gt; network id + Host Id**
    

* <table><tbody><tr><td colspan="1" rowspan="1" colwidth="200"><p><strong>192</strong></p></td><td colspan="1" rowspan="1"><p><strong>168</strong></p></td><td colspan="1" rowspan="1"><p><strong>45</strong></p></td><td colspan="1" rowspan="1"><p><strong>55</strong></p></td></tr></tbody></table>
    

**<mark>Classes</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Class A -</strong></p></td><td colspan="1" rowspan="1"><p><strong>1 - 126</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class B -</strong></p></td><td colspan="1" rowspan="1"><p><strong>128 - 191</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class C -</strong></p></td><td colspan="1" rowspan="1"><p><strong>192 - 223</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class E -</strong></p></td><td colspan="1" rowspan="1"><p><strong>240 - 255</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>127.0.0.0</strong></p></td><td colspan="1" rowspan="1"><p><strong>Loopback Reserved</strong></p></td></tr></tbody></table>

**<mark>Private IP</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Class A</strong></p></td><td colspan="1" rowspan="1"><p><strong>10.0.0.0-171</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class B</strong></p></td><td colspan="1" rowspan="1"><p><strong>172.16 , 172-31</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class C</strong></p></td><td colspan="1" rowspan="1"><p><strong>192.</strong></p></td></tr></tbody></table>

**<mark>Network id</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Class A</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class B</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Class C</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>N</strong></p></td><td colspan="1" rowspan="1"><p><strong>H</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Network Bit -1</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr></tbody></table>

**<mark>Example Network Id</mark>**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong><mark>Ip</mark></strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Class</mark></strong></p></td><td colspan="1" rowspan="1"><p><strong><mark>Network id</mark></strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>10.3.2.3</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class A</strong></p></td><td colspan="1" rowspan="1"><p><strong>10.0.0.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>120.0.0.0</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class A</strong></p></td><td colspan="1" rowspan="1"><p><strong>120.0.0.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>128.43.54.77</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class B</strong></p></td><td colspan="1" rowspan="1"><p><strong>128.43.0.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>188.64.94.3</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class B</strong></p></td><td colspan="1" rowspan="1"><p><strong>188.64.0.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>192.34.55.3</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class C</strong></p></td><td colspan="1" rowspan="1"><p><strong>192.34.55.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>221.34.43.23</strong></p></td><td colspan="1" rowspan="1"><p><strong>Class C</strong></p></td><td colspan="1" rowspan="1"><p><strong>221.34.43.0</strong></p></td></tr></tbody></table>

**Binary**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>128</strong></p></td><td colspan="1" rowspan="1"><p><strong>64</strong></p></td><td colspan="1" rowspan="1"><p><strong>32</strong></p></td><td colspan="1" rowspan="1"><p><strong>16</strong></p></td><td colspan="1" rowspan="1"><p><strong>8</strong></p></td><td colspan="1" rowspan="1"><p><strong>4</strong></p></td><td colspan="1" rowspan="1"><p><strong>2</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>Ip</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>192</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>168</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>20</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>0</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>1</strong></p></td><td colspan="1" rowspan="1"><p><strong>7</strong></p></td></tr></tbody></table>

**Question**

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Ip</strong></p></td><td colspan="1" rowspan="1"><p><strong>150.20.3.30</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Network Id</strong></p></td><td colspan="1" rowspan="1"><p><strong>150.20.0.0</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Broadcast Id</strong></p></td><td colspan="1" rowspan="1"><p><strong>150.20.255.255</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>No of Usage Host</strong></p></td><td colspan="1" rowspan="1"><p>216-2= 65535</p></td></tr></tbody></table>

### **Lecture -8. IPv4 Header**

**IPv4 header**

* **20 bytes**
    
* **Max 60 bytes**
    

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Version 4</strong></p></td><td colspan="1" rowspan="1"><p><strong>IHL 4</strong></p></td><td colspan="1" rowspan="1"><p><strong>TOS&nbsp; 8</strong></p></td><td colspan="1" rowspan="1"><p><strong>Total Length 16</strong></p></td></tr></tbody></table>

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Identifier</strong></p></td><td colspan="1" rowspan="1"><p><strong>Elags</strong></p></td><td colspan="1" rowspan="1"><p><strong>Fragments offset</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>TTL</strong></p></td><td colspan="1" rowspan="1"><p><strong>Protocol</strong></p></td><td colspan="1" rowspan="1"><p><strong>Checksome</strong></p></td></tr></tbody></table>

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Source Address</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Destination Address</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>option</strong></p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr></tbody></table>

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>Version -</strong></p></td><td colspan="1" rowspan="1"><p><strong>Version no of Internet Protocol</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>IHL -</strong></p></td><td colspan="1" rowspan="1"><p><strong>Internet Header length</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>TOS -</strong></p></td><td colspan="1" rowspan="1"><p><strong>Type of service</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Identifier -</strong></p></td><td colspan="1" rowspan="1"><p><strong>Exact position of the fragment but big lavel</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Flag -</strong></p></td><td colspan="1" rowspan="1"><p><strong>Fragment not</strong> <strong>Fragmented</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Fragment OFFSet</strong></p></td><td colspan="1" rowspan="1"><p><strong>Exact position of the fragment</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>TTL-</strong></p></td><td colspan="1" rowspan="1"><p><strong>Time to leave this is depend on router</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Protocol</strong></p></td><td colspan="1" rowspan="1"><p><strong>TCP/UDP</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><strong>Checksum</strong></p></td><td colspan="1" rowspan="1"><p><strong>Header check</strong></p></td></tr></tbody></table>

**Datagram - a** packet of data is called a datagram

**UDP -** User Datagram Protocol

**Ip Security**

* **IPsec is a group of protocol**
    
* **Use VPN**
    

---

### **Lecture -9. Subnetting**

**Subnetting:-**

* **A big network ko chote chote network me ch**
    

*  **The practice of dividing a network into two or more networks is called subnetting.**
    

* **Network within a network**
    
* **Logically division of ip address**
    

**CIDR-** Classless Inter-Domain Routing

### <mark>Questions:-</mark>

* **What is Hardware, Firmware, and Software?**
    
* **What is transmission mode?**
    
* **How many types of transmission modes in a computer network?**
    
* **What is the OSI Model ? - APSTNDP**
    
* **What is the TCP/IP Model?**
    
* **What are network Devices?**
    
* **What is networking and Internetworking?**
    
* **What is Gateways?**
    
* **What is Topology?**
    
* **Types of Topology? -  MBRTHS**
    
* **How many types of Networks?**
    
* **What is MAC Address?**
    
* **Find the Decimal Value of 1-10.**
    
* **IP address?**
    
* **Class of IP?**
    
* **What is Subnetting**