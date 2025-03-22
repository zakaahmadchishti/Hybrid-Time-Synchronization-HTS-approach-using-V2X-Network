# Hybrid Time Synchronization(HTS) approach using V2X Network
Time Synchronization using Flooding Time Synchronization(FTSP)

### February 2023
### Copyright © 2023 by Zaka Ahmed

All rights reserved. No part of this thesis may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, by any information storage and retrieval system without the prior written permission of the author. This is not an original version it's changed for public display.


### ABSTRACT

In wireless networks, time synchronization is crucial for basic communication as well as for the detection of movement, proximity, and position. Time synchronization means the distribution of time across clocks in a network. There are two types of time synchronization wire and wireless synchronization. In wired synchronization, we have a master clock which is connected with the child clock using an ethernet connection. On the other hand, instead of an ethernet cable between master and slave, a wireless connection is established between all devices.

In both wired and wireless networks, time synchronization is crucial. It enables effective
communication between network nodes. However, it is crucial for wireless networks in
particular. A TDMA(Time Division Multiple access) techniques can be used over a multi-hop
wireless network thanks to synchronization in the wireless nodes. Numerous uses of wireless
time synchronization exist, including those related to location, closeness, energy conservation,
and mobility, to name a few.

The common protocols include Time Stamp synchronization(TSS), Flooding Time
Synchronization(FTSP), Reference Broadcast Synchronization (RBS), Timing-Sync Protocol
for Sensor Networks (TPSN), and lightweight time synchronization (LTS) for Wireless Sensor
Networks. I have discussed all of these protocols for WSN.

When nodes in sensor networks are deployed, their precise location is unknown; as a result,
time synchronization is utilized to pinpoint their location. To establish the nodes' relative
closeness to one another, time-stamped messages will also be sent between them. Energy-
saving time synchronization enables the nodes to go to sleep for a predetermined amount of
time and then periodically wake up to receive beacon signals. Energy-efficient protocols are
required since a large number of wireless nodes are battery-powered. Finally, determining a
moving node's speed will be possible because of the common time between nodes.

I have proposed a hybrid technique which is a combination of FTSP and GNSS (Global
Navigation Satellite System). As FTSP is one of the most accurate solutions for time

synchronization. GNSS allows the WSN to receive time and location from satellites.
Remember GNSS and GPS refers to the same system, that uses signals from the satellite to
determine accurate location and time. FTSP is one of the most steady and robust protocols used
having a high synchronization precision for WSN.

There are a few common protocols for synchronization in the wired network including Network
Time Protocol (NTP), Precision Time Protocol (PTP), and Simple Network Time Protocol
(SNTP). As PTP is considered the most accurate whose error is in the few nanoseconds range
while the remaining NTP and SNTP are considered less accurate.

Particularly in wireless networks, the idea of time and time synchronization is essential. I have
discussed Wireless and Wire-time synchronization techniques. And classifying the importance
of time synchronization. I discussed the previous research conducted over time. There are a
few limitations in the implementation of various techniques. This thesis discusses the
importance of Time synchronization. And also discuss the implemented results and conclude
with the new approach which will increase the time precision in WSN.


## Contents

   - AUTHOR’S DECLARATION
   - PLAGIARISM UNDERTAKING
   - ACKNOWLEDGMENTS
   - ABSTRACT
   - Figure Contents
- Chapter 1...............................................................................................................................................
- Introduction............................................................................................................................................
   - 1.1. Introduction
   - 1.2. Research Contribution
   - 1.3. Problem Statement (Time Synchronization)
   - 1.4. Scope of the research
   - 1.5. Thesis Organization
- Chapter 2...............................................................................................................................................
- Background
   - 2.1. Background
   - 2.2. Modes of Operation
      - 2.2.1. Vehicle-to-Network(V2N)
      - 2.2.2. Vehicle-to-Pedestrian (V2P)
      - 2.2.3. Vehicle-to-Infrastructure (V2I)
      - 2.2.4. Vehicle to Vehicle (V2V)
   - 2.3. Sensor Networks (Wireless)
   - 2.4. Time Synchronization in Wireless Sensor Networks
   - 2.5. Wired Network Synchronization
- Chapter 3...............................................................................................................................................
- Related Work
   - 3.1. Vehicular Networks and Intelligent Transportation Systems
   - 3.2. Time Synchronization Approaches
      - 3.2.1. Time-stamp synchronisation (TSS)
      - 3.2.2. Flooding Time-Synchronization Protocol (FTSP)
      - 3.2.3. Time-stamping Multiple
      - 3.2.4. Reference-Broadcast Synchronization (RBS)
      - 3.2.5. Timing-Sync Protocol for Sensor Networks (TPSN)
      - 3.2.6. Lightweight Time Synchronization (LTS)
      - 3.2.7. Delay Measurement Time Synchronization Protocol (DMTS)
   - 3.3. Evaluation Criteria of WSN Synchronization
      - 3.3.1. Synchronization Precision.
      - 3.3.2. Accuracy
      - 3.3.3. Computational Complexity.
      - 3.3.4. Scalability
      - 3.3.5. Energy Efficiency
   - 3.4. FTSP in Recent Studies
- Chapter 4...............................................................................................................................................
- The Proposed Approach
   - 4.1. VANETS issue of Time Synchronization
      - 4.1.1. Receiver-to-receiver vs. Sender-to-receiver Synchronization
      - 4.1.2. Sender-to-receiver synchronization.
      - 4.1.3. Receiver-to-receiver synchronization.
   - 4.2. Master-to-slave vs. Peer-to-peer Synchronization
      - 4.2.1. Master-to-slave synchronization
      - 4.2.2. Peer-to-peer synchronization
   - 4.3. GPS Time Receiver and Time Transfer
      - 4.3.1. Solutions and Challenges in Absence of GNSS Signals
      - 4.3.2. Hybrid Time Synchronisation Prospects in Vehicular Networks
   - 4.4. GNSS and FTSP Synchronisation Challenges
   - 4.5. Summary
- Chapter 5...............................................................................................................................................
- Tool Support
   - 5.1. Current Implementation
   - 5.2. Complete FTSP Implementation
      - 5.2.1. Software Setup Omnet++
      - 5.3.2. Running the simulation
- Chapter 6...............................................................................................................................................
- Experiments and Results Analysis
   - 6.1. Primary and Hot-Standby Master Clocks
   - 6.2. One Master Clock
   - 6.3. Two Master Clocks Exploiting Network Redundancy
- Chapter 7...............................................................................................................................................
- Conclusion and Future Work.................................................................................................................
   - 7.1. Conclusion
   - 7.2. Future Work
- References

### Figure Contents
- Figure 1: Different types of V2X applications in 3GPP [1]. Figure Contents
- Figure 2: WSN Application [9]
- Figure 3: Radio Message Delay Sources [8]
- Figure 4: Wired Synchronized Network for School Clock
- Figure 5: Illustration of ITS System Concept.
- Figure 6: V2X Communication Infrastructure
- Figure 7:FTSP Packet
- Figure 8: Packet Format
- Figure 9: Time-Stamping Technique Multiple
- Figure 10: RBS (right) and traditional time synchronization protocols (left) Path Analysis
- Figure 11: Timing-Sync Protocol in wireless network
- Figure 12: Lightweight Time Synchronization
- Figure 13: VENET Communication Architecture
- Figure 14: Installation of Omnet++
- Figure 15: Setting-up Environmental Variables
- Figure 16: Configuring and Building OMNeT++
- Figure 17: Configuring and Building OMNeT++
- Figure 18: Verifying Installation OMNeT++ INET
- Figure 19: Lanucing Oment++ INET
- Figure 20: Sample Project Deployment
- Figure 21: Node Communication with Server in Oment++
- Figure 22: Topology of Two Master Clocks
- Figure 23: Settings for the clock nodes
- Figure 24: Switches Configration
- Figure 25: Configration of Devices
- Figure 26: Hot Standby and Primary master Clock difference
- Figure 27: Gptp message transmissions (Spanning tree Visualization)
- Figure 28: Hot-Standby Master synchronizing to the Primary
- Figure 29: Devices Synchronizing with the Primary Master
- Figure 30: Clock 2 Synchronization in time domain-1
- Figure 31: Topology of One Master Clock in Oment++
- Figure 32: Toplogy of One Master Clock Difference
- Figure 33: GPTP Application and Oscillator Clock
- Figure 34: Spanning tree direction of gPTP sync messages
- Figure 35: Clock time difference to simulation time
- Figure 36: Primary master clock in time domain
- Figure 37: All sensors are synchronized



## Chapter 1...............................................................................................................................................
## Introduction............................................................................................................................................


### 1.1. Introduction

At the start, I will discuss Vehicle-to-everything. V2X technology makes connectivity between
the road infrastructure and the vehicle. So, the infrastructure guide, the car about the obstacles,
and other objects. The main reason behind V2X communication is to increase traffic safety and
optimize traffic flow. There are various designed technologies for communication using
cellular and vehicular networks. Two modes of communication using the V2X network are
Cellular and Wireless communication. The radio technologies are connected to the vehicle
using the network infrastructure. Accidents are increasing continuously. The V2X network can
play a significant role in our world to increase people's safety. Time synchronization provides
a common time frame throughout all nodes. (F. Sivrikaya, 26 July 2004) Time synchronization
is critical for sharing location and warning Widgets for different applications specific to road
safety that’s why in an Ad-hoc network Timesharing is done between automated and connected
vehicles. For great communication networks, many techniques of synchronization have been
developed. I will try to explain the Practical implementation and theory of time synchronization
in VANETs.

In the recent few years, most of the applications are moved from wired systems to wireless
systems. This transformation is mostly a result of the several benefits wireless communication
provides, including adaptability and scalability. These characteristics enable node deployment
in locations that may be challenging for mankind to access, as well as make it simple to add
and remove end nodes. WSNs (Wireless Sensor Networks) are utilized for a variety of
purposes, the majority of which put the sensor nodes on moving elements to take advantage of
the network's mobility. While many alternative network configurations may be created in
wireless sensor networks thanks to this ad hoc structure, there are also additional difficulties.

When time-stamp precision is important, it might be challenging to give accurate timing
information due to the unpredictable type of wireless channel. To determine the precise
moment, received or sends by the sensor to determine the present time of the rest of the
network, time synchronization is utilized (Khondokar Fida Hasan, October 2018). The
necessity for time synchronization is large because data accuracy in most WSN applications


depends on the time-stamp assigned to it. In time Synchronization receiver node determines
the correct time using the input signal. Or we can say that Synchronization allows the nodes to
share time with the neighbor node or correct their time using the parent time. I am going to use
a hybrid approach for time synchronization which is a combination of FTSP and GNSS. The
complete approach is discussed in chapter 4. And the comparison Results are discussed in
Chapter 6. More specifically, a synchronization protocol is required to guarantee that packets
arrive on time and with the correct time stamps. Algorithms known as synchronization
protocols make an effort to close the time gap between when a packet was transmitted and
when it was received. To do this computation, choose a sent or received time estimate that is
close to the other.

### 1.2. Research Contribution

In communication, Time synchronization provides a framework between various nodes and
also supports different network features such as resource-sharing channels, scheduling message
transmission, and correct format in the real-time network.

Time synchronization is critical for sharing location and warning Widgets for different safety
apps that’s why in an Ad-hoc network Timesharing is done between automated and connected
vehicles. For great communication networks, many techniques of synchronization have been
developed. I have explained the theoretical thinking and practical implementation of VANETs
(Vehicular Ad Hoc Network) time synchronization And also try to explain the key factors in
VANETs Such as Precision analysis scalability, and availability, and highlighted the pros and
cons of the Global navigation satellite system (GNSS).

In our real world, we have various types of clocks which we use throughout the day, these
clock includes mechanical clocks, atomic clocks, and electric clocks. The second name of
Quartz clocks is electrical clocks, the main phenomenon behind quartz clocks is to count the
oscillation of vibrating quartz crystals.[3] This system is used in most of our daily life watches
and clocks as well as in communication and computer networks.


As the manufacturing typically in quartz clocks, there is a time error rate of nearly a few
seconds every week whereas else in quartz clocks which are low-cost, the time error may be
more than one second per day so overall. Nearly six minutes per year so we need to understand
high accuracy is possible at a higher price date is a crucial role in oscillator stability is also
included especially when the temperature is continuously changing. The timekeeping
component of an atomic clock uses the electromagnetic spectrum of an atom as a reference for
frequency.

Atomic clocks are expensive for communication and computers because their time is accurate
and frequency is also standard. That’s five for maintaining the time synchronization it is
important to keep the quartz clock time-synchronized with all of the communication network
nodes.

As time is one of the important information for logging information and delivery of packets on
time. As two devices can have a time difference or two sensors can have a time difference. This
difference affects the communication between both devices. Suppose two cars are approaching
a pedestrian as soon as the first car detects the pedestrian on road it will notify the other car.
But due to the time difference in both cars. The second car receives the message with a time
difference of 10 Second. So we need to understand that this 10-second difference can cause a
collision. So these vehicles must be synchronized with each other.

For wireless communication networks, time synchronization is always a challenge especially
when the network is decentralized means there is no central administrator which will control
the particular ad_hoc network. As we know vehicles are always traveling on the road drive
time synchronization between these mobile devices or nodes is a challenge for the network
administrator that’s why VANETs When are being progressed by applying the principle of
mobile ad-hoc Network two-vehicle VANETs have unique features Search as time-sensitive
applications dynamic topology and hybrid network architecture.

This thesis makes a significant addition to the field of wireless sensor networks. The lack of
awareness of this issue is the main motivation for this thesis. Furthermore, studies have


demonstrated that the outcomes presented, in the initial FTSP(2004) publication are nowadays
in use and utilized as a standard for novel and incoming synchronization protocols. Future
researchers will be able to use this work's new implementation as the FTSP's new benchmark.
To reach the most nominal accuracy of micro-seconds, this thesis addresses and fixes technical
faults in the current system. When dealing with Wireless Sensor Networks that require the most
nominal precision, researchers will now have access to a fully functional FTSP implementation
with simple reproducible findings. The extensive research done for this thesis on the
challenging time synchronization problem enhances the worth of the effort done to reach a
wider audience.

Finding time synchronization techniques for remote networks is a well-researched issue with a
long history of advancements. Additionally, GNSS-supported solutions have been suggested
for the root server in several indoor-based networks as well as for a variety of applications in
numerous outdoor-based networks. However, the creation of a comprehensive GNSS time
synchronization solution for automotive networks has been motivated by the outside nature of
vehicular networks, their distinctive topologies, and recent advancements in GNSS systems.
Below is a description of this thesis's specific contributions to research.

1. This thesis develops crucial knowledge regarding time synchronization issues in-
    vehicular networks.
2. It is suggested to use GNSS timing services for time synchronization in distributed
    vehicle networks to achieve accurate and precise time. This required carrying out a
    comprehensive feasibility study of GNSS time synchronization.
3. Integrating a GNSS receiver with onboard communicators and running experiments in
    urban settings serve to validate the proposed GNSS time synchronization. Discuss a
    demonstration of GNSS time synchronization with a functioning on-board node.
4. Deployment of FTSP and GNSS for achieving high accuracy of time synchronization.
    As FTSP offers can provide a time accuracy of 1.5 μs as well as GNSS also provide an
    efficiency of less than 40ns. So, If both protocols enhanced the precision of WSN.


5. Comparison of Wireless and Wired Protocols. PTP is considered one of the most
    accurate whose error is in the few nanoseconds range while the remaining NTP and
    SNTP are considered less accurate. And finally, I have concluded with my opinions and
    discussed the future work which can be done in the upcoming time.

### 1.3. Problem Statement (Time Synchronization)

The clock Synchronization topic always arises with independent clocks. After the first
initialization, real clocks will defer after some amount of time. As various problems arise due
to slight drift in clock time. So for avoiding this clock difference synchronization is important.
There are various approaches available to keep the nodes synchronized with each other. The
GPS was designed to address this problem for wired networks by giving nodes precise position
and time information. However, it was discovered that the system was inefficient with power
and not generally accessible, which inspired the creation of software-based time
synchronization protocols like NTP (Network Time Protocol)[15]. By making a single request
to the kernel, these protocols will guarantee that tasks are in the correct order and that processes
are time-stamped. This process establishes that every sensor in the network receives its time
from the same clock, removing any uncertainty that would otherwise exist in wireless networks.
When GPS and FTSP were used together, wired networks had excellent time synchronization
with results in the range of a few microseconds [16]. The time synchronization problem cannot
be solved in the same way again because of the characteristics of WSN. The development of a
solution particular to WSNs is necessary due to the restricted hardware and computational
capabilities of wireless sensor networks as well as the network unpredictability generated by
the wireless channel [17]. An additional complication is imposed by the features of wireless
sensor nodes as independent devices. Each node has its physical clock, CPU, and set of sensors.
It is challenging to select a common time because of this setup's unpredictable volatility [18].
Thus, time-synchronization methods are created to reduce the inaccuracy brought on by these
uncertainties. The various synchronization techniques will be explained in the next section
along with how they help wireless sensor networks become less unpredictable.


### 1.4. Scope of the research

Clock synchronization can be classified based on the various methods and applications for
example absolute clock synchronization is a standard referral clock that is considered absolute
for maintaining the system time synchronized relative clock synchronization is between the
nodes when two notes or multiple nodes are synchronized with each other concerning time.

We can categorize time synchronization based on different synchronization protocols. Time
synchronization protocols Resemble each other or differ from one another based on some
aspects. A time reference system is the furthermost prevalent way of categorizing the
synchronization method. A distributed network of blocks is categorized into two various
categories of synchronization external time scaling and internal time scaling synchronization.

In ad-hoc networks, VANET and Wireless sensors Network (WSNs) internal constraint time
scale can be implemented in time synchronization that’s why external time scale global time
synchronization can be deployed. Internal time scale synchronization can be defined as it is a
set of messages or operations which exchange between two or multiple nodes.

The common way of implementing is external time scale method is to take a reference time
standard search as UTC which will be a synchronized search external time reference will be
transmitted using a specific Global Radio system including Satellite-based GNSS and
shortwave WWVB Station.

The proposed method will help VANET in synchronization. The proposed method is composed
of FTSP and GNSS which will empower vehicles or WSNs to synchronize time and exchange
information with minimal difference. This thesis scope is not limited to wireless protocols but
also wired protocols are discussed. Synchronization also improves the response time for data
requests.


### 1.5. Thesis Organization

The process used to develop a workable implementation of the FTSP (Flooding Time
Synchronization Protocol) is demonstrated in this thesis. The main focus of this research is to
represent the importance of Time Synchronization in WSNs or VANETs. I explain the key
factors in VANETs Such as Precision analysis scalability, and availability, and highlight the
pros of the Global navigation satellite system (GNSS). For this implementation, the original
FTSP work by Levente Mészáros. [2] forms the foundation. When the available code was
examined, it became clear that the implementation [3] and the features of the FTSP described
in the original study needed a clear demonstration. Background information on the requirement
for synchronization protocols and the current WSN protocols is provided in Chapter 2. The
flooding time synchronization protocol is one of the most common protocols of
synchronization for WSN that are covered in Section 2.2.2 and FTSP in Section 2.2.6. Finally,
a defense of the existing implementation's integrity [3] is offered, supported by several recent
research. The current implementation [3] is described in Chapter 3, along with the areas where
it falls short. A fully operational gPTP solution with a thorough explanation of the alterations
made is also included in Chapter 3. The study is concluded in Chapter 5 after Chapter 4
compares the outcomes and future work[2]. The sending party embeds its own time as the
global time in the flooding time synchronization protocol (FTSP), for instance, and the
receiving party uses the received time as the local time. The protocol tries to develop an
estimated global time from the available local time.


## Chapter 2...............................................................................................................................................

## Background


### 2.1. Background

Nowadays, Autonomous driving is rapidly growing and providing us with a smooth driving
experience. A high number of corporates are focusing on communication and Manufacturing
technologies that will be deployed in autonomous cars for a long way. The scale ranges from
0 to 5 used for measuring the autonomous level in table 2.1. This scaling was introduced by
the Society of Automotive Engineering (SAE) [1]. The below tables 2.1 shows the scale of the
range of autonomous levels in vehicles.

```
Level Name Fallback When Automation fails
5 Fully Automated Driving Automated system
4 High Driving Automation Automated system
3 Conditional Driving Automation Driver
2 Partial Driving Automation Driver
1 Driving Assistance Driver
0 No Automation in Driving Driver
Table 1: Autonomous Driving Level [1].
```
Many engineers believe achieving Level 4 and Level 5 would not be possible before 2025[2].
In the last few years, the demand for autonomous cars is increasing terribly. Normally
Nowadays we see Level 2 and Level 3 autonomous cars on road. These Partially autonomous
cars required drivers to take control in case of imitated decisions. These cars are trained for
talking in limited real-time situations. This is also considered that if the driver does not take
control, the vehicle will lead to an accident [3][4]. Corporates are increasing the number of
sensors including Radar/LiDAR, IP Cameras, and Advanced Driver Assistance systems
(ADAS) on autonomous vehicles. These sensor data help the autonomous vehicle to make a
decision. The sensors are imported for vehicles but there are chances that these sensors will be
affected by poor light and bad weather. For increasing safety in levels 3 and level 4, it is
necessary to make connectivity more reliable. It’s time that now vehicles need to communicate


with each other for decreasing the number of Accidents. The cooperative C-V2X systems are
known as V2N (vehicle-to-network), V2P (vehicle-to-pedestrian), vehicle-to-infrastructure
(V2I), and V2V (vehicle-to-vehicle) Communication. C-V2X allows communication vehicles
with the infrastructure, Pedestrians, and other vehicles to improve road safety and also help in
case of sensor failure.

For sending a message to all RSU. V2X platform or MEC used. Using PC5 interface. The RSU
broadcast the message to the vehicle. For sending a message to the network areas you might
use the uU interface.

The main reason behind V2X is related to Traffic Efficiency, Road safety, As well as efficient
use of energy. Several estimates By the US NHTSA. If the V2X network has been
implemented. There will be a reduction of nearly 13% in road accidents. Underlined two major
types are WLAN-based and second one is Cellular based.

Programs like the Japanese CACS and the US Electronic Road Guidance System (ERGS) have
been working on V2V interaction projects to improve safety, minimize accidents, and provide
driver assistance since the 1970s. Japan, Europe, the United States, and are responsible for the
majority of steps in the history of automobile networks.

WLAN-based V2X systems have more standardization than cellular-based V2X systems. In
2010, the IEEE issued the WLAN-based V2X (IEEE 802.11p) specification for the first time.
It enables vehicle-to-infrastructure (V2I) and vehicle-to-vehicle (V2V) communication.
Dedicated Short Range Communication (DSRC) is the name given to this technology (DSRC).
The primary radio connectivity offered by 802.11p is used by DSRC. Next, I will discuss the
modes of Operations.

### 2.2. Modes of Operation

There are four various modes to deploy V2X. It includes Vehicle-to-Infrastructure(V2I),
Vehicle-to-Vehicle Communication (V2V), Vehicle-to-Pedestrian (V2P) and Vehicle-to-
Network(V2N) [8]. These Modes collect data from surrounding sensors, which help
autonomous vehicles move safely.


These four modes are discussed below:

#### 2.2.1. Vehicle-to-Network(V2N)

Vehicle-to-Network is a network transmission between the V2X application server and the
Vehicle. The parties like Vehicle-to-Vehicle communicate with each other using Evolved
Packet Switching (EPS) and Vehicle-to Network communicates with the application server
using the Vehicle network Application as shown in Fig 1.

```
Figure 1: Different types of V2X applications in 3GPP [1].
```
Different Operation scenarios and application services required Vehicle-to-infrastructure
services. This will help the Operators reduce cost, and time to market and eliminate the
complexity of design reliability is crucial but doesn't need to be precise. Due to the Vehicle to
network, Vehicles can communicate with the Vehicle to the infrastructure management system.
As this network is only used as a back, Being precise is not a requirement. For interacting with
road Infrastructure and with other vehicles dedicated short-range communication (DSRC) is
used which means the objective is to keep nearby connectivity active. The vehicle reacts as a
device or we can say that it is considered a device similar to wearable devices, tablets, and
smartphones. The network allows Vehicles to use any mobile network such as 5G, LTE, or
DSRC system. V2N help Vehicle receives real-time updates regarding road condition,
Weather, etc. or we can say that it allows connectivity with Vehicle to Infrastructure(V2I)


direct communication. Communication with surrounding vehicles is also possible using V2N
or using direct communication known as V2V. V2N also provides connectivity with the data
center and devices connected to the cloud. V2N allow vehicles to interact with infrastructure
like pedestrian, Cars, Poles, etc. using DSPC, LTE, or 5G connectivity.

#### 2.2.2. Vehicle-to-Pedestrian (V2P)

This is the new subcategory of the Vehicle-to-Infrastructure Ecosystem. This communication
has occurred between vehicles and Valuable Road Users(VRUs) like bicycles, pedestrians, etc.
VRUs carried UEs which will allow pedestrians to receive and send messages or alerts. This
system will allow vehicles to remain in touch with VRUs in low visibility (like in the rain,
Foggy weather, and night) and especially when there is no line of sight(NLOS). Due to battery
and antenna, the sensitivity of pedestrian UEs is lower as compared to Vehicular UEs. That’s
the reason that vehicle-to-pedestrian UE cannot continue transmitting messages like V2V.
Other technologies like Vehicle-to-Infrastructure and Vehicle-to-Vehicle involve road and car
communication with each other. In a few cases like Strollers, Bicycles, and wheelchairs smart
sensors are used to send alerts or awareness of objects.[6] Whereas dealing with pedestrians,
especially with children playing in the streets is different from the above scenarios. Various
car manufacturers like Telsa, and BMW uses 360 cameras, LiDAR technology, or blind spot
warnings for the detection of human. So, these approaches are not far-reliable. Maybe in the
future mobile devices will help vehicles to aware of possible collisions.

#### 2.2.3. Vehicle-to-Infrastructure (V2I)

Locally available servers or Remote switching units (RSU) are used for sending information
about V2I. Remote Switching stations are the receiver that can be allocated alongside the road.
Remote Switching Station receives the broadcasting message and then sends it one by one to
specific UE’s that support the V2I application.[7] Vehicle-to-Infrastructure helps users with
information regarding Road congestion, Parking space, Availability, etc. But also there are


demerits of V2I especially lengthy deployment time and High cost. V2I is a bidirectional
connection in which there is connectivity between road infrastructure and the vehicle. V2I data
includes information from roadside infrastructure (Traffic lights, Cameras, Road Signs,
Parking Meters), etc. This exchange of information is done using Short-range Communication
(DSRC) and Cellular network frequencies. The purpose behind V2I is to enhance road safety
and to gather real-time data from the road for avoiding road accidents. However, V2I is the key
feature of Autonomous Vehicles and it will help to enhance the safety of these vehicles.

#### 2.2.4. Vehicle to Vehicle (V2V)

This communication network allows vehicles to communicate and exchange data in real-time
with each other. In V2V short-Range communication frequencies are used which is the same
as in V2I communication. V2V virtually makes a mesh network that exchanges data with each
other. This mesh network help devices make a decision and exchange information using these
mesh nodes. Each Vehicle becomes a node that will transmit, receive and capture the signals.[5]
The exchange of information is not possible without subscribing to a specific network and then
gaining authorization for it. V2V exchanges application data like the location of the vehicle,
Vehicle attributes, Vehicle speed, direction, etc. As V2V is also a sub-category of V2X.
According to a report by NHTSA, V2V technology prevents more than 6 million accidents. So,
every vehicle can get information about the surrounding 300 meters using V2V
communication. This information also enhances the safety of vehicles.[9]

### 2.3. Sensor Networks (Wireless)

Development of technology, attention has increased on improving the wireless performance of
existing systems. Particularly, the majority of new applications are now built on top of wireless
sensor networks. As the name implies, a wireless sensor network is a group of sensors that are
deployed in numerous locations and can be either stationary or mobile and are connected via a
wireless medium. Wireless sensors have a wide range of uses, including autonomous house
networks, surveillance systems neighborhoods, army operations, and distant sensing [4]. They


are typically positioned in interesting regions where measurements will be made over time.
WSNs were initially employed to detect and transmit environmental physical data to monitor
particular conduct, such use in monitoring intelligent homes and greenhouses [5]. Lastly,
improvements in Wireless Sensor Networks made networks more complex. More WSN
applications are shown in Figure 2, including those for tracking and monitoring military targets,
disaster relief, biomedical tracking of one’s health device, behavior automation, tracking, and
exploring threatening environments.

Additionally, in recent developments, wireless sensor networks are being used to remotely
track a patient’s medical history by examining the patient's biological data [8]. WSNs are
primarily employed in the military to identify any threat or hazard, such as nuclear or chemical
strikes, and to warn the proper channels.

## Figure 2: WSN Application [9]

For the sake of national security, sensing might potentially take the method of spotting foreign
aircraft objects visually form of visual. When it comes to WSN employment in ordinary
catastrophes, they are mostly employed for forecasting reasons by keeping an eye on the
performing calculations performed on sensor inputs. This type of Wireless sensor network
application is frequently gathering information about specific ecosystems, detects earthquakes,
and monitors forest fires. Sensors that keep an eye on public spaces like malls and send out
notifications if the security is compromised are more frequent and regular uses of wireless


sensor networks. Some parking uses sensors to discover the empty parking spaces.
Interplanetary exploration and high-energy physics represent a more challenging yet extremely
valuable application of wireless sensors [10]. to carry out reporting and monitoring tasks. Since
the nodes are placed ad hoc in the field, this kind of WSN has the benefit of being expandable
in range. The option of sensor placement in difficult-to-reach places is made possible by node
mobility. However, this feature makes finding faults and troubleshooting more challenging.
Structured wireless sensor networks are arrangements of sensors that have been thought out in
advance. The number of nodes that may be used is restricted, even though this might lessen
uncertainty because access is easier and administrative costs are reduced [6].

Security of the network in WSNs is seriously threatened by the unreliability of the wireless
medium. Any nearby device can access the wireless communication channel because of its
susceptibility. Due to the absence of protection, a hacker might simply intercept the network's
transmission and make destructive alterations [13]. Last but not least, while the scalability of
WSNs is seen as a benefit, it also imposes certain requirements on the network that must be
met to actualize that attribute [14].”

Energy consumption is one of the major problems with wireless sensor networks. This problem
arises from the enormous number of activities that sensor nodes must continuously carry out
during their brief lifespan. Time synchronization, to make sure that all of the Nodes have the
same time, is another more contentious problem that comes up [11]. Timing is crucial because
of the nature of the actions taking place in a wireless sensor network. The timing at which the
data was received affects its usefulness and validity.

### 2.4. Time Synchronization in Wireless Sensor Networks

Although there are other ways to categorize synchronization protocols, for this study, their
key characteristics will be used. The following is a list of the most popular synchronization
protocol types:

“


 Internal synchronization vs external synchronization: The goal of the protocol is to
reduce the gap between the nodes as internal synchronization lacks a global time.
The nodes can utilize the same time, such as UTC, when external synchronization
is used [18].
 Deterministic synchronization vs Probabilistic: This is referring to how the clock
offset is calculated. When using probabilistic synchronization, the maximum clock
offset is determined using a promise with a known failure probability. The upper
and lower bounds for the clock offset will be predetermined for deterministic
synchronization protocols.
 R-to-R vs S-to-R synchronization: In addition to the propagation time, the sender
to the receiver will difference based delay on determine the delay based on the
difference in time-stamps between the sender and receiver. The time-stamps are
computed using the interval between the moments at which two receivers receive
identical messages [19].
 Un-tethered clocks vs Clock correction: The issue of clock drift arises because
nodes' hardware clocks and crystal oscillators have different properties. To deal
with this issue, some synchronization protocols will have a specific clock-
correction method.
 Peer-to-peer synchronization vs Master-slave: When all the other nodes
synchronize their clocks and times to the master node clock, this is known as
master-slave synchronization. Peer-to-peer synchronization enables nodes to
interact directly with one another, eliminating the possibility of the master node
failing.
 Non-MAC-layer-based approach vs MAC-layer-based approach: In order to
conduct time-synchronization, some synchronization protocols are MAC-layer
implementation and are closely related to the access strategy utilized. This makes
the synchronization protocols more accurate but non-modular. Although they won't


```
have the same accuracy as those that are at the MAC layer, that benefit of being
modular.
```
The types of mistakes that synchronization protocols help to reduce are what distinguish them
in addition to the previously mentioned characteristics. As seen in Figure 3, radio
communication delays are the primary cause of mistakes in wireless sensor networks. The
delays that have a substantial impact on radio message transmission. The common is
propogation delay.

## Figure 3: Radio Message Delay Sources [8]

Numerous techniques attempt to close this gap because accurate time synchronization is one
of the most contentious problems that wireless sensor networks encounter. Is followed by a
comparison utilizing the attributes stated in Section 3.2. In this chapter 3, each synchronization
protocol is described in more detail, and there is also a quick summary of the algorithms that
were employed. The Flooding Time Synchronization Protocol (FTSP) is then the subject of a
thorough analysis.


### 2.5. Wired Network Synchronization

There are two common methods of time synchronization named Global Positioning System
and Network Time protocol both are used for wired network time synchronization. As NTP
required a server with an atomic clock so, it will get an extremely accurate time. As the client-
server sent a UDP message containing a request for time information will be sent from the
client-server to the parent server. So, the server responds with the time information which will
be used by the client servers to get synchronized. The same goes for autonomous vehicles as it
is composed of various sensors and indicating devices that are interlinked with a wired network.
So these sensors and indicators need continuous synchronization. As we also need to keep in
mind that most of these devices are powered with batteries, especially the WSN-based devices.

As in GPS, we required a wireless device that will communicate with the satellite. As GPS
devices have a few limitations like a line of sight. As deploying a GPS receiver on all devices
is not possible or expensive. So we need to establish an interconnected device that is connected
using an ethernet cable. There are serval mechanisms the common ones are Precision Time
Protocol (PTP), Network Time Protocol (NTP), and Simple Network Time Protocols(SNTP).
As PTP is considered one of the most precise and accurate as compared to NTP and SNTP
protocols. NTP and SNTP are considered less accurate as compared to PTP. In wired systems,
the clock is utilized as a dual correction scheme that includes minutes and seconds
synchronization after every hour. So the clock will be synchronized after every specific time.

One common example is school clocks which are interconnected using wire, the reason behind
this is that the school bells will ring at rock-solid accuracy. As shown in fig 4. As this enables
the clock time will be the same in every class and the ring in every block will be rigged at the
same time without any limitations like availability, etc. As shown in fig 4. All clocks are
synchronized with each using the local time and the bell is also attached to that local time so,
the bell will be completely synchronized and ring according to the timing setting. This will


enable high accuracy for the whole school. The same applies to the vehicle inside the
infrastructure.

## Figure 4: Wired Synchronized Network for School Clock


## Chapter 3...............................................................................................................................................

## Related Work


### 3.1. Vehicular Networks and Intelligent Transportation Systems

In ITS, a variety of assisting systems and sensors are incorporated into cars to monitor their
immediate surroundings and provide them with correct information about their surroundings.
Kockelman and Fagnant (2015). As shown fig 5. Wireless connections enable information
sharing between automobiles and other road components in addition to this. As can be seen in
the Figure below, ITS support spans from Connected Vehicles (CV) to Autonomous Vehicles
(AV).

## Figure 5: Illustration of ITS System Concept.

A wide variety of sensors are built into autonomous cars to gather information about their
surroundings and allow them to function on their own. In fig 6, Drivers of connected cars (CV)
have wireless links to other nearby vehicles, infrastructure, people, and other objects nearby.
The capacity to obtain knowledge that might otherwise be out of the driver's immediate
awareness is wireless communications' main benefit. Exchange of critical information (such as
the direction of movement of neighbor cars, speed, location [Latitude, longitude], etc.) and
events that are critical for driver safety like (such as collision alerts and, lane changes, etc.),
these wireless connections would aid in the prevention of potential crashes. Such
communication would support transmitting traffic information, weather updates, and Internet-
based entertainment in addition to these safety warning messages.


Vehicle to Everything, or V2X communication, is the term used to refer to this varied roadside
communication. Figure 6, shows the concept of V2X communication.

## Figure 6: V2X Communication Infrastructure

Connected Vehicle (CV) is the support application of Vehicle to Everything (V2X)
communications, using two popular protocols: Dedicated Short-Range Communication
(DSRC) and Long Term Evolution (LTE). LTE-Vehicle is the name for how V2X
communications are implemented on LTE networks (LTE-V). This supports PC5, the direct
interface used by LTE, for V2V communications (also known as side-link).

### 3.2. Time Synchronization Approaches

In communication network, most of the time protocols are acceptable in wireless and wired
networks. For example, wired computer communications are adopted by network time
protocols (NTP). NTP is considered a backbone as can be implemented in wireless media. In
technologies improvement of performance is required.

Further, I will try to explain various synchronization techniques used over WSN. In mobile ad-
hoc wireless networks, There are various techniques of Wired and Wireless synchronization.


It includes Flooding time synchronization protocol (FTSP), Timing-sync protocol for sensor
network (TPSN), Lightweight time synchronization (LTS), Reference-Broadcast
synchronization (RBS), and Time-stamp synchronization (TSS).

#### 3.2.1. Time-stamp synchronisation (TSS)

The timestamp method is the most versatile generic synchronization approach. The method
involves tracking when each user lasts synchronized and using that information to control how
many rows are downloaded to each remote database. Each MobiLink user has a timestamp
value that indicates when they last downloaded data. The last download timestamp is the name
given to this item. Many events include a parameter for the last download timestamp, which
can be utilized in synchronization scripts. It is a WSN synchronization method and is used for
internal synchronization. To perform synchronization post-facto, it uses timestamps embedded
inside other packages.

The time offset is computed by calculating the round-trip delay from initialization till receiving
back means from transmitting till receiving. Nearly, 200 micro-seconds are considered as a
single hope WSNs average uncertainty whereas 3 micro-seconds (5 hops) are achieved in
multi-hop networks.

#### 3.2.2. Flooding Time-Synchronization Protocol (FTSP)

In wireless sensor networks, the flooding time synchronization protocol (FTSP) is an
expandable, stable, and reliable protocol with high synchronization precision. FTSP can be
used to easily implement synchronization in a mesh network by sending periodic broadcast
synchronization messages in competing timeslots. FTSP is a low-bandwidth protocol that is
resistant to link and node failures. The FTSP accomplishes its robustness by flooding
synchronization messages regularly and updating the topology implicitly. MAC-layer time-
stamp and complete error compensation, including clock skew estimation, are used to provide
the unique high accuracy performance. The sources of message transmission delays and
uncertainty are thoroughly examined, and solutions for mitigating their impacts are offered.


The FTSP is an RBS/TPSN hybrid time synchronization protocol. In FTSP, the root node,
which serves as the reference node is a time sender node, with the lowest node identity. In case
of a node failure, the root node is changed with the lower node as a reference node.
Synchronization messages are sent by root containing the reference time to the network
regularly. As a result, the entire network is synced. FTSP packet in Fig.7. The FTSP algorithm
is a self-organizing algorithm. To execute local clock correction and low-level time stamping
creates a hierarchy. The average error in an FTSP lab experiment with 8x8 grid is 1.7
microseconds, with a maximum of 38 microseconds per hop. The time required for an
electromagnetic wave to travel from sender to receiver is known as propagation delay. the time
it takes for a radio chip to convert a portion of a message to electromagnetic waves and to
decode.

## Figure 7:FTSP Packet

##### “

The sender-receiver protocol developed by Maroti et al. known as the FTSP, achieves
microsecond precision in multi-hop networks. Comparing it to well-know sensor network
protocols, FTSP is thought to have the highest level of precision and robustness. With an
average observed time synchronisation error of 1.48 s in a single-hop example, FTSP's
synchronisation precision exceeds that of all other synchronisation protocols mentioned, as
seen in Table 2. The ability of FTSP to establish a synchronisation point with just one broadcast
message and its promise to eliminate interrupt jitter using a variety of mechanisms, such as
multiple time-stamping, set it apart from competing protocols [2, 30]. It has also been utilised
for time synchronisation in a counter-sniper application [29].


A global-local time pair is created by flooding or broadcasting the synchronisation message to
all nodes, which includes the root's time, also known as the global time. The receiving node
then generates its own local time. Since the timestamp is included in the synchronisation
message, overhead is decreased by accomplishing time synchronisation using a single message
transfer. This historical difference is consequently known as the offset for that pair. The MAC
layer time stamping can prevent the majority of mistakes that occur during radio message
transmission; nonetheless, this protocol seeks to minimise interrupt handling time,
encoding/decoding delays, byte alignment and clock drift as additional causes of error.
Through the repeated time stamping technique discussed in the following section, both the
interrupt handling time and the encoding/decoding time are significantly decreased. As
described in the sections below, the SYNC bytes are used to determine the byte alignment time
and linear regression is applied to lessen clock drift.

#### 3.2.3. Time-stamping Multiple

FTSP attributes its micro-second precision, which is applied to both the sender and recipient.
After the SYNC bytes have been transmitted specified that additional time-stamps ( 6 in their
calculations) are to be taken at each byte boundary.. Below is a description of this process in
more depth. As shown in Figure 2.5, to minimise t1 to t6, select the smaller of each pair of
normalised time stamps, starting with t0 6 being equal to t6. According to Maroti et al., the
BYTE TIME is the amount of time needed to transmit a single byte and is calculated based on
the hardware's transfer rate. In Figure 8, the packets' format is depicted. The aforementioned
time stamps will then be reduced and averaged before being normalised by deducting a specific
delta from them that corresponds to the nominal byte transmission time.

## Figure 8: Packet Format


The 16bit in each sequence and that the Mica2 hardware being utilised has a transmission rate
of 38.4 kbps, this computes to a delta of 417 s [32]. Chapter 3 offers more information on this
problem.

## Figure 9: Time-Stamping Technique Multiple

#### 3.2.4. Reference-Broadcast Synchronization (RBS)

A reference message is transmitted in the RBS. When hearing the reference broadcast, the
receivers record their local time and exchange it with one another. The fundamental benefit of
RBS is that it reduces non-determinism on the transmitter side. The approach's downside is that
it requires additional message exchange to relay the nodes' local time-stamps. Only the
variation in propagation time between two receivers makes RBS sensitive. RBS is visible at
the left side of figure 10.

## Figure 10: RBS (right) and traditional time synchronization protocols (left) Path Analysis


For time synchronization, beacon Broadcast is used by RBS. In RBS, a Single-hop node
network can broadcast time reference by sending a beacon. RBS not contain unambiguous
time-stamps because it uses physical layer broadcasts. A node adjusts its clock by comparing
its local reference time to the master reference timings arrived from surrounding nodes. When
refreshing the clock, RBS makes both rate corrections and offsets. This synchronization occurs
across the entire network.

In muti-hope network, nodes are organized into groups. A solo beacon is utilized to make a
cluster node. This ensures that the offset and rate corrections are computed using the same
reference time. In fig 11, RBS reduces random access delay and hardware delay by using last-
minute time-stamps. To transfer timestamps from one cluster to another, a gateway node is
used. In laboratory tests with 30 broadcasts, the average uncertainty was determined at 11
microseconds. FTSP is also known as Hybrid Approach which is one of the best approach.

```
Figure 11: Accuracy (Errors) of time Sync Protocols
```

#### 3.2.5. Timing-Sync Protocol for Sensor Networks (TPSN)

TPSN is far superior to RBS. Because the average of the time discrepancies is used, using a
two-way handshake reduces uncertainty by half. Pairwise synchronization is executed at the
boundaries of the hierarchical structure defined earlier in the synchronization step. The TPSN
protocol is a hierarchical network-wide synchronization protocol. To establish a hierarchical
topology, it uses the traditional method of receiver-sender synchronization. Distinguish nodes
for doing actions, the hierarchy maintains many levels.

Time synchronization is accomplished by TPSN in two stages. The root node during 1st phase
is a node at level 0. It broadcast a 'level discovery' massage that includes its identification and
hierarchy level. The message is received by its immediate neighbors, who are assigned level 1
under the root node. Figure 12 shows, each node at level 1 broadcasts a 'level discovery'
message, which is received by lower-level neighbors. This procedure continues until such 'level
discovery' notifications reach all nodes. In the second phase, every node uses a round-trip
synchronization in the tree procedure to synchronize clocks with their parent nodes. The MAC
layer performs round-trip synchronization. As a result, message-delay uncertainties are greatly
reduced. TPSN has a very high level of accuracy. The TPSN synchronization achieved a
precision of 17 microseconds in experiments. The considerable message exchange overhead of
TPSN, especially for a large number of nodes, is a disadvantage.

## Figure 11: Timing-Sync Protocol in wireless network


#### 3.2.6. Lightweight Time Synchronization (LTS)

The communication accuracy and complexity of multi-hop synchronization are a function of
the spanning tree's structure and depth, according to LT synchronization for sensor networks.
This protocol describes several spanning-tree creation strategies. The goal of Lightweight Time
Synchronization (LTS) is to simplify the synchronization process. As a result, unlike other
synchronization systems, it allows for precise synchronization. It starts with the building as a
centralized algorithm with n nodes spanning trees. Following that, a pair-wise synchronization
is done sideways on the spanning tree's n 1 edges. The reference node is considered the root.
All on-demand resynchronization activities are started by it. In LTS, the average
synchronization error is 0.4 seconds. The maximum inaccuracy can be up to 0.5 seconds.

```
Figure 13: Lightweight Time Synchronization
```
#### 3.2.7. Delay Measurement Time Synchronization Protocol (DMTS)

With the help of this sender-receiver technique, a master node is chosen to send the identical
synchronisation message simultaneously to every receiver. Then, they will adjust their local
time such that it equals the global time plus the predicted delay. The computed delay will
account for some radio message faults, but the transmission time, receive/send times, and
access time-related delays still exist. All receivers will determine their own delays based on
the master's time, which is used as the global time. These two errors are addressed by this
protocol in the following ways:


```
 Transmission time: The transmission times are split into two independent times by
this protocol. Since the transmit rates for the data transmission time and the
transmission of the preamble/start symbols may differ. The delay is then estimated
using the transmission component speeds [24].
 Access time and Sender processing time: To eliminate the inaccuracy brought on by
those two delays, when the channel is found clear, the protocol will collect a time
stamp.
```
```
Table 2: Synchronization protocols Comparison
```
Protocol Clock

```
Correction
```
```
Standard / MAC
layer
```
```
Probabilistic/
Deterministic
```
```
Sync
Error
(μs)
```
Sichitiu and

Veerarittiphans

```
Yes MAC layer Deterministic 3000
```
Mock et Al Yes MAC layer Deterministic 300

Romer’s

protocol

```
No Standard Deterministic 200
```
DMTS No Standard Deterministic 32

FTSP Yes MAC layer Deterministic 1.48

TPSN Yes MAC layer^ Deterministic 16.9

RBS No Standard Deterministic 29.1


### 3.3. Evaluation Criteria of WSN Synchronization

The state-of-the-art wireless sensor network time synchronisation techniques are compared and
evaluated in this thesis. The criteria that will be employed in the following comparisons must
be thoroughly established before these treatments can be evaluated. The evaluation criteria are
broken down into five categories in this paper, including synchronisation accuracy,
computational complexity, scalability, and energy efficiency.

#### 3.3.1. Synchronization Precision.

Every sensor node has a hardware oscillator circuit-based physical clock. However, within a
given range, the actual clocks' frequency varies from one node to the next. In wireless sensor
networks, this means that various nodes' clocks run at various rates. Therefore, the clock values
utilised for time synchronisation in wireless sensor networks are not the readings from the real
clock. Network nodes often have a logical understanding of time, and logical clocks can be
altered by both hardware and software. As a result, there are two different definitions of
synchronisation precision.

```
 absolute accuracy the greatest possible discrepancy between a node's logical clock and
an outside clock, such UCT.
 Relative accuracy. The widest variation in wireless sensor network node nodes' logical
clock values.
```
In this debate, the aforementioned relative precision concept is typically applied. High
synchronisation precision is generally a desirable attribute for a synchronisation mechanism.
However, the protocols examined in this work are more complicated and have higher
synchronisation precision, more messages are sent between nodes, and more storage is needed
for the protocol.

#### 3.3.2. Accuracy

Regarding how closely the time is kept in the wireless sensor network to the standard time,
accuracy is a crucial metric. In other words, it serves as a gauge for the degree of time


synchronisation precision. Due to the fact that there are two alternative ways to define
synchronisation precision, a time synchronisation protocol that is very accurate also ensures
that it is highly precise.

#### 3.3.3. Computational Complexity.

Due to the limited hardware capabilities and various energy limits in wireless networks, the
complexity of a synchronisation protocol might render a protocol unworkable for many
applications. The message complexity of a protocol, such as the amount of messages sent
during time synchronisation, and the computational complexity of a protocol, such as in
relation to the memory needs, must be given appropriate consideration. Both a protocol's
memory needs and the number of nodes being synchronised are taken into account in this
evaluation.

#### 3.3.4. Scalability

The geographic range of the synchronised nodes defines the sensor network's scope. Generally
speaking, adding more sensor nodes to a sensor network will enable it to cover more ground.
Wireless sensor networks are expanding, and sensors are getting ever-cheaper. Tens of
thousands of sensor nodes make up a wireless sensor network. As a result, time synchronisation
methods need to be scalable enough in relation to the size of the network.

#### 3.3.5. Energy Efficiency

The majority of wireless sensor networks have a crucial requirement for energy efficiency,
which varies depending on the application. The energy required for time synchronisation and
other operations is constrained, for instance, in some cases where the energy efficiency
requirements for sensor networks are particularly severe. The size of the batteries in the sensor
nodes, which severely restricts the quantity of energy that can be consumed and stored, is the
primary cause of the energy limitation. Consideration must be given to a key trade-off for
wireless sensor networks, which has to do with how much energy is allocated to compute and
how much to communication.


For instance, FTSP has the highest level of precision, making it suitable for a variety of military
applications. Additionally, RBS can be used in some situations where great accuracy and
limited power are required because of its high accuracy, good scalability, and high energy
efficiency.

### 3.4. FTSP in Recent Studies

It was suggested in a recent study on synchronisation protocols that there is currently no
implementation that properly adheres to the FTSP criteria. New and forthcoming
synchronisation techniques are also still evaluating their effectiveness in comparison to the
numbers provided in the original FTSP study. One such synchronisation protocol is Glossy
[35], which aims to saturate the network with implicit time synchronisation. They used the
synchronisation error (measured in microseconds) found in Maroti et alpaper .'s to compare
their protocol to it without having to recreate the implementation.

On hardware like the Mica2, Thomas Kunz and Ereth MCKnight-MacNeil [38] built the clock
sampling mutual network synchronisation (CS-MNS) algorithm in TinyOS and evaluated its
performance in comparison to the FTSP in 2011. It was discovered that the FTSP performed
considerably worse than was previously claimed in the original publication. According to their
final findings, the final synchronisation error for the CS-MNS method was 31 s as opposed to
61 s for FTSP. The results were replicated by the authors of [39] using the TinyOS 2.x [3]
implementation, however they discovered that when they used the default parameter settings,
the available code FTSP was unable to synchronise the network's nodes. They change the code
to get outcomes that might be analogous to their own as a result of the implementation flaws
they have found. This variance in the FTSP code is a result of its flaws and may lead to various
adaptations of the protocol that may not accurately translate the FTSP algorithm. The FTSP
benchmark is used by the EBSP published in [40] to assess the effectiveness of the
synchronisation mechanism. TinyOS's implementation of the innovative time synchronisation
protocol described in [41] produced test results that were up to 40% more favourable than those


obtained using FTSP. The authors in [42] claim that their modifications to the protocol increase
battery life by lowering the amount of sent and received frames by 20% in an effort to enhance
the FTSP. Instead of using actual hardware, they tested using simulation using OMNeT++.
.Another synchronisation protocol established in 2011 is Average TimeSync (ATS) [36], which
likewise refers to FTSP as "the defacto standard for time synchronisation in WSN" and utilises
it as a benchmark. They have said that they tested 3x3 WSN synchronisation period of 60s, as
well as using the widely used FTSP TinyOS [37] implementation. The validity of the prior
comparison may be impacted because this study contends that the currently accessible web
code is not an accurate translation of the flooding time synchronisation methodology.

Since the following node won't now receive a synchronisation message from this node, which
is presently resetting and trying to re-establish synchronisation, it will declare itself the root
and so impair network performance. According to P.A. Sommer, the current implementation
fails to take into consideration errors that arise in this situation, which have been shown to be
harmful to the FTSP's accuracy. The authors had to fix the root to one particular node and
verify the protocol in order to make sure that this problem is not present in their
implementation. Following this change, an average one-hop synchronisation error of 9.04 s
was found. The correctness of the current FTSP implementation is impacted by a much-debated
issue, according to P.A. Sommer [43]. The FTSP nodes will always synchronise with the node
that is one level higher due to the nature of the synchronisation protocol, however there is
currently some potential for error due to the way the protocol was designed. If the discrepancy
between the calculated and actual received times is greater than a predetermined threshold, the
linear regression procedure would reset and this mistake would result.


## Chapter 4...............................................................................................................................................

## The Proposed Approach


### 4.1. VANETS issue of Time Synchronization

For getting constant data traffic and exchange of real-time messages time synchronization in a
wireless network is a major element, especially time synchronization is a major issue in
distributed network systems. As many network applications require accurate time
synchronization for making major decisions. In the context of telecommunication networks
and computers, the problem of time synchronization is deeply explored and various protocols
are defined. For example, Synchronization is required to guarantee the sequence of the order
in the packet over SONET.

Many protocols are implement in the area of time synchronization in the recent few years, these
protocols are various in terms of precision, type of network, and services. Considering an
example of a routed network, Physical time is not a big issue SDH Links (POS) required
synchronization to maintain the order of packets. Whereas the other side few networks required
synchronization with high time accuracy. For example, for SDH and SONET the precision of
time is required along with fixed time-division multiplexing is necessary.

In VANET, many applications required physical time to play an important role by satisfying
logical time and kind of event ordering models. Most tasks uses a time-of-day clock as
VANET, allowing traffic management, in which vehicle share information with road
infrastructure on an individual level like driving intentions and car dynamics. Whereas on the
other hand few nodes’ parameters required continuous time synchronization like speed,
position and other important values which change continuously. VANET provides various
critical safety applications which increase road safety like Emergency Electronic Brake Lights
(EEBL), Forward Collision Warning (FCW) and Cooperative collision Warning (CCW) are
a few common applications that can alert the driver before the collision. Remember, for the
usage of these applications, every vehicle is required to transmit a basic safety message (BSW)
at 10 Hz periodically. As, these alerts are time sensitive and we need to transmit this delay with
low time delay (typically 100ms). If the node clock in VANET has a common agreed time
stamp, this can cause many problems, maybe the alert is synced with a past timestamp in which
massage may reach after a collision or incident as well for other condition if the alert reaches


before time, it is also a bad impression and question on safety. In such conditions warning
massage does not help to avoid collisions. Therefore, Time synchronization in VANET is
essential to achieve precise time and accuracy over the network.

For efficient channel scheduling and proper bandwidth utilization, physical time is also crucial.
So, therefore, all nodes are required to report accurate time and the same time regardless of
network latency and errors in their clock. Also, a few security measures such as identifying
hijackers in session and duplication detection also required absolute time for detestation in
VANET. This clearly defines the importance of time synchronization between two nodes for
real-time communication and coordination in VANET.

## Figure 13: VENET Communication Architecture


#### 4.1.1. Receiver-to-receiver vs. Sender-to-receiver Synchronization

The majority of existing protocols broadcast the packet with local clock values as the
timestamps in order to synchronize a sender and a receiver. These techniques are therefore
quite susceptible to message delay. By leveraging the time that each receiver node receives the
identical message from a sender, some techniques, like RBS, synchronize the times of the
receivers. Such a technique can lessen the time-critical path, which is the path taken by the
message to help determine unclear protocol errors[8], [3].

#### 4.1.2. Sender-to-receiver synchronization.

This is the conventional method. Typically, there are three steps involved: Periodically, a
sender node delivers a message packet to the receiver nodes with the value of its local clock as
a timestamp. Then, either instantly or later, the receiver nodes synchronize themselves with the
sender node using the timestamps received from the sender. The total round-trip time—the
period of time between when a receiver node requests a timestamp and when it actually receives
the response—can be used to compute the message delay between the sender node and the
receiver nodes.

However, this approach has several clear drawbacks. The network latency and the workload
on each node cause a difference in message delay between the sender and the recipient nodes.
The majority of methods determine the average message delay after conducting numerous
experiments, during which they lose the accuracy of the time synchronization and also increase
network overhead. Additionally, it is important to optimise both the time it takes for the
recipient nodes to digest the message and the time it takes the sender node to prepare and send
the message.

#### 4.1.3. Receiver-to-receiver synchronization.

The physical broadcast media is used in this technique such that if two receiver nodes receive
the same message during a single-hop transmission, they do so virtually simultaneously. When


receiving the same message from the same sender node, receiver nodes do not communicate
with the sender node; instead, they exchange timestamps and use the difference in reception
time to determine their clock offset. The benefit of this approach is the decrease in message
delay variance. Only the propagation delay to the various receiver nodes and the variations in
reception time make this approach problematic.

### 4.2. Master-to-slave vs. Peer-to-peer Synchronization

#### 4.2.1. Master-to-slave synchronization

One node is chosen as the master in a master-to-slave protocol, while all other nodes in the
network are chosen as slaves. The slave nodes synchronise with the master and use the local
clock value of the master as their reference time.

#### 4.2.2. Peer-to-peer synchronization

The majority of protocols, including RBS, are peer-to-peer oriented. Any node in a peer-to-
peer network can communicate with every other node in the network directly. This eliminates
the master node failure's potential impact on the ability to accomplish time synchronisation.
Peer-to-peer synchronisation control, however, is more challenging.

### 4.3. GPS Time Receiver and Time Transfer

In this method, we suppose we have receive a one way signal contiously from two satations B
and A. We will meaure the time difference between the local time and receiving time. As
government of America introduced as ITC via a GPS signal in a space. Which is considered as
a accurate time. The difference can be expected less than 30 nanoseconds.

#### 4.3.1. Solutions and Challenges in Absence of GNSS Signals

Only the Line-of-Sight (LOS) wave propagation theory is used in the transmission of signals
between satellites and receivers. Driving across high-rise streets frequently results in
navigational failures. The loss of time synchronisation is not necessarily the result of this. First,


with a single satellite and with a decreased level of accuracy, GNSS time solutions can be
acquired. Valid time solution availability is substantially higher than valid position solution
availability. For instance, a car experiment demonstrates that over several Brisbane high-rise
streets, the percentage of valid GPS+Beidou position solutions is 99.25%, whereas the
percentage of at least one satellite is 100%. [2018b] Hasan et al.

Second, various actions have been suggested as backup plans in the event that GPS signals are
blocked. One of these is to use a GPS Disciplined Oscillator to transition from regular mode to
holdover mode (GPSDO). GPSDO is a firmware designed specifically for holdover mood. It
enables the internal oscillator to anticipate and replicate the GNSS system's initial time and
frequency. A phase detector and a voltage control oscillator make up the majority of a GPSDO
(VCO). Its main objective is to gather data from GNSS satellite signals in order to regulate the
frequency of nearby quartz or rubidium oscillators. Using the knowledge of its prior
performance, GPSDO maintains its oscillation in a constant frequency even when GPS signals
are not available.

During the holdover time, various techniques including adaptive temperature and age
adjustment have been developed in order to improve GPSDO's performance. Recursive linear
regression is the foundation of the adaptive temperature and age compensation. Simple
semiconductor ambient temperature sensors and an A/D converter are employed as extra
circuitry. Both forms of enhanced GPSDOs perform similarly, to a certain extent.

The execution time of the independent free-running GPSDOs is not well determined, though.
Nevertheless, tests have been done to see how well GPSDO performs. According to Elson et
al. [2002], ETSI [1–12], an experiment was conducted over the course of a week for holdover
on four GPSDOs, of which one oscillator is made of quartz and the other three are composed
of rubidium. The time difference from the quartz oscillator was determined to be 82 s after a
week. For the three rubidium oscillators, the best time offset performance of less than 3 s was
measured. For VANET time synchronisation applications, this degree of synchronisation
precision is regarded as acceptable.


Finally, by integrating GPS synchronisation with other techniques, the issue of GPS signal
blockages can be solved. If some vehicle nodes with satellite-viewing capabilities have GNSS
time solutions, they function as root servers for synchronising other nodes using a method other
than GPS. The foundation of universal computer networks is FTSP-GNSS, which synchronises
all nodes which required accurate time. For instance, the Automatic Identification System
(AIS) for ships Tetreault [2005] uses time synchronisation based on absolute GPS.

#### 4.3.2. Hybrid Time Synchronisation Prospects in Vehicular Networks

A well-known satellite-based communication system that offers users timing (PNT),
navigation, and positioning services is the Global Navigation Satellite System (GNSS). The
Global Positioning System (GPS) satellites were initially launched by the USA and now cover
the whole planet. Later, the independent communication services, timing, and positioning,
satellite-based navigation and of the Russian GLONASS, the Chinese BeiDou, and the
European Union's Galileo were joined. Table 1.1 provides information on the number of
satellites in the present [2018]. GPS now has 31 satellites in orbit, making it the single satellite
system with the most satellites. This number rises to 99 under the multi-GNSS idea, though,
and is predicted to reach 134 by the year 2023. This logically increases the likelihood of
consistently detecting satellite signals from a variety of satellites, which would aid in
supporting precise PNT services. The GNSS timing service is regarded as the global reference
source for timing. It is also recongnised as one of the most accurate UTC sources since GNSS-
based satellite time is maintained with exceptionally precise atomic clocks and satellite time
transfer is more dependable than other ground-based time-transfer technologies.

The timing reference point for the entire world is the GNSS timing service. It is also recognized
as one of the most accurate UTC sources since GNSS-based satellite time is maintained with
exceptionally precise atomic clocks and satellite time transfer is more dependable than other
ground-based time-transfer technologies. Any time transfer system's accuracy is compromised
by the uncertainty brought on by the various propagation path delays, and this is true for several


fundamental reasons. Path delays in satellite-based GNSS systems are easier to measure and
calibrate than in ground-based radio communication systems. This is due to the modest
variation in path delays and the large clear paths between the satellite and receiver.
Additionally, since they can be statistically modeled and adjusted for, signal interferences
brought on by the effect of the weather are typically less of an issue. Therefore, under a clear
sky, the time guidance provided by GNSS systems is precise and common.

The GPS or several GNSS receivers are already built into contemporary cars. Thus, accurate
time support from GNSS is possible without incurring any additional expenses. Although many
networks use GPS-based time synchronization, there are few articles describing how well these
systems perform in time synchronization. But the question arises in tunnels and places where
the GNSS signal doesn’t reach. The best and the most accurate protocol for those areas is FTSP.
As FTSP is one of the most steady and Robust protocols it has the highest precision in a wireless
networks. And FTSP is also robust against link and node failures and also uses low
communication bandwidth. But here we also need to discuss the FTSP, which is used for a
computer networks or we can say that for wired networks. FTSP offers accuracy within
nanoseconds. Implementation of FTSP is demonstrated in Chapter 6.

### 4.4. GNSS and FTSP Synchronisation Challenges

GNSS receivers come in a variety of manufacturing grades depending on the type of
application and price. A quartz oscillator and simple circuitry are frequently used in consumer-
grade receivers to keep costs down for use in everyday navigation applications. The majority
of the GNSS navigational systems found in automobiles are of the consumer-grade. It is critical
to comprehend what level of time synchronization accuracy they may provide given that they
employ cheap hardware. A synchronization technique known as TA, which depends on
message exchanges between nodes, is implemented inside an IEEE 1609.04 protocol stack that
underpins the IEEE 802.11p-based WAVE (Wireless Access for Vehicular Environment)
structure. The synchronization procedure is coordinated by a TSF (Time Synchronisation


Function) register found in the MAC. The TA scheme is represented diagrammatically in
Figure 1.3, with the moving station receiving and updating following the received time. The
TSF of the Access Point (AP) can maintain time and send out time through the communication
channel. Due to the extremely dynamic nature of vehicular situations, message-transfer-based
time synchronization is difficult since, at relative speeds of 200 km/h, the nodes may only be
in communication range for a very brief period. Investigating the chances of GNSS time
synchronization over such systems is crucial notwithstanding the difficulties with TA-based
solutions.

Additionally, GNSS signals can be interfered with by obstructions like trees, buildings, and
other structures, which can cause service interruptions. The majority of vehicular networks are
placed outdoors, where communications take place in the open air; however, in metropolitan
settings, obstacles like tall buildings, trees, and tunnels make it difficult to provide GNSS
services.

Well FTSP doesn't have any specific limitation as GNSS has, In FTSP when a node receives
sufficient timing messages, it becomes a master node and starts broadcasting timing messages
to other child nodes. As root nodes are elected or re-elected dynamically in case of failure this
ensures that the system is robust. The average error of FTSP is less than 3μs per hop.

### 4.5. Summary

In VANETs, both V2V and V2I communications are used. Network connectivity and numerous
applications related to road safety, serve as the foundation for VANETs. VANETs require
precise timing and accurate measurement of transmission delay because of their highly
dynamic and movable nature. Over VANETs, time synchronization aids in establishing an
agreed-upon time. It makes it possible for numerous events to be properly coordinated and
consistent across networks. Additionally, it enables precise sequencing and real-time
management of message transmissions through networks. The necessity of time


synchronization for VANETs has been covered in this chapter and I have presented a new
approach which is a combination of FTSP and GNSS.

As most techniques that are earth-driven always face delays and uncertainties. Whereas in
GNSS satellite-based time have a specific path delay that can be calculated. In satellite time
the delay is constant. As there is no obstacle in front of the satellite that’s why the variation in
path delay is predictable. Calculating the delay is straightforward to calibrate as compared to a
ground-based system. Also, bad weather and ground noise have less impact on radion satellite
communication. GNSS is used to synchronize, the root node outdoors. Using these nodes, other
nodes get synchronized. Technically saying, it is a message exchange between nodes. Our
approach is the use of FTSP and GNSS signals for time synchronization. This means this will
be the hybrid approach in which FTSP and GNSS are used. Hear in tunnels, VANETs need to
use FTSP for synchronization. GNSS follows the principle of velocity, position, and time
computing for estimation.


## Chapter 5...............................................................................................................................................

## Tool Support


### 5.1. Current Implementation

As there are very few implementations currently available that discuss time synchronization.
The only implementation available is considered as an official code for the flooding time
Synchronization Protocol, which is open source and available on GitHub [3].

### 5.2. Complete FTSP Implementation

The current Operating system is MACOS. So, the step starts with setting up Omnet++ which
is used for deploying the FTSP.

#### 5.2.1. Software Setup Omnet++

Omnet++ is one of the famous network simulator whose simulation library is build in C++
modular based. It is one of the non commerical simulator used for research and acedemia. The
module offer plenty of modules the famous one is INET which has the network protocols like
BGP, Ipv6 etc. The Software is supported on all platforms like linux, MACOS and Windows.
As I am going to use my MAC for this installation and implementation. And also this is
important that the laptop I am using is powered by SiliconChip (Apple Processor M1) instead
of Intel-based Processor.

Step 1: Development Mode Enabling
Unsigned code cannot be executed by MacOS due to its rigorous default security policy. You
must specifically permit running unsigned code from a Terminal because this behavior
frequently obstructs the development process. To override the Terminal app's default security
policy, click Development Tools on the left side of the screen, unlock the panel with the lock
icon in the bottom left corner, and choose the Terminal app on the right side.

Step 2: Unsigned Code Debugging
Because the debugged process is launched by the IDE, not the terminal, missing code
signatures will still create issues even if development mode is enabled in the terminal. You
must deactivate code signature verification globally to debug. To do this, type:

```
$ sudo spctl --master-disable
```

Go to System Preferences / Security and Privacy / General after running the aforementioned
program, then click Any at the bottom of the dialogue. You can debug your unsigned simulation
models after restarting your terminal program.

Step 3: Omnet ++ on Apple Silicon (Recommended)
Although the Apple M1 CPU is not now natively supported by OMNeT++, you can use the
Rosetta 2 emulator to run the x86 64 version. Installation step show in fig 15. Open a terminal
window and enter the following commands to launch OMNeT++ in emulation:

```
$ arch -x86_64 /bin/zsh --login
```
After that, carry with the regular installation steps, making sure to use this terminal for all
commands.


## Figure 14: Installation of Omnet++

Step 4: Unpacking and Downloading Omnet++
OMNeT++ can be downloaded from https://omnetpp.org. Make careful to choose the omnetpp-
6.0.1-macos-x86 64.tgz macOS-specific ZIP while downloading. The place where you want to
instal it should receive the archive. /Users/you> is often your home directory. Open a terminal
and type the following command to extract the archive:

```
$ tar zxvf omnetpp-6.0.1-macos-x86_64.tgz
```
The simulator files will be placed in a subdirectory called omnetpp-6.0.1. As an alternative,
you can use Finder to extract the archive.


Step 5: Setting up Environment Variables
Generally speaking, OMNeT++ needs the omnetpp-6.0.1/bin directory to be in the PATH and
a few environment variables to be specified. Seeting up enviromental variable shown in fig 16.
To set up all these variables, use the setenv script as a source.

```
$ cd omnetpp-6.0.1
$ source setenv
```
Edit.profile,.zprofile, or.zshenv in your home directory and add a line like this to permanently
set the environment variables:

```
[ -f "$HOME/omnetpp-6.0.1/setenv" ] && source "$HOME/omnetpp-6.0.1/setenv"
```

## Figure 15: Setting-up Environmental Variables

## Figure 16: Configuring and Building OMNeT++

Make sure to configure it. the user has the settings you require by checking it. Most of the time,
nothing needs to be changed. Type: in the OMNeT++ directory at the root level.

```
$ ./configure
```

## Figure 17: Configuring and Building OMNeT++

The configure script finds installed software and records system configuration. The Makefile.
inc file, which the makefiles read during the building process, receives the results and writes
them there.

You can compile OMNeT++ after./configure has been completed. In the terminal, type:

```
$ make
```

## Figure 18: Verifying Installation OMNeT++ INET

Step 7: Verifying Installation
Now you may check to see if the example simulations function properly. For instance, the
following commands are entered to launch the Aloha simulation:

```
$ cd samples/aloha
$ ./aloha
```

## Figure 19: Lanucing Oment++ INET

By default, the Qtenv environment will be used to run the experiments. Nice GUI windows and
dialogues should be visible.

Step 7: Lanucing Oment++
A simulation IDE built on Eclipse is included with OMNeT++. The below command is used
to access Omnet++.

```
$ omnetpp
```

```
Figure 20: Lanucing Oment++ INET
```
Do the following if you want to be able to launch the IDE from Applications, the Dock, or a
desktop shortcut: Create an alias for the omnetpp application in the ide subdirectory (right-
click, Make Alias) and drag it into the Applications folder, the Dock, or the desktop after
opening the omnetpp-6.0.1 folder in Finder.

Alternately, execute one or both of the following commands:

```
$ make install-menu-item
$ make install-desktop-icon
```

#### 5.3.2. Running the simulation

A new GUI window should open after your simulation has been successfully built and
launched, looking much like the one in the screenshot below. Qtenv, the primary OMNeT++
simulation runtime GUI, is the owner of the window. In the main area, we should also see a
graphic representation of the network that contains tic and toc. To launch the simulation, click
the Run option in the toolbar. What we ought to observe is that Tic and Toc are communicating
with one another.

Sample Deployment:

Here I have run the test program in which nodes communicate with each other. As shown below
fig 21 & 22. The packets move from one to another. This is one of the common examples in
which the packet move from host-1 to server. Then host-2 sent a packet to Server. And at the
same the whole network. All nodes try to communicate with the server. And transmit the packet
to the server according to the turn.

## Figure 20: Sample Project Deployment


## Figure 21: Node Communication with Server in Oment++


## Chapter 6...............................................................................................................................................

## Experiments and Results Analysis


### 6.1. Primary and Hot-Standby Master Clocks

This topology architecture is similar to a tree. There is a separate time synchronization domain
for each master clock node. The topology consists of two master clock nodes, one is the primary
and the second one is hot-standby node in the network. Hot -standby clock is synchronized
with the primary master clock, and it is the only connection between both time domains. Switch
and device nodes each have two clocks that are independently synced to one of the master
clocks. The main advantage of having two domains empowers the user to continue
synchronization without any hustle in case of one domain failure. The topology in fig 23
consists of the following devices.

```
 Four Device nodes
 Two TSN Switches
 Two Clock Nodes (Hot-Standby and Primary)
```
## Figure 22: Topology of Two Master Clocks


The two Clock spanning trees must be set up for the two different time domains. The clock
nodes in this configuration each have one clock, while the others have two (one for each
domain). Now what we have to consider is that we have to set up two spanning trees for two
separate time domains. As all the nodes have two-time domains except the clock node in one
clock. Code shown in fig 24. Clock1 consists of one FTSP domain and one clock and sends
time as domain 0 to all the other member nodes. Whereas clock 2 sends the timing of its domain
1 to domain 1 of all the other member nodes. Whereas Clock2 never sends the time to
tsnClock2. So now we have learned that clock 2 is our hot-standby master. Whereas Clock1 is
our primary master. So, the hot-standby master node sync with domain-0, and it will send the
time to all the child nodes which are in the domain-1.

## Figure 23: Settings for the clock nodes

As switches also have FTSP modules and two clocks. As the connection between both switches
is a bridge type so, no need to configure it. As in these interfaces, the other clock nodes are the
child nodes and the remaining is the master node. The only exemption that exists is that the
master clock cannot receive sync from switch-1. So, the ethernet-1 can’t be set as a master port.


```
Figure 25: Switches Configration
```
So, As shown above figure 26, we have set clock1 as the master node which has FTSP module
Clock1 going to use his clock, and clock2 is used as a settable clock or initializer. Which is
used to initialize all the nodes for the first time. As in hot-Standby, we have two clocks. By
supposing the example of a tree one is the root and the other one is the branch of the tree. Hot-
standby or clock2 is set as a multi-domain FTSP, so we have two domains but remember one
acts as a parent, and the other one act as a child.

## Figure 25: Configration of Devices


The switches are set up with two FTSP modules and two clocks (one for each domain). The
spanning tree is then specified by defining the ports (we don't need to mention the FTSP
Module Type because it defaults to BRIDGE NODE in TsnSwitch). The interface that connects
to the clock node is the slave port in both domains, while the others are master ports. Since
tsnSwitch1 shouldn't send sync messages to tsnClock1 (since we don't want it to become
synchronized to anything), the eth1 interface isn't configured as a master port.

Same as in switches where we have two FTSP and two clocks in a device so, we need the same
in devices. As shown below fig 27, the clock difference of every node is displayed. The arrows
represent the Flooding time messages.

## Figure 26: Hot Standby and Primary master Clock difference

By exchanging the pDelay messages, the slave nodes and bridges measure the link delay. Link
delay specifics the latency of bits that occur while traveling from one point to the other
endpoint. Using Pdelay messages the average path delay between two clock nodes are


measured. After a basic exchange of pDelay messages, the master clock sends FTSP message
to sync all nodes. As when the master clock time is received there will become a major
difference in time. As the message reaches the slave nodes the time will be set as the new time.
As the setup is protected from failure. In case the master node gets failed we have a backup of
the master clock. The clock speedily switched to clock 1 without affecting synchronization.

## Figure 27: Gptp message transmissions (Spanning tree Visualization)

Below plot show the time difference of clock time to simulation time of the two master
clocks.


## Figure 28: Hot-Standby Master synchronizing to the Primary

## Figure 29: Devices Synchronizing with the Primary Master


As shown in fig. The Hot-Standby is continuously syncing with the primary clock and the
devices shown in fig. are also synchronizing with the primary node in time domain 0. Now we
will consider the time domain 1. The Synchronization from the primary clock has been stopped
and we are on hot standby.

## Figure 30: Clock 2 Synchronization in time domain-1

As the devices are periodically synchronized with the secondary clock or hot-standby clock.
The blue thick line demonstrates the display of the hot-standby clock and all other nodes are
synchronizing with them. Before moving further we will take a look at a single master clock
then we will try to develop a topology that will be more redundant which means the
synchronization never stops even in case of any failure.


### 6.2. One Master Clock

The illusion of the topology is similar to a simple tree. TSNClock is the master node that
transmits the reference time to another node. As this topology consists of two slave nodes and
one master node. The master node time is constered as the reference time for the slaves. One
bridge, two end stations (TsnDevice), one master clock node (TsnClock), and one other node
make up the entire network and are linked by a TsnSwitch:

## Figure 31: Topology of One Master Clock in Oment++

The TSNSwitch input node is connected with TSNDevice whereas the output node of
TSNWwitch is connected with TSNDevice1 and TSNDevice2. By configuring the master ports
in tsnClock and switch, we can configure the spanning tree:

```
“*.tsnClock.ftsp.masterPorts = ["eth0"] // TSN clock master ports
```

```
*.tsnSwitch.ftsp.masterPorts = ["eth1", "eth2"] //TSN switch bridge master ports”
```
As TSNDevice1 has a time difference of 4.15 microseconds whereas a 7.38 microseconds
difference from the Master Node. As the reference node is transmitting the reference time
continuously which the child node uses to synchronize time. The clocks are set once the follow-
up messages are received, so take note of that. The master clock's time and the time gap
between it and the other nodes' times are shown in the following Fig of the synchronization
mechanism:

## Figure 32: Toplogy of One Master Clock Difference

We have one ftsp Master, this is also known as TSNClock. As shown below this have a ftsp
application and a clock. So, each network node in this network has a clock inside and an
oscillator in a clock that is not oscillating accurately. So according to our example there 9ppm
clock difference as compared to standard oscillation time.


## Figure 33: GPTP Application and Oscillator Clock

As GptpSync Message from TSNClock arrives at TSNSwitch Input port. And then the packet
is broadcasted to the child nodes (TSNDevice1,TSN Device2). And in this way time
synchronization took place. The spanning tree shown here corresponds to the direction of the
FTSP sync messages. At the start of the simulation, a few starts are used to measure the link
delay. Stating frames are the standard pattern frames with FTSP packet inside then we have a
sync message. As shown below FTSP massages are continuous.


##### .

## Figure 34: Spanning tree direction of gPTP sync messages

As the time-dependent application needs one of precise time. And once a while we need to
synchronize clocks. So, every device in the topology has its own local time not performing
accurately. This is also true for gate scheduling which is also based on the synchronized local
time.

By comparing the clock time difference to the simulation time, we investigate clock drift across
all clocks:


## Figure 35: Clock time difference to simulation time

The slave clocks are periodically synchronized to the time of the master clock as the difference
in simulation time for the master clock widens (so they keep drifting together). As TSNDevice2
is showing a higher time difference as compared to TSNDevice1. As soon as the Master-node
reference time arrives the child node time gets synced. We also have more complicated cases
as this has only one master and one sync domain, where there are cases where we have multiple
masters nodes as discussed earlier.

### 6.3. Two Master Clocks Exploiting Network Redundancy

The network topology in this arrangement is a ring as shown in fig 37. There are two distinct
time domains for both the hot-standby master clock and the primary master clock. To distribute
the clock time throughout the network, a one-time domain employs the ring topology in a
clockwise fashion, while another uses an anticlockwise direction. The edge of this approach is
provided in case of link failure from the master node or any individual link failure in the


topology ring as we know that they are interlinked from both directions and reach the one-of-
time domain from both master clocks.

The below network consists of the same nodes(TSNClock, TSNSwitch, TsnDevice).

## Figure 36: Primary master clock in time domain

Redundancy in time synchronization can be achieved by following steps:

```
 Device and Switch consist of four sub-clock(Domains), domains 3 and 2 are syncing to
the master node (hot-standby) whereas domains 1 and 0 are syncing with the primary
master node.
 Two Master and One clock FTSP time domains are present on the primary master node.
In the ring, the domains transmit time data both clockwise and anticlockwise.
 We have two sub-clocks, a master domain, and two FTSPs in the hot-standby master
node. The clocks are synced to the master's two domains (primary) by domains 0 and
1, and timing data for the two clocks are sent in both directions by domains 2 and 3
across the ring.
```

```
 As a result, FTSP modules in switches, bridges, and other devices are ftsp slaves.
```
The network will be made redundant in the following section so that any network link or the
primary master clock can fail without interfering with time synchronization. The below fig 38
shows how the sensors are connected in any Vehicle. So, these sensors need continuous
synchronization.

## Figure 37: All sensors are synchronized


## Chapter 7...............................................................................................................................................

## Conclusion and Future Work.................................................................................................................


### 7.1. Conclusion

The proposed methods can be utilized for wire and wireless time synchronization. These are
the most advanced protocols that are available for deployment in autonomous cars. The main
focus of this thesis is the importance of time synchronization in WSN. As the FTSP error is
below 0.5 microseconds. But in a location like particular coverage and out-of-coverage
scenarios, synchronization is further supported with decentralized algorithm, which empower
the WSN to synchronize by multiple sources and limit the residual error. The approach
suggested in this thesis is a combination of FTSP and GNSS. As GNSS refers to the group of
satellites which provide signals from space. Those signals are composed of timing data and
positioning. As the ON-Ground WSN receives this data to determine the exact location as well
as to synchronize the time. As the results of the GNSS approach have been discussed in the
above section. FTSP is implemented by a few numbers of researchers. Whereas FTSP allows
the precise synchronization of safety-critical applications and time in distributed systems.
FTSP high precision is achieved through peer-to-peer communication which took place in layer
2 (MAC Layer). FTSP can achieve an accuracy below 1μs. Delay in the FTSP network can be
assumed to be constant and the Hybrid combination of FTSP and GNSS is more robust as
compared to other protocols (Scheiterer, Na, Obradovic, & Steindl, July 2009).

I have presented a few basic synchronization methods for WSN. FTSP and gPTP are considered
highly Precision. The sender-receiver required 2 sent and receive messages, on the other hand,
Reciever-Receiver required 4 messages to send and 3 messages to receive at nodes. Also, we
need to consider that radio communication is one of the most energy-consuming components.
While TPSN does not suffer from energy complexity in this regard, it does require the
formation of a hierarchical network of nodes, which could raise the synchronization cost.
Although it is a low-complexity alternative for synchronizing sensor networks, mini-sync also
depends on a hierarchical structure among sensor nodes. LTS techniques provide
synchronization at a relatively cheap cost, but their applicability is constrained due to their low
accuracy. In the final conclusion, this approach will minimize the error rate of less than 0.5
microseconds. As In this thesis, I have first discussed the protocols in the literature review and


provided the full functionality of FTSP. As the original paper suggested the results in the range
of 1 μs as the steps missing in the original implementation. As observed that there are a few
other implementations that are combined. So this work is available for further improvements
and to realize new benchmarks. As there is one hardware( CC1000 radio) option also available
nowadays, which can help to achieve new benchmarks.

### 7.2. Future Work

As I have closely followed the research paper of Maroti et. Al’s paper. The minimum error that
has been observed was near 13μs and so more research is needed to match the accuracy of 1.4
μs. As the major component of the constant offset of 5 is also visible which can lead to the
synchronization error of 1.3 μs. Further work needs to consider the appointment to offset and
also the hardware calibrations to achieve the microseconds accuracy. As there is no hardware
implementation yet available. So there is a major lack of in-depth knowledge of FTSP required
to implement it on hardware. To determine the source of error, we need to make a depth study
of plague synchronization within WSN. Further research will also help, to learn about the
distance effect on propagation delay and the effect of propagation delay on time
synchronization. The next step intakes the FTSP implementation on Field Programmable Gate
Arrays. Furthermore, this is the start of time synchronization, yet so many implementations are
required to convert this research into real-life implementation.


## References

1. A. Hu, a. S. (September 2003). Asymptotically Optimal Time Synchronization in Dense Sensor
    Networks. Proceedings of the 2nd ACM International Conference on Wireless Sensor
    Networks and Applications.
2. Aakvaag, N. M. (n.d.). Timing and Power Issues in Wireless Sensor Networks - An industrial
    Test Case. Parallel Processing. ICPP 2005.
3. Athanasios Kanavos, D. F. (January 2021). V2X Communication over Cellular Networks:
    Capabilities and Challenges. CC BY 4.0. doi:10.3390/telecom2010001
4. Benedikt Brecht, D. T. (February 2018). A Security Credential Management System for V2X
    Communications. doi:10.1109/TITS.2018.2797529
5. Bharath Sundararaman, U. B. (May 2005). Clock synchronization for wireless sensor
    networks: a survey. 281-323. Retrieved from https://doi.org/10.1016/j.adhoc.2005.01.002
6. Dr Ian F. Akyildiz, M. C. (29 June 2010). Wireless Sensor Networks. John Wiley & Sons, Ltd.
    doi:10.1002/9780470515181
7. Elson, J. E. (2002). Fine-Grained Network Time Synchronization using Reference Broadcast.
    The Fifth Symposium on Operating Systems Design and Implementation.
8. Estrin, J. E. (2001). Time Synchronization for Wireless Sensor Networks. International Parallel
    and Distributed Processing Symposium.
9. F. Sivrikaya, B. Y. (26 July 2004). Time synchronization in sensor networks: a survey. 45 - 50.
    doi:10.1109/MNET.2004.1316761
10. G.Y. Deng, F. Z. (27-30 November 2006). A Power management for probabilistic clock
    Synchronization in Wireless Sensor Networks. doi:10.1109/ICCT.2006.341714
11. Ganeriwal, S. K. (2003). Timing-Sync Protocol for Sensor Networks. The First ACM Conference
    on Embedded Networked Sensor Systems (SenSys).
12. Ganesan, K. &. (October 2019). 5G V2X Architecture and Radio Aspects. 2019 IEEE
    Conference on Standards for Communications and Networking (CSCN).
    doi:10.1109/CSCN.2019.8931319
13. Geng, H. (2017). Internet of Things and Data Analytics Handbook. Retrieved from
    https://ieeexplore.ieee.org/book/8040335
14. Ghosal, A. &. (March 2020). Security Issues and Challenges in V2X: A Survey. Computer
    Networks 169:107093. doi:10.1016/j.comnet.2019.107093


15. Gyula Simon, M. M. (November 2004). Sensor network-based countersniper system.
    Proceedings of the 2nd International Conference on Embedded Networked Sensor Systems,
    SenSys 2004. doi:10.1145/1031495.1031497
16. Hossain, T. I. (n.d.). Introduction to Network Simulator NS2. Wireless Mobile Ad Hoc
    Networks, 293–344. Retrieved from https://link.springer.com/chapter/10.1007/978-1-4614-
    1406-3_12
17. Ill-Keun Rhee, J. L.-C. (2009;9(1):56-85. doi: 10.3390/s90100056. Epub 2009 Jan 6.). Clock
    synchronization in wireless sensor networks: an overview. Retrieved from
    https://pubmed.ncbi.nlm.nih.gov/22389588/
18. J. Elson, a. K. (October 2002). Wireless Sensor Networks: A New Regime For Time
    Synchronization. In Proceedings of the First Workshop on Hot Topics In Networks (HotNets-I).
19. J. Elson, L. G. (December 2002). Fine-Grained Time Synchronization using Reference
    Broadcasts. Proceedings of the Fifth Symposium on Operating Systems Design and
    Implementation.
20. J. Hill, D. C. (2001). A Wireless Embedded Sensor Architecture for System-Level Optimization.
    Technical Report, U.C. Berkeley,.
21. J.V. Greunen, a. J. (September 2003). “Lightweight Time Synchronization for Sensor
    Networks”. Proceedings of the 2nd ACM International Conference on Wireless Sensor
    Networks and Applications.
22. Karls, M. M. (2018). Networking Vehicles to Everything. Retrieved from
    https://doi.org/10.1515/9781501507243
23. Khondokar Fida Hasan, C. W.-C. (October 2018). Time synchronization in vehicular ad-hoc
    networks: A survey on theory and practice. 39-51. Retrieved from
    https://www.sciencedirect.com/science/article/abs/pii/S2214209618300421
24. Lédeczi, Á. M. (SenSys 04 SenSys 04, 2004). The Flooding Time Synchronization Protocol.
    Proceedings of the 2nd International Conference on Embedded Network Sensor Systems.
    Baltimore, MD, USA. Retrieved from
    https://www.researchgate.net/publication/221091643_The_Flooding_Time_Synchronizatio
    n_Protocol
25. Levy. (n.d.). timesynchronization gptp. Retrieved from github.com: https://github.com/inet-
    framework/inet/tree/master/showcases/tsn/timesynchronization/gptp
26. Lien, S.-Y. &.-J.-C.-L.-M. (13 February 2020). 3GPP NR Sidelink Transmissions Toward 5G V2X.
    (pp. 35368 - 35382). IEEE. doi:10.1109/ACCESS.2020.2973706
27. Lili Miao, S.-F. C.-L.-L. (17 January 2022). How Does C-V2X Help Autonomous Driving to Avoid
    Accidents? Retrieved from https://doi.org/10.3390/s22020686
28. Manzo, M. R. (2005). Time Synchronization Attacks in Sensor Networks. Proceedings of the
    3rd ACM workshop on Security of ad hoc and sensor networks SASN.
29. Maria Christopoulou, S. B. (28 December 2022). Artificial Intelligence and Machine Learning
    as key enablers for V2X communications: A comprehensive survey. Vehicular
    Communications. Retrieved from
    https://www.sciencedirect.com/science/article/abs/pii/S2214209622001164
30. Maroti, M. K. (2004). The Flooding Synchronization Protocol. Proc. Of the Second ACM
    Conference on Embedded Networked Sensor Systems (SenSys). Retrieved from
    [http://www.isis.vanderbilt.edu/publications/archive/Maroti_M_11_3_2004_The_Floodi.pdf](http://www.isis.vanderbilt.edu/publications/archive/Maroti_M_11_3_2004_The_Floodi.pdf)
31. Murtuza Jadliwala, Q. D. (16 March 2009). Towards a theory for securing time
    synchronization in wireless sensor networks. Retrieved from
    https://dl.acm.org/doi/10.1145/1514274.1514303
32. R ̈omer, K. (June 2003). Temporal Message Ordering in Wireless Sensor Networks. IFIP
    MedHocNet, Mahdia, Tunisia.
33. R ̈omer, K. (October 2001). Time Synchronization in Ad Hoc Networks. ACM Symposium on
    Mobile Ad Hoc Networking and Computing.
34. Ray Lattarulo, D. H. (n.d.). Towards conformant models of automated electric vehicles. 2018
    IEEE International Conference on Vehicular Electronics and Safety (ICVES).
    doi:10.1109/ICVES.2018.8519484
35. S. Ganeriwal, R. K. (November 2003). Timing Sync Protocol for Sensor Networks. ACM
    SenSys.
36. S. Natarajan, A. K. (June 2019). IoT, Automotive Vehicle-to-Everything (V2X) Communication
    Using IOT. In S. V. P. Janani, Information and Communication Technology for Sustainable
    Development, Proceedings of ICT4SD 2018 (pp.195-204) (Vols. 10.1007/978-981-13-7166-
    0_19). Retrieved from
    https://www.researchgate.net/publication/334031994_Automotive_Vehicle-to-
    Everything_V2X_Communication_Using_IoT
37. Scheiterer, R., Na, C., Obradovic, D., & Steindl, G. (July 2009). Synchronization Performance
    of the Precision Time Protocol in Industrial Automation Networks. IEEE Transactions on
    Instrumentation and Measurement. doi:10.1109/TIM.2009.2013655
38. Sheng-Lung Peng, S. P. (January 2020). Principles of Internet of Things (IoT) Ecosystem:
    Insight Paradigm. Intelligent Systems Reference Library. doi:10.1007/978-3-030-33596-0


39. Sivrikaya, F., & Yener, B. (2004). Time synchronization in sensor networks: A Survey.
    Network, IEEE Volume 18.
40. Veerarittiphan, M. S. (WCNC 2003). Simple, Accurate Time Synchronization for Wireless
    Sensor Networks. IEEE Wireless Communications and Networking Conference.
41. Wang, J. &. (15 January 2019). A Survey of Vehicle to Everything (V2X) Testing. Retrieved
    from https://doi.org/10.3390/s19020334
42. Zsolt Szendrei, N. V. (May 2018). A SUMO-Based Hardware-in-the-Loop V2X Simulation
    Framework for Testing and Rapid Prototyping of Cooperative Vehicular Applications. (V. a.
    (pp.426-440), Ed.) doi:10.1007/978-3-319-75677-6_37


