# Part - A (2M)

### 1. State uses of C.N:
- Information and Resource Sharing
- Retrieving Remote Information
- Speedy Interpersonal Communication
- E-Commerce
- Highly Reliable Systems
- Cost–Effective Systems
- VoIP - Voice over Internet protocol

### 2. Why do you need router:
- Routers allow multiple computers to share a common Internet connection from your ISP, allowing you to take a laptop into another room and still have Internet access. 
- They also put your computers onto a local network, allowing you to share files and printers between them. 
- A router creates a local area network within your house, allowing your devices to share files and peripherals like printers.

### 3. Types of Topology:
- Bus Topology
- Star Topology
- Mesh Topology 
- Ring Topology
- Tree Topology
- Hybrid Topology
- Point to Point Topology

### 4. What is Ethernet:
- A communication technology used to connect devices in a wired local area network (LAN) or wide area network (WAN).
-  Enables devices to communicate with each other via a protocol, which is a set of rules or common network language.
- Ethernet has since been refined to support higher bit rates, a greater number of nodes, and longer link distances, but retains much backward compatibility.

### 5. Diff. btw 

| <font color="#ff0000">Circuit Switching </font>                                                                                             | <font color="#f79646">Packet Switching </font>                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| More reliable.                                                                                                                              | Less reliable                                                                                                    |
| A communication method where a dedicated communication path, or circuit, is established between two devices before data transmission begins | A communication method where data is divided into smaller units called packets and transmitted over the network. |
| Data is processed at the source system only                                                                                                 | Data is processed at all intermediate nodes including the source system.                                         |
| It is not a store and forward technique                                                                                                     | It is a store and forward technique.                                                                             |
| Transmission of the data is done by the source.                                                                                             | Transmission of the data is done not only by the source but also by the intermediate routers.                    |
| Implemented at the physical layer                                                                                                           | Implemented at the datalink layer and network layer                                                              |
| Requires simple protocols for delivery                                                                                                      | Requires complex protocols for delivery                                                                          |
### 6. TCP vs UDP:
| Basis           | Transmission Control Protocol (TCP)                                                                                                                                                                                                                                                                                | User Datagram Protocol (UDP)                                                                                                                                                                                                                                                                                                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Type of Service | [TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/) is a connection-oriented protocol.                                                                                                                                                                                                 | [UDP](https://www.geeksforgeeks.org/user-datagram-protocol-udp/) is the Datagram-oriented protocol.                                                                                                                                                                                                                                                                                               |
| Reliability     | TCP is reliable as it guarantees the delivery of data to the destination router.                                                                                                                                                                                                                                   | The delivery of data to the destination cannot be guaranteed in UDP.                                                                                                                                                                                                                                                                                                                              |
| Acknowledgment  | An acknowledgment segment is present.                                                                                                                                                                                                                                                                              | No acknowledgment segment.                                                                                                                                                                                                                                                                                                                                                                        |
| Speed           | TCP is comparatively slower than UDP.                                                                                                                                                                                                                                                                              | UDP is faster, simpler, and more efficient than TCP.                                                                                                                                                                                                                                                                                                                                              |
| Retransmission  | Retransmission of lost packets is possible in TCP, but not in UDP.                                                                                                                                                                                                                                                 | There is no retransmission of lost packets in the User Datagram Protocol (UDP).                                                                                                                                                                                                                                                                                                                   |
| Header Length   | 20-60 bytes variable length header.                                                                                                                                                                                                                                                                                | 8 bytes fixed-length header.                                                                                                                                                                                                                                                                                                                                                                      |
| Weight          | TCP is heavy-weight.                                                                                                                                                                                                                                                                                               | UDP is lightweight.                                                                                                                                                                                                                                                                                                                                                                               |
| Broadcasting    | TCP doesn’t support Broadcasting.                                                                                                                                                                                                                                                                                  | UDP supports Broadcasting.                                                                                                                                                                                                                                                                                                                                                                        |
| Protocols       | TCP is used by [HTTP, HTTPs](https://www.geeksforgeeks.org/difference-between-http-and-https-2/), [FTP](https://www.geeksforgeeks.org/file-transfer-protocol-ftp/), [SMTP](https://www.geeksforgeeks.org/simple-mail-transfer-protocol-smtp/) and [Telnet](https://www.geeksforgeeks.org/introduction-to-telnet/). | UDP is used by [DNS](https://www.geeksforgeeks.org/details-on-dns/), [DHCP](https://www.geeksforgeeks.org/dynamic-host-configuration-protocol-dhcp/), TFTP, [SNMP](https://www.geeksforgeeks.org/simple-network-management-protocol-snmp/), [RIP](https://www.geeksforgeeks.org/routing-information-protocol-rip/), and [VoIP](https://www.geeksforgeeks.org/voice-over-internet-protocol-voip/). |
| Stream Type     | The TCP connection is a byte stream.                                                                                                                                                                                                                                                                               | UDP connection is a message stream.                                                                                                                                                                                                                                                                                                                                                               |
| Overhead        | Low but higher than UDP.                                                                                                                                                                                                                                                                                           | Very low.                                                                                                                                                                                                                                                                                                                                                                                         |
| Applications    | Safe and trustworthy communication procedure is necessary, such as in email, on the web surfing, and in military services.                                                                                                                                                                                         | VoIP, game streaming, video, and music streaming, etc.                                                                                                                                                                                                                                                                                                                                            |
### 7. four common data compression techniques used in computer networks:
- Run-Length Encoding (RLE)
- Huffman Coding
- Lempel-Ziv-Welch (LZW) Compression
- Deflate Compression

# Part - B

### 11. OSI reference model:

- OSI - Open Systems Interconnection. 
- It is a 7-layer architecture with each layer having specific functionality to perform. 
- All these 7 layers work collaboratively to transmit the data from one person to another across the globe. 
- OSI model was developed by ISO – ‘International Organization for Standardization‘, in the year 1984.

#### PDNTSPA

| <font color="#f79646">Layers No.</font> | <font color="#92d050">Layers Name</font> | <font color="#ff0000">Function</font>                                        |
| --------------------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------- |
| Layer 1                                 | Physical Layer (LOWEST)                  | Transmission method used to propagate bits through a network                 |
| Layer 2                                 | Data Link Layer                          | Frame formatting for transmitting data across a physical communication line. |
| Layer 3                                 | Network Layer                            | Network addressing and packet transmission on the network.                   |
| Layer 4                                 | Transport Layer                          | Data tracking as it moves through a network.                                 |
| Layer 5                                 | Session Layer                            | Job management tracking                                                      |
| Layer 6                                 | Presentation Layer                       | Encoding the language used in transmission.                                  |
| Layer 7                                 | Application Layer (HIGHEST)              | User networking applications and interfacing to the network.                 |

   1. Physical Layer:
      1. Responsibility is hop-to-hop delivery of bits.
      2. Physical Topology
      3. Transmission mode
   2. Data link Layer:
      1. Responsibility is hop-to-hop delivery of frames.
      2. Uses Physical address called MAC adderss associated with Metwork Interface Card (NIC)
      3. Hop-to-hop flow & Errro control.
   3. Network Layer:
      1. Responsibel for End to end delivery of individual packets.
      2. The sender and receiver are identified by using a logical address or IP address.
   4. Transport Layer:
      1. Flow Control − It keeps a fast transmitter from flooding a slow receiver.
      2. Error Control − To retransmit the damaged segments.
   5. Session Layer:
      1. Responsobilities:
         1. Network log-on and log-off procedures
         2. User authentication
         3. Determines the type dialog available − simplex, half-duplex, and full-duplex.
   6. Presentation Layer:
      1. Deals how data is presented to the network.
      2. Responsibilities:
         1. Translation
         2. COmpression
         3. Encryption
   7. Application Layer:
      1. 7th and topmost layer
      2. Very close to user
      3. uses WWW to aloow the web browsers to request documents from web servers
      4. Holds protocol services such as HTTP.

### 12. Ethernet Frame Format:

https://www.geeksforgeeks.org/ethernet-frame-format/

- Basic frame format which is required for all MAC implementation is defined in IEEE 802.3 standard. 
- Though several optional formats are being used to extend the protocol’s basic capability.
- Ethernet frame starts with Preamble and SFD, both work at the physical layer. 
- Ethernet header contains both the Source and Destination MAC address, after which the payload of the frame is present. 
- The last field is CRC which is used to detect the error. Now, let’s study each field of basic frame format.

<img alt="Ethernet Frame Format" src="Pasted image 20240323195703.png" />

![[Pasted image 20240323195703.png]]

1. **PREAMBLE –** 
	1. Ethernet frame starts with a 7-Bytes Preamble. 
	2. This is a pattern of alternative 0’s and 1’s which indicates starting of the frame and allow sender and receiver to establish bit synchronization. 
	3. Initially, PRE (Preamble) was introduced to allow for the loss of a few bits due to signal delays. 
	4. But today’s high-speed Ethernet doesn’t need Preamble to protect the frame bits. 
	5. PRE (Preamble) indicates the receiver that frame is coming and allow the receiver to lock onto the data stream before the actual frame begins.
2. **Start of frame delimiter (SFD) –** 
	1. This is a 1-Byte field that is always set to 10101011. 
	2. SFD indicates that upcoming bits are starting the frame, which is the destination address. 
	3. Sometimes SFD is considered part of PRE, this is the reason Preamble is described as 8 Bytes in many places. 
	4. The SFD warns station or stations that this is the last chance for synchronization.
3. **Destination Address –** 
	1. This is a 6-Byte field that contains the MAC address of the machine for which data is destined.
4. **Source Address –** 
	1. This is a 6-Byte field that contains the MAC address of the source machine. 
	2. As Source Address is always an individual address (Unicast), the least significant bit of the first byte is always 0.
5. **Length –** 
	1. Length is a 2-Byte field, which indicates the length of the entire Ethernet frame. 
	2. This 16-bit field can hold a length value between 0 to 65534, but length cannot be larger than 1500 Bytes because of some own limitations of Ethernet.
6. **Data –** 
	1. This is the place where actual data is inserted, also known as **Payload**. 
	2. Both IP header and data will be inserted here if Internet Protocol is used over Ethernet. 
	3. The maximum data present may be as long as 1500 Bytes. 
	4. In case data length is less than minimum length i.e. 46 bytes, then padding 0’s is added to meet the minimum possible length.
7. **Cyclic Redundancy Check (CRC) –** 
	1. CRC is 4 Byte field. 
	2. This field contains a 32-bits hash code of data, which is generated over the Destination Address, Source Address, Length, and Data field. 
	3. If the checksum computed by destination is not the same as sent checksum value, data received is corrupted.
8. **VLAN Tagging –** 
	1. The Ethernet frame can also include a VLAN (Virtual Local Area Network) tag, which is a 4-byte field inserted after the source address and before the EtherType field. 
	2. This tag allows network administrators to logically separate a physical network into multiple virtual networks, each with its own VLAN ID.
9. **Jumbo Frames –** 
	1. In addition to the standard Ethernet frame size of 1518 bytes, some network devices support Jumbo Frames, which are frames with a payload larger than 1500 bytes. 
	2. Jumbo Frames can increase network throughput by reducing the overhead associated with transmitting a large number of small frames.
10. **Ether Type Field –** 
	1. The EtherType field in the Ethernet frame header identifies the protocol carried in the payload of the frame. 
	2. For example, a value of 0x0800 indicates that the payload is an IP packet, while a value of 0x0806 indicates that the payload is an ARP (Address Resolution Protocol) packet.
11. **Multicast and Broadcast Frames –**  
	1. In addition to Unicast frames (which are sent to a specific destination MAC address), Ethernet also supports Multicast and Broadcast frames. 
	2. Multicast frames are sent to a specific group of devices that have joined a multicast group, while Broadcast frames are sent to all devices on the network.
12. **Collision Detection –** 
	1. In half-duplex Ethernet networks, collisions can occur when two devices attempt to transmit data at the same time. 
	2. To detect collisions, Ethernet uses a Carrier Sense Multiple Access with Collision Detection (CSMA/CD) protocol, which listens for activity on the network before transmitting data and backs off if a collision is detected.

### Advantages:

1. **Simple format:** 
2. **Flexibility:** 
3. **Widely adopted:** 
4. **Error detection:** 
5. **Support for VLANs:**

### Disadvantages:

1. **Limited frame size:** 
2. **Broadcast storms:**
3. **Security vulnerabilities:** 
4. **Limited speed:** 
5. **Limited distance:**

### 13. IPV4 Datagram header format:

https://www.geeksforgeeks.org/introduction-and-ipv4-datagram-header/

**IPv4:** 
- IPv4 - Internet Protocol Version 4
- IPv4 is a connectionless protocol used for packet-switched networks. 
- It operates on a best-effort delivery model, in which neither delivery is guaranteed, nor proper sequencing or avoidance of duplicate delivery is assured. 
- Internet Protocol Version 4 (IPv4) is the fourth revision of the Internet Protocol and a widely used protocol in data communication over different kinds of networks. 
- IPv4 is a <span style="background:#fff88f">connectionless protocol used in packet-switched layer networks, such as Ethernet.</span> 
- It provides a logical connection between network devices by providing identification for each device. 
- There are many ways to configure IPv4 with all kinds of devices – including manual and automatic configurations – depending on the network type. 
- IPv4 is defined and specified in IETF publication RFC 791. IPv4 uses 32-bit addresses for Ethernet communication in five classes: A, B, C, D and E. 
- Classes A, B and C have a different bit length for addressing the network host. 
- Class D addresses are reserved for multicasting, while class E addresses are reserved for military purposes. IPv4 uses 32-bit (4-byte) addressing, which gives 232 addresses. 
- IPv4 addresses are written in the dot-decimal notation, which comprises of four octets of the address expressed individually in decimal and separated by periods, for instance, 192.168.1.5.

### 14. TCP Congestion Control:

https://www.geeksforgeeks.org/tcp-congestion-control/

- TCP congestion control is a method used by the TCP protocol to manage data flow over a network and prevent congestion. 
- TCP uses a congestion window and congestion policy that avoids congestion. 
- Previously, we assumed that only the receiver could dictate the sender’s window size. 
- We ignored another entity here, the network. 
- If the network cannot deliver the data as fast as it is created by the sender, it must tell the sender to slow down. 
- In other words, in addition to the receiver, the network is a second entity that determines the size of the sender’s window 
##### Congestion Policy in TCP

1. **Slow Start Phase:** Starts slow increment is exponential to the threshold.
2. **Congestion Avoidance Phase:** After reaching the threshold increment is by 1.
3. **Congestion Detection Phase:** The sender goes back to the Slow start phase or the Congestion avoidance phase.

# Part - C

### 15. How can you determine the mini. & maxi. prize of TCP package, Calculate the Maximum size and no. of a package of a payload when a 1000 bytes message is forwarded to a router:

<span style="background:#ff4d4f">BEWARE of ChatGPT</span>

we need to consider several factors:

1. TCP Header Size: 
	1. The TCP header consists of various fields such as source and destination port numbers, sequence number, acknowledgment number, header length, flags, window size, checksum, and urgent pointer. 
	2. The size of the TCP header varies depending on the options present and can range from 20 to 60 bytes.
    
2. Maximum Transmission Unit (MTU): 
	1. MTU is the maximum size of the data payload that can be transmitted in a single packet over a network. 
	2. It is determined by the underlying network technology and can vary. 
	3. For example, Ethernet has an MTU of 1500 bytes, while some other networks may have different MTU sizes.
    
3. IP Header Size: 
	1. TCP operates over IP, so each TCP packet also includes an IP header, which contains information such as source and destination IP addresses, protocol version, header length, type of service, total length, identification, flags, fragment offset, time to live, protocol, header checksum, and source and destination addresses. 
	2. The size of the IP header is typically 20 bytes but can be larger if options are present.
    
4. Overhead: 
	1. Overhead includes any additional bytes added to the packet for error detection, encryption, or other purposes.

<font color="#de7802">**To calculate the maximum size and number of packets required to transmit a 1000-byte message to a router, we follow these steps:**</font>

- Step 1: 
	- Determine the size of the TCP header, IP header, and any additional overhead.
- Step 2: 
	- Subtract the total size of the headers and overhead from the MTU to calculate the maximum payload size that can be transmitted in a single packet.
- Step 3: 
	- Divide the size of the 1000-byte message by the maximum payload size calculated in Step 2 to determine the number of packets required to transmit the entire message.

Let's illustrate this with an example:

Assuming:

- TCP header size: 20 bytes
- IP header size: 20 bytes
- Additional overhead: 0 bytes (for simplicity)
- MTU: 1500 bytes (for Ethernet)

- Step 1: 
	- Total header size = TCP header size + IP header size Total header size 
	- = 20 bytes (TCP) + 20 bytes (IP) 
	- = 40 bytes

- Step 2: 
	- Maximum payload size = MTU - Total header size Maximum payload size 
	- = 1500 bytes - 40 bytes 
	- = 1460 bytes

- Step 3: 
	- Number of packets required = Total message size / Maximum payload size Number of packets required 
	- = 1000 bytes / 1460 bytes 
	- ≈ 0.6849

Since we cannot transmit a fraction of a packet, we round up to the nearest whole number.

Number of packets required = 1 packet (as we need at least 1 packet to transmit the message)

In summary, to transmit a 1000-byte message to a router using TCP packets with an MTU of 1500 bytes, we would need to divide the message into 1 packet, with a maximum payload size of 1460 bytes.