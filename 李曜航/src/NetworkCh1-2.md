### 1.2.2 Physical Media

**bit**: propagates (传播) between transmitter/receiver (发射器—接收器) pairs

**physical link**: what lies between transmitter & receiver

**guided media (导引型媒体)**: 

•  signals propagate传输 in solid media: copper, fiber, coax

**unguided media (非导引型媒体)**: 

•  signals propagate freely (e.g., radio)

##### Twisted pair (TP, 双绞铜线)

two insulated (绝缘的) copper wires

•  Category 5: 100 Mbps, 1 Gbps Ethernet

•  Category 6: 10Gbps Ethernet

##### Coaxial cable (同轴电缆)

two concentric (同心的) copper conductors

bidirectional

broadband:

•  multiple frequency channels on cable

•  100's Mbps per channel

##### Fiber optic cable (光纤电缆) 
~~我只见过这个~~


glass fiber carrying light pulses, each pulse a bit

high-speed operation:

•  high-speed point-to-point transmission (10's-100's Gbps)

low error rate: 

•  repeaters spaced far apart 

•  immune to electromagnetic noise

##### Wireless radio

signal carried in various "bands" in electromagnetic spectrum

no physical "wire"

broadcast, "half-duplex" (半双工，sender to receiver)

propagation environment effects:

•  reflection 

•  obstruction by objects

•  interference/noise

Radio link types:

•  **Wireless LAN (WiFi)**

•  10-100's Mbps; 10's of meters

•  **wide-area** (e.g., 4G cellular)

•  10's Mbps over ~10 Km 

•  **Bluetooth**: cable replacement

•  short distances, limited rates

•  **terrestrial (陆地的) microwave**

•  point-to-point (点对点); 45 Mbps channels

•  **satellite**

•  up to 45 Mbps per channel

•  270 msec end-end delay



## 1.3 Network Core

Forwarding, routing; packet switching; circuit switching; a network of networks

##### The network core

Mesh (网状物) of interconnected routers (好像现在家里流行组mesh 可惜没有细说了)

**Packet-switching (分组交换)**: hosts break application-layer messages into **packets**

•  network **forwards** packets from one router to the next, across links on path from **source to destination**

##### Two key network-core functions

  **Forwarding (转发) :** 

•  aka "switching" (交换)

•  local action: move arriving packets from router's input link to appropriate router output link

  **Routing (路由):** 

•  **global** action: determine source-destination paths taken by packets

•  routing algorithms

### 1.3.1 Packet Switching

**Packet transmission delay (时延)**: takes *L*/*R* seconds to transmit (push out) *L*-bit packet into link at *R* bps

##### Store-and-Forward (存储转发) Transmission

**Store and forward**: entire packet must arrive at router before it can be transmitted on next link

**One-hop (跳) numerical example:**

•  *L* = 10 Kbits

•  *R* = 100 Mbps

•  one-hop transmission delay = 0.1 msec

##### Queuing Delays and Packet Loss

**Queueing** occurs when work arrives faster than it can be serviced

**Packet queuing and loss**: if arrival rate (in bps) to link exceeds transmission rate (bps) of link for some period of time:

•  packets will queue, waiting to be transmitted on output link 

•  packets can be dropped (lost) if memory (buffer) in router fills up