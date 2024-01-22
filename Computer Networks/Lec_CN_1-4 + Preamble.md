# Computer Networks (SOFE3850)

Todo: Upload images

## <ins>Office hours</ins>:
- Tues. 6-7 pm
- Thurs. 2-3 pm

## <ins>Tutorials</ins>:
- Mondays 2:10 - 3:30
- **Wednesdays 5:10 - 6:30**

## <ins>Labs</ins>:
| CRN  | Location | Times        | Days                              | TA                |
|------|----------|--------------|-----------------------------------|-------------------|
|74018 | ERC3052  | Fri 5-8 pm   | 19/1, 2/2, 16/2, 8/3, 22/3, 5/4   | Md Maruf          |
|74019 | ERC3052  | Tue 2-5 pm   | 16/1, 30/1, 13/2, 05/3, 19/3, 2/4 | Shawon Ashadullah |
|74020 | ERC3052  | Tue 2-5 pm   | 9/1, 23/1, 6/2, 27/2, 12/3, 26/3  | Shawon Ashadullah |
|74021 | ERC3052  | Thr 11am-2pm | 18/1, 1/2, 15/2, 7/3, 21/3, 4/4   | Amin Avan         |
|74283 | ERC3052  | Thr 11am-2pm | 11/1, 25/1, 8/2, 29/2, 14/3, 28/3 | Amin Avan         |

**Quizzes:**
- Lockdown browser will be used in quizzes and must be done in class.
- Expect a quiz every week. *(I will drop the lowest quiz mark)*

| Category                     | Mark   |
|------------------------------|--------|
| In-Class Activities/Quizzes  | 10%    |
| Labs                         | 15%    |
| Project                      | 15%    |
| Midterm (Feb. 26th)          | 20%    |
| Final                        | 40%    |

**Project:**
TBD

**Midterm:**
- The exam will be on Feb. 15th during the class time.
- No midterm deferral, marks will be added to the final exam
- Must pass final.

## <ins>Course Overview</ins>

Network history and architectures; reference Model for Open Systems Interconnection (OSI): descriptions, examples, and applications; bridges, routers, gateways; routing, multicast deliver; TCP/IP protocol suite; network topologies (ring, bus, tree, star, mesh); local area networks, Ethernet, Token passing, wireless LAN, personal LAN, WAN

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 1 | Introduction to Computer Networks</summary>


  # **Intro:**
  - Information gathering, processing, and distribution are the key technologies in these days
  - As the ability to gather, process, and distribute information grows, the demand for sophisticated information processing grows even faster.
  - The merging of computers and communications has had a profound influence on the way computer systems are organized;
    - From computer center to computer networks

#  **Uses of Computer Networks:**

  Computer networks are collections of autonomous computers interconnected by a single technology, e.g., the Internet
  
  They have many uses:
  - Business Applications
    - Resource sharing
    - Information sharing
    - VoIP: Voice over Internet Protocol
  - Home Applications
  - Mobile Users

These uses raise social issues.

### Business Applications

Companies  use networks and computers for resource sharing with the client-server model:
Other popular uses are communication, e.g., email, VoIP, and e-commerce

|Tag| Full name| Example|
|---|---|---|
| B2C | Business-to-consumer | Ordering books online |
| B2B | Business-to-business | Car manufacturer ordering tires from supplier |
| G2C | Government-to-consumer | Government distributing tax forms electronically |
| C2C | Consumer-to-consumer |Auctioning second-hand products online |
| P2P | Peer-to-peer | Music sharing |

### Home Applications
- Homes contain many networked devices, e.g., computers, TVs, connected to the Internet by cable, DSL, wireless, etc.
- Home users communicate, e.g., social networks, consume content, e.g., video, and transact, e.g., auctions
- Some application use the peer-to-peer model in which there are no fixed clients and servers:

### Mobile Users

- Tablets, laptops, and smart phones are popular devices; WiFi hotspots and 4G LTE cellular provide wireless connectivity.
- Mobile users communicate, e.g., voice and texts, consume content, e.g., video and Web, and use sensors, e.g., GPS.
- Wireless and mobile are related but different:

| Wireless  | Mobile | Typical applications|
|-|-|-|
|  No | No  | Desktop computers in offices|
|  No | Yes | A notebook computer used in a hotel room|
| Yes | No  | Networks in unwired buildings|
| Yes | Yes | Store inventory with a handheld computer|

### Social Issues
- Network neutrality – no network restrictions
  - Communications that are not differentiated by their content or source or who is providing the content
- Content ownership,
  - Pirated music and movies
- Anonymity and censorship
  - Web browsers store cookies (small files) on users’ computers to allow companies to track users’ activities
- Privacy, e.g., Web tracking and profiling
- Theft of information, e.g.,
  - Botnets: pool of compromised machines used to send spams
  - Phishing: messages masquerade as originating from a trustworthy party (e.g. your bank), to trick you into revealing sensitive information

# **Network Hardware:**

Networks can be classified by:

- Transmission technology:
  - Point-to-point: connect individual pairs of machines (unicast)
  - Broadcast: the communication channel is shared by all machines on the network
- Network scale:

| Scale    | Type                                   |
|----------|----------------------------------------|
| Vicinity | PAN (Personal Area Network)            |
| Building | LAN (Local Area Network)               |
| City     | MAN (Metropolitan Area Network)        |
| Country  | WAN (Wide Area Network)                |
| Planet   | The Internet (network of all networks) |
  
- An **“internetwork”** is any larger network made up of smaller component networks. The **“Internet”** (with a capital I) is the set of all connected networks.

### Personal Area Network (PAN)
Connect devices **over the range of a person**
- Example of a Bluetooth (wireless) PAN:

![bluetooth](../static/CN_0.png)


### Local Area Networks (LAN)
Connect devices **in a home or office building**
- If it is used in a company, it is called enterprise network

### Metropolitan Area Networks (MAN)
Connect devices **over a metropolitan area (city)**
Example: MAN based on cable TV network:
- Also delivers Internet

### Wide Area Networks 
Connect devices **over a country**
Example:
- WAN connecting three branch offices by using leased lines
- An ISP (Internet Service Provider) network is also a WAN. Customers buy connectivity from the ISP to use it.
- A VPN (Virtual Private Network) is a WAN built from virtual links that run on top of the Internet.

# **Internetworks**

Internetwork (internet): a collection of interconnected networks
- Networks are connected through devices (called gateways) that provide the necessary translation, both in terms of hardware and software
- Gateways are distinguished by the layer at which they operate in the protocol hierarchy:
  - Using too low-level gateway, will prevent from making connections between different kinds of networks
  - Using too high-level gateway, then the connection will only work for particular applications.
  - The level in the middle that is ‘‘just right’’ is often called the network layer, and a router is a gateway that switches packets at the network layer.

# **Internet**
Before the Internet was the ARPANET (Advanced Research Projects Agency Network ), a decentralized, packet-switched network based on Baran’s ideas. The early Internet used NSFNET (National Science Foundation Network) (1985-1995) as its backbone; universities connected to get on the Internet NSFNET topology in 1988.

The modern Internet is more complex:
- ISP networks serve as the Internet backbone
  - ISPs connect or peer to exchange traffic at IXPs
  - Within each network routers switch packets
  - Between networks, traffic exchange is set by business agreements
  - Customers connect at the edge by many means
    - Cable, DSL, Fiber-to-the-Home, 3G/4G wireless, dialup
- Data centers concentrate many servers (“the cloud”)
- Most traffic is content from data centers (esp. video)
- The architecture continues to evolve
- **ISP** = Internet Service Provider,
- **IXP** = Internet eXchange Point, where ISPs connect their networks to exchange traffic

## What’s the Internet?

### Millions of connected computing devices:
- hosts = end systems
- running network apps
- Eg. PC, smartphone, ...

### Communication links
- fiber, copper, radio, satellite
- transmission rate: bandwidth

### Packet switches:
- forward packets (chunks of data)
- routers and switches

### Internet: “network of networks”
- Interconnected ISPs

### Protocols:
- Control sending, receiving of messages
- e.g., TCP, IP, HTTP, Skype, 802.11

### Internet standards:
- RFC: Request for comments
- IETF: Internet Engineering Task Force


# Internet Architecture

![cn1](../static/CN_1.png)
![cn1_1](../static/CN_1_1.png)

## Internet structure: network of networks
End systems connect to Internet via access ISPs (Internet Service Providers)
- Residential, company and university ISPs

Access ISPs in turn must be interconnected.
- So that any two hosts can send packets to each other

Resulting network of networks is very complex
- Evolution was driven by economics and national policies

At center: small number of well-connected large networks
- “tier-1” commercial ISPs (e.g., Level 3, Sprint, AT&T, NTT), national & international coverage
- content provider network (e.g, Google): private network that connects its data centers to Internet, often bypassing tier-1, regional ISPs

**TODO: GET IMAGES FOR THIS SECTION (from slide 30)**

# Types Of Networks
## Network Virtualization
![network virtualization](../static/CN_1_2_1.png)
![network virtualization](../static/CN_1_2_2.png)


## Cloud (Infrastructure as a Service)


![cloud](../static/CN_1_3.png)

# Network Security
## Malware
Malware exists in hosts via the internet. Malware can get into host machines from:
- virus: self-replicating infection by receiving/executing object (e.g., e-mail attachment)
- worm: self-replicating infection by passively receiving object that gets itself executed

Spyware: malware that can record keystrokes, web sites visited, upload info to collection site

Infected host can be enrolled in *botnet*, used for spam, or DDoS attacks

## Server Attacks, Network infrastructure

Denial of Service (DoS): attackers make resources (server, bandwidth) unavailable to legitimate traffic by overwhelming resource with bogus traffic
1. select target
2. break into hosts around the network
3. send packets to target from compromised hosts\


## Packet sniffing
- broadcast media (shared Ethernet, wireless)
- promiscuous network interface reads/records all packets (e.g., including passwords!) passing by
- wireshark software is a (free) packet-sniffer

## Fake addresses
*IP spoofing*: send packet with false source address

# Wireless LANS
In 802.11, clients communicate via an AP (Access Point) that is wired to the rest of the network.
Uses the ISM (Industrial, Scientific, and Medical) bands defined by ITU-R
- 902-928 MHz
- 2.4-2.5 GHz
- 5.725-5.825 GHz

## IEEE802.11 (WiFi)
Signals in the ISM band vary in strength due to many effects, such as multipath fading due to reflections
- requires complex transmission schemes, e.g., OFDM (Orthogonal Frequency Division Multiplexing)

Radio broadcasts interfere with each other, and radio ranges may incompletely overlap
- CSMA (Carrier Sense Multiple Access) designs are used

# RFID & Sensor Networks

## RFID (Radio Frequency Identification)
Passive UHF RFID networks everyday objects:
- Tags (stickers with not even a battery) are placed on objects
- Readers send signals that the tags reflect to communicate

## Sensor networks
They spread small devices over an area:
- Devices send sensed data to collector via wireless hops

# Standardization
Standards define what is needed for interoperability
Some of the many standards bodies:
| Body | Area | Examples |
|-|-|-|
| ITU (International Telecommunication Union) | Telecommunications | G.992, ADSL, H.264, MPEG4 |
| IEEE (Institute of Electrical and Electronics Engineers) | Communications | 802.3, Ethernet, 802.11, WiFi |
| IETF (Internet Engineering Task Force) | Internet | RFC 2616, HTTP/1.1, RFC 1034/1035, DNS |
| W3C (World Wide Web Consortium) | Web | HTML5 standard, CSS standard |

# Metric Unit review
![units](../static/CN_1_99_1.png)

</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 2 | Network Software</summary>

## Layer Architecture
- Networking requires the co-operation of many different tasks
- Raw data transfer over a physical channel
- Error and flow control
- Switching
- Routing
- Traffic control
- Network Security

# Protocol Layers
Protocol layering is the main structuring method used to divide up network functionality.
- Each protocol instance talks virtually to its peer
- Each layer communicates only by using the one below
- Lower layer services are accessed by an interface
- At bottom, messages are carried by the medium
- Each protocol at different layers serves a different purpose
- Each lower layer adds its own header (with control information) to the message to transmit and removes it on receive
- Layers may also split and join messages, etc.

![pl](../static/CN_2_1.png)

![pl](../static/CN_2_2.png)

# Design Issues for the Layers

Each layer solves a particular problem but must include mechanisms to address a set of recurring design issues.
| Issue | Example mechanisms at different layers |
|-|-|
| Reliability | despite failures Codes for error detection/correction (Ch 3.2, 3.3), Routing around failures (Ch 5.2) |
| Network growth and evolution | Addressing (Ch 5.6) and naming (Ch 7.1), Protocol layering (Ch 1.3) |
| Allocation of resources like bandwidth | Multiple access (Ch 4.2), Congestion control (Ch 5.3, 6.3) |
| Security against various threats | Confidentiality of messages (Ch 8.2, 8.6), Authentication of communicating parties (Ch 8.7) |


# Connection-oriented vs. connectionless service

Layers can offer two types of service to the layers above them:
- **Connection-oriented**: a connection must be set up for ongoing use (and torn down after use), e.g., phone call. A connection should be established before sending data and every packet should be acknowledged
- **Connectionless**: messages are handled separately, e.g., postal delivery (each message (letter) carries the full destination address and routed independently)

Each kind of service can further be characterized by its reliability. Reliability in this context means the message is acknowledged. (i.e. whether or not a service receives a data packet)

![connect](../static/CN_2_3.png)


# Service Primitives

- A service is provided to the layer above as primitives (operations). If the protocol stack is located in the _operating system,_ the primitives are normally **system calls.**
  - These calls cause a trap to kernel mode, which then turns control of the machine over to the operating system to send the necessary packets.
 
A hypothetical example of service primitives that may provide a reliable byte stream (connection-oriented) service:

| Primitive | Meaning |
|-|-|
| LISTEN | Block waiting for an incoming connection |
| CONNECT | Establish connection with a waiting peer |
| ACCEPT | Accept an incoming connection from a peer |
| RECEIVE | Block waiting for an incoming message |
| SEND | Send a message to the peer |
| DISCONNECT | Terminate a connection |


![primitives](../static/CN_2_4.png)

# Relationship of Services to Primitives

A service is a set of primitives (operations) that a layer provides to the layer
above it:
- A layer provides a _service_ to the one above it [**vertical**]

A protocol, in contrast, is a set of rules governing the format and meaning of the packets, or messages that are exchanged by the peer entities within a layer.
- A layer talks to its peer using a _protocol_ [**horizontal**]

![PROTOCOL](../static/CN_2_5.png)

## Reference Models

Reference models describe the layers in a network architecture
- **OSI** (Open Systems Interconnection) reference model (Developed by the International Standard Organization (ISO))
- **TCP/IP** reference model
- Model used for this text
- Critique of OSI and TCP/IP

# OSI Reference Model

A principled, international standard, seven layer model to connect different systems

| Layer | Name | Protocol |
|-|-|-|
| 7 | Application | Provides functions needed by users |
| 6 | Presentation | Converts different representations |
| 5 | Session | Manages task dialogs |
| 4 | Transport | Provides end-to-end delivery |
| 3 | Network | Sends packets over multiple links |
| 2 | Data Link | Sends frames of information |
| 1 | Physical | Sends bits as signals over the channel |

### Physical Layer:
- bits “on the wire”.
- Determines the specs for all physical components
  - Cabling: Twisted Pair, Fiber Optic, Coax Cable
  - Interconnect methods (topology / devices)
  - Data encoding (bits to signals)
  - Electrical properties

Examples:
- Ethernet (IEEE 802.3)
- Token Ring (IEEE 802.5)
- Wireless (IEEE 802.11n, ac)


What are the Physical Layer components on computer?
- NIC: Network Interface Card
- It has a MAC Address/Physical address of a computer

---

### Link Layer:
- Data transfer between neighboring network elements
  - Moving frames from one hop (node) to another
- Provides error detection/correction capability
  - Using acknowledgement
  - FEC (Forward Error Correction)
- Control access to the shared channel.
  - MAC: Medium Access Control sublayer
 
#### Sub-layers of the Data Link Layer
- MAC (Media Access Control)
  - Gives data to the NIC
  - Controls access to the media through:
    - CSMA/CD Carrier Sense Multiple Access/Collision Detection
    - Token passing
- LLC (Logical Link Layer)
  - Manages the data link interface (or Service Access Points (SAPs))
  - Can detect some transmission errors using a Cyclic Redundancy Check (CRC).
    - If the packet is bad the LLC will request the sender to resend it.

---

### Network Layer:
- Controls the operation of the subnet
  - Provides network-wide addressing and a mechanism to move packets between networks (routing)
    - routing of datagrams (packets) from source to destination
- Responsibilities:
  - Network addressing, Routing
  - Handling congestion in conjunction with higher layers

Examples: IP, routing protocols

![network layer](../static/CN_2_6_1.png)

### Transport Layer:
- Process-process data transfer
- Provides reliable data delivery
- Receives info from upper layers and segments it into packets
- Provides end-to-end error control and flow control
  - Examples:
  - TCP, UDP
 

![transport layer](../static/CN_2_6_2.png)

Differences between Data-Link and Transport layers in terms of Error Control


![transport layer](../static/CN_2_6_3.png)

### Session Layer:
- Allows applications to maintain an ongoing session
- Synchronization, checkpointing to allow users to pick up from where they left off in the event of a crash and subsequent recovery
  - Examples:
  - Operating systems, Scheduling
  - Remote Procedure Call (RPC)

### Presentation Layer: Data representation
- Allow applications to interpret meaning of data, e.g., encryption, compression, machine-specific conventions
  - Examples:
  - ASCII/EBCDIC, JPEG, MP3
- Why presentation layer?
  - Example: what is the value of 10010001 ?
    - Answer: It depends on how you want to interpret it.
      - If it is interpreted as unsigned integer: 145
      - If it is interpreted as signed integer: -111
      - If it is interpreted as ASCII (odd parity): H

### Application Layer: supporting network applications
- Network Processes to applications
- Gives end-user applications access to network resources
- Where is it on my computer?
  - Workstation or Server Service in MS (Microsoft) Windows
    - Examples:
    - FTP, SMTP, HTTP, Telnet, VoIP, Secure Shell

## How do all layers work together?

Each layer contains a Protocol Data Unit (PDU), which are used for peer-to-peer contact between corresponding layers.

**Data** is handled by the _top three layers_, then **Segmented** by the _Transport_ layer. The _Network_ layer places it into **packets** and the _Data Link_ **frames** the packets for transmission. _Physical_ layer converts it to **bits** and sends it out over the media. The _receiving computer_ **reverses** the process using the information contained in the PDU.


![work together](../static/CN_2_7_1.png)
![work together](../static/CN_2_7_2.png)
![work together](../static/CN_2_7_3.png)


# TCP/IP Reference Model

![work together](../static/CN_2_7_4.png)

The **link layer** describes what links such as **serial lines** and **classic Ethernet** must do to meet the needs of the connectionless internet layer.



The internet layer defines two protocols:
- IP (Internet Protocol),
- ICMP (Internet Control Message Protocol) to help the IP.

The job of the **internet layer** is to deliver IP packets where they are supposed to go.

The **transport layer** allows peer entities on the source and destination hosts to carry on a conversation. It defines two protocols:
- **TCP** (Transmission Control Protocol)
  - It is a reliable connection-oriented protocol
  - It handles flow control to make sure a fast sender cannot swamp a slow receiver
- **UDP** (User Datagram Protocol)
  - It is an unreliable, connectionless protocol
  - It is also widely used for one-shot, client-server-type request-reply queries and applications in which prompt delivery is more important than accurate delivery, such as transmitting speech or video.
  - 
![Layers](../static/CN_2_8_1.png)

![TCP](../static/CN_2_8_2.png)

![UDP](../static/CN_2_8_3.png)

# Socket Programming: TCP

## Server Programming:
1. Socket Creation
```java

int sockfd = socket(domain, type, protocol)

/* sockfd: socket descriptor, an integer (like a file handle)

domain: integer, specifies communication domain

AF_ LOCAL: used for communication between processes on the same host
AF_INET: used for communication between processes on different hosts connected by IPV4
AF_INET6: used for communication between processes on different hosts connected by IPV6

type: communication type

SOCK_STREAM: TCP(reliable, connection-oriented)
SOCK_DGRAM: UDP(unreliable, connectionless)

protocol: Protocol value for Internet Protocol(IP), which is 0 */

```

2. Bind: binds the socket to the address and port number specified in addr. You can use INADDR_ANY to use any IP address on the server to receive new clients.

```java
int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);
```

3. Listen: It puts the server socket in a passive mode, where it waits for the client to approach the server to make a connection.

```java
int listen(int sockfd, int backlog);
```
backlog: is the maximum length to which the queue of pending connections

4. Accept

```java
int new_socket= accept(int sockfd, struct sockaddr *addr, socklen_t *addrlen);
```
It extracts the first connection request on the queue of pending connections for the listening socket, sockfd, creates a new connected socket, and returns a new file descriptor referring to that socket.

At this point, the connection is _established_ between client and server, and they are ready to transfer data.

You can send and receive data, when done, close the connection:

```java
close(sockfd);
```

## Client Programming:

1. Socket Creation
- The same as that of server’s socket creation

```java
int sockfd = socket(domain, type, protocol)
```

1. Connect
```python
int connect(int sockfd, const struct sockaddr *addr, socklen_t addrlen);
```
- The connect() system call connects the socket referred to by the file descriptor sockfd to the address specified by addr.
- Server’s address and port is specified in addr.

You can send and receive data; When done, close the connection:
```python
close(sockfd);
```
![stuff](../static/CN_2_9_1.png)
![stuff](../static/CN_2_9_2.png)
![stuff](../static/CN_2_9_3.png)
![stuff](../static/CN_2_9_4.png)
![stuff](../static/CN_2_9_5.png)

# Socket Programming: UDP

UDP is a connection-less protocol. It does not require any handshaking prior to sending or receiving data

## Server Side
1. Create a socket:
```java
int socket_desc = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
```
2. Bind socket descriptor to the server address:
```java
bind(socket_desc, (struct sockaddr*)&server_addr, sizeof(server_addr);
```
- Unlike TCP, the server-side does not wait for a client to connect and, therefore, does not receive the client’s address prior to sending and receiving data. Instead, the server receives information about the client when it receives data using the recvfrom() method:

3. Send/receive data
```java
recvfrom(socket_desc, client_message, sizeof(client_message), 0, (struct sockaddr*)&client_addr, &client_struct_length);
```
- The client’s information, stored in the variable client_addr
```java
sendto(socket_desc, server_message, strlen(server_message), 0, (struct sockaddr*)&client_addr, client_struct_length);
```
4. Close the socket to end the communication:
```java
close(socket_desc);
```

## Client Side
1. Create a socket, and initialize the server’s address information in a variable of type sockaddr_in
```java  
int socket_desc = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
```
2. Send and receive data:

- Unlike TCP, when the client sends and receives data using sendto() and recvfrom(), the server’s information has to be given every time:
```java
sendto(socket_desc, client_message, strlen(client_message), 0, (struct sockaddr*)&server_addr, server_struct_length);
```
```java
recvfrom(socket_desc, server_message, sizeof(server_message), 0, (struct sockaddr*)&server_addr, &server_struct_length);
```




The **application layer** contains all the higher-level protocols:
- **TELNET**, to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection
- **FTP** (File Transfer Protocol)
- **SMTP** (Simple Mail Transfer Protocol), for electronic mail
- **DNS** (Domain Name System), for mapping host names onto their network addresses
- **HTTP** (Hyper Text Transferee Protocol), for fetching pages on the World Wide Web
- **RTP** (Real Time Protocol), for delivering real-time media such as voice or movies

![stuff](../static/CN_2_10.png)




</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 3 | The Physical Layer</summary>

The physical layer is the foundation on which other layers are built. The properties of wires, fiber, and wireless limit what the network can do. It determines _**throughput, latency, and error rate**_ of a network communication link.
The key problem is to send (digital) bits using only (analog) signals; This is called _**modulation**._

# Theoretical Basis for Data Communications

Information can be transmitted on wires by varying some physical property such as **voltage or current, frequency, or phase.**

Communication rates have fundamental limits:
- Fourier analysis
- Bandwidth-limited signals
- Maximum data rate of a channel


**Bandwidth:**

To electrical engineers, (analog) bandwidth is a quantity measured in Hz.
To computer scientists, (digital) bandwidth is the maximum data rate of a channel, in **bps**.

## Fourier Analysis
A time-varying signal can be equivalently represented as a series of frequency components (harmonics) or infinite number of sines and cosines:

The signal period is T, so its fundamental frequency is f=1/T

![](../static/CN_3_1_1.png)

## Bandwidth-Limited Signals
Consider the transmission of the ASCII character "b" = "01100010". Having less bandwidth, we loose some of the harmonics.
- This degrades the received signal

![](../static/CN_3_1_2.png)

# Guided Transmission Media

Media have different properties, hence performance in terms of bandwidth, delay, cost, and ease of installation and maintenance. They are divided into two groups:

**Guided media**,
- Copper wire
  - Twisted pairs
  - Coaxial cable
  - Power lines
- Fiber optics
  - Single mode
  - Multimode

**Unguided media**,
- Terrestrial wireless
- Satellite
- Lasers through the air

## Wires – Twisted Pair
Two insulated copper wires; used in LANs and telephone lines. The twists reduce radiated signal (interference), and the signal is carried as the difference in voltage between the two wires. The bandwidth depends on wire thickness and the distance traveled. Twisted-pair cabling comes in several categories:
- Category 5 (Cat 5) has 4-twisted pairs grouped together:
  - 100-Mbps Ethernet uses two (out of the four) pairs, one pair for each direction
  - 1-Gbps Ethernet uses all four pairs in both directions simultaneously
- Category 6 (compatible with cat 5): 10Gbps, has more stringent specifications for crosstalk and system noise, up to 100m.
  - UTP (unshielded twisted pair).
- Category 7: it is STP (shielded twisted pair)

![](../static/CN_3_2_1.png)

## Wires – Coaxial Cable (“Co-ax”)
Two concentric copper conductors, also common but more expensive than twisted pair. It has better shielding and more bandwidth for longer distances and higher rates than twisted pair. This is commonly used for video, (cable TV), because it needs larger bandwidth. It is bidirectional, broadband (multiple channels on cable)

Two types:
- 50-ohm: mainly used for digital transmission
- 75-ohm: mainly used for analog transmission (TV cable)
  -  Now it is used for both digital and analog.

![](../static/CN_3_2_2.png)

## Wires – Power Lines
Household electrical wiring is another example of wires
- Convenient to use, but horrible for sending data
- Electricity is at 50-60Hz
- Data is at much higher frequencies

![](../static/CN_3_2_3.png)

Wires – Fiber Optics Cables
- Glass fiber carrying light pulses, each pulse a bit (pulse of light indicates a 1 bit and absence of light indicates a 0 bit)
- Used for high-speed point-to-point transmission (e.g., 10’s-100’s Gpbs)
- It has a low error rate, therefore repeaters spaced far apart (Light is immune to electromagnetic noise)
- Common for high data rates and long distances (backbone)
  - Long distance ISP links, and Fiber-to-the-Home (FttH)
  - Light carried in very long, thin strand of glass
- It has three key components: the light source, the transmission medium, and the detector (generates an electrical pulse when light falls on it.).

![](../static/CN_3_2_4.png)

**Single-mode**
- Core so narrow (10μm) light can’t even bounce around
- Used with lasers for long distances, e.g., 100km

**Multi-mode**
- Core diameter is 50 μm
- So light can bounce; each ray above the critical incident is said to have a different mode
- Used with LEDs for cheaper, shorter distance links

![](../static/CN_3_2_5.png)

# Network Topology / Hardware

## How so many computers are connected together? 

Three various configurations, called **topologies**, have been used to administer LANs:

- Bus topology: All nodes are connected to a single communication line that carries messages in both directions
  - Simple and low-cost
  - A single cable called a trunk (backbone, segment)
  - Only one computer can send messages at a time
  - Passive topology - computer only listen for, not regenerate data

![](../static/CN_3_3_1.png)

- Star topology: A configuration that centers around one node to which all others are connected and through which all messages are sent
  - Each computer has a cable connected to a single point
  - More cabling, hence higher cost
  - All transmission through the hub (switch); if down, entire network down
  - Depending on the intelligence of hub, two or more computers may send message at the same time

![](../static/CN_3_3_2.png)

- Ring topology: A configuration that connects all nodes in a closed loop on which messages travel in one direction
  - Every computer serves as a repeater to boost signals
  - Typical way to send data by Token passing:
    - only the computer who gets the token can send data
   
![](../static/CN_3_3_3.png)


Disadvantages:
- If one computer fails, whole network fails
- Difficult to add computers
- More expensive

## Network interface cards
- Network adapter
- Connects node to the media
- Unique Machine Access Code (MAC address)
  - It is a 6 bytes long
 
![](../static/CN_3_4_1.png)


## Network linking devices
- Connect nodes in the network
- Cable runs from node to device
- Crossover cable connects two computers together

### Switches
- Replacement for hubs
- Only intended node receives the transmission
- Fast and secure

![](../static/CN_3_4_2.png)

### Router
- Connects two or more LANs together
- Packets sent to the remote LAN will cross
- Network is segmented by the IP addresses
- Connect internal networks to the Internet
- Need to be configured before installation

![](../static/CN_3_4_3.png)

## Gateway
- Connects two dissimilar networks
- Connects coax to twisted pair
- Most gateways contained in other device

# Wireless Transmission
Types:
- Electromagnetic Spectrum
- Radio Transmission
- Microwave Transmission
- Light Transmission
- Wireless vs. Wires/Fiber

## Electromagnetic Spectrum
- Signal carried in electromagnetic spectrum
- The number of oscillations per second of a wave is called its frequency (f) and is measured in Hz
- The time between two consecutive maxima (or minima) is called the period, T in seconds (T=1/f).
- The distance between two consecutive maxima (or minima) is called the wavelength, λ (lambda) in meters.
- Electromagnetic waves travel at the speed of light c (where c = 3 × 10<sup>8<sup> m/sec)
- The fundamental relation between f, λ, and c (in a vacuum) is: λ = c/f

![](../static/CN_3_5_1.png)



# Communication Satellites
# Digital Modulation and Multiplexing
# Public Switched Telephone Network
# Mobile Telephone System
# Cable Television



# Physical media

- bit: propagates between transmitter/receiver pairs
- physical link: what lies between transmitter & receiver
- guided media:
  - signals propagate in solid media: copper, fiber, coax
- unguided media:
  - signals propagate freely, e.g., radio

- Host: sends packets of data
  - takes application message
  - breaks into smaller chunks, known as packets, of length **L** bits
  - transmits packet into access network at transmission rate **R**
    - link transmission rate, aka link **capacity**, aka _**link bandwidth**_

todo: add images


</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 4 | ???</summary>




</details>

---


