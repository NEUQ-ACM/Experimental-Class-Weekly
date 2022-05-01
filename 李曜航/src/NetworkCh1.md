## 1.1 What Is the Internet? 

A nuts-and-bolts and a services description.

### 1.1.1 A Nuts-and-Bolts Description

Billions of connected computing **devices**: 

•  **hosts** (主机)= end systems (端系统)

•  running network **apps** (应用) at Internet's "edge" (边缘)

**Packet switches** (分组交换机) : forward packets (分组) (chunks of data)

•  routers (路由器) , switches (交换机)

**Communication links** (通信链路)

•  fiber (光纤) , copper (铜) , radio (无线电) , satellite (卫星) 

•  transmission rate (传输速率): bandwidth (带宽) 

**Networks**

•  collection of devices, routers, links: managed by an organization 

**Internet**: "network of networks", consisted by many networks

•  Interconnected ISPs (Internet Service Providers, 中国电信中国移动中国联通。。。)

**Protocols** are everywhere

•  control sending, receiving of messages (报文)

•  e.g., HTTP (Web), streaming video, Skype, TCP, IP, WiFi, 4G, Ethernet

**Internet standards**

•  RFC: Request for Comments (请求评论) (有疑问)

•  IETF: Internet Engineering Task Force (因特网工程任务组)

### 1.1.2 A Services Description

**Infrastructure**(基础设施) that provides services to applications:

•  Web, streaming video, multimedia teleconferencing, email, games, e-commerce, social media, inter-connected appliances, …

provides **programming interface** to distributed applications (分布式应用程序):

•  "hooks" allowing sending/receiving apps to "connect" to, use Internet transport service

•  provides service options, analogous相似 to postal service

### 1.1.3 What Is a Protocol?

  **Network protocols:**

•  all communication activity in Internet governed by protocols

  **Protocols (协议)** define the **format**, **order** of **messages sent and received** among network entities, and **actions taken** on message transmission, receipt

## 1.2 The Network Edge

Access networks, physical media

##### A closer look at Internet structure

**Network edge (网络边缘) :**

•  hosts (主机): clients and servers

•  servers often in data centers (数据中心)

**Access networks (接入网), physical media (物理媒体):**

•  wired, wireless communication links 

**Network core (网络核心)** : 

•  interconnected routers

•  network of networks

### 1.2.1 Access Networks

##### Cable-based Access

**Frequency division multiplexing (FDM, 频分复用)**: different channels transmitted in different frequency bands

**HFC: hybrid fiber coax (混合光纤同轴)**

•  asymmetric: up to 40 Mbps – 1.2 Gbps downstream transmission rate, 30-100 Mbps upstream transmission rate非对称：中国大概是这种，上传速度更慢

  **network** of cable, fiber attaches homes to ISP router

•  homes **share access network** to cable headend

##### Digital Subscriber Line (DSL, 数字用户线)

Use **existing** telephone line to central office DSLAM (digital subscriber line access multiplexer, 数字用户线接入复用器) 太老了，不是我能接触到的东西。。。B站上的视频看到过那种拨号的奇怪声音

•  data over DSL phone line goes to Internet

•  voice over DSL phone line goes to telephone net

•  24-52 Mbps dedicated downstream transmission rate 

•  3.5-16 Mbps dedicated upstream transmission rate

##### Home Networks

•  Shared wireless access network connects end system to router

•  via base station (基站) aka "access point" (接入点) （不太懂）

##### Data Center Networks

high-bandwidth links (10s to 100s Gbps) connect hundreds to thousands of servers together, and to Internet

**Host: sends packets of data**

host sending function:

•  takes application message

•  breaks into smaller chunks, known as **packets**, of length ***L\*** bits

•  transmits packet into access network at **transmission rate \*R\***

•  link transmission rate, aka link **capacity, aka link bandwidth**

packet transmission delay = time needed to transmit *L*-bit packet into link = *L* (bits) /*R* (bits/sec)