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
- The exam will be on Feb. 215h during the class time.
- No midterm deferral, marks will be added to the final exam

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

### Local Area Networks (LAN)
Connect devices **in a home or office building**
- If it is used in a company, it is called enterprise network

### Metropolitan Area Networks (MAN)
Connect devices **over a metropolitan area (city)**
Example: MAN based on cable TV network:
- Also delivers Internet

### Wide Area Networks (one images for each)
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

## Cloud (Infrastructure as a Service)

# Network Scurity
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
Body Area Examples
ITU
International Telecommunication Union
Telecommunications G.992, ADSL
H.264, MPEG4
IEEE
Institute of Electrical and Electronics Engineers
Communications 802.3, Ethernet
802.11, WiFi
IETF
Internet Engineering Task Force
Internet RFC 2616, HTTP/1.1
RFC 1034/1035,
DNS
W3C
World Wide Web Consortium
Web HTML5 standard
CSS standard
53

</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 2 | Network Software</summary>




</details>

---
