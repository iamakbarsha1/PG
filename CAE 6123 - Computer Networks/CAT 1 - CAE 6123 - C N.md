2M

1. Unicast & Multicast communication:
   1. Unicast:
      1. Source node sends a msg to a single destination node
   2. Multicast:
      1. Source node sends a msg to some sudset of other nodes but not to entire nodes/network
2. List 2 Error detection Mechanisms:
   1. Msg is corrupted, the sender may retransmit.
   2. An error correction algorithm used to recover the correct msg.
3. List of Topology:
   1. Physical Topology
      1. Bus
      2. Ring
      3. Star
      4. Mesh
   2. Logical Topology
4. Bluetooth Network:
   1. Wireless LAN technology
   2. Simply follows the principle of transmitting and receiving data using radio waves.
   3. When two devices start to share data, they form a network called <font color="#ff0000">piconet</font> which can further accommodate more than five devices.

10M & 5M:

1. Circuit & Packet Switching:

| <font color="#ff0000">Circuit Switching </font>                                                                                             | <font color="#f79646">Packet Switching </font>                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | --- | --- |
| More reliable.                                                                                                                              | Less reliable                                                                                                    |
| A communication method where a dedicated communication path, or circuit, is established between two devices before data transmission begins | A communication method where data is divided into smaller units called packets and transmitted over the network. |
| Data is processed at the source system only                                                                                                 | Data is processed at all intermediate nodes including the source system.                                         |
| It is not a store and forward technique                                                                                                     | It is a store and forward technique.                                                                             |
| Transmission of the data is done by the source.                                                                                             | Transmission of the data is done not only by the source but also by the intermediate routers.                    |
| Implemented at the physical layer                                                                                                           | Implemented at the datalink layer and network layer                                                              |
| Requires simple protocols for delivery                                                                                                      | Requires complex protocols for delivery                                                                          |     |     |

---

2. OSI Layers:

| <font color="#f79646">Layers No.</font> | <font color="#92d050">Layers Name</font> | <font color="#ff0000">Function</font>                                        |
| --------------------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------- |
| Layer 1                                 | Physical Layer (LOWEST)                  | Transmission method used to propagate bits through a network                 |
| Layer 2                                 | Data Link Layer                          | Frame formatting for transmitting data across a physical communication line. |
| Layer 3                                 | Network Layer                            | Network addressing and packet transmission on the network.                   |
| Layer 4                                 | Transport Layer                          | Data tracking as it moves through a network.                                 |
| Layer 5                                 | Session Layer                            | Job management tracking                                                      |
| Layer 6                                 | Presentation Layer                       | Encoding the language used in transmission.                                  |
| Layer 7                                 | Application Layer (HIGHEST)              | User networking applications and interfacing to the network.                 |

2. <font color="#ff0000">OSI Layers:</font>

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

---

2. Lost Token & Orphan Token:
   1. Lost token:
      1. Keeps tracks of when the token last passed by and how long it's been since then.
      2. Token is lost and fresh token is introduced into the ring if maxTRT is exceeded.
      3. TRT - Token Rotation Time
      4. THT = n \* THT (n = no. of stations on the ring)
   2. Orphan Token:
      1. If sending stations fails to drain its frame, the frame becomes orphaned.

---

4. Types of wireless networks:
   1. <font color="#ff0000">4 types:</font>
      1. wireless LAN (Local Area Network)
      2. wireless MAN (Metropolitan Area Network)
      3. wireless PAN (Personal Area Network)
      4. wireless WAN (Wide Area Network)
   2. Wireless Local Area Network:
      1. Provides internet access within a building or a limited outdoor area.
      2. Used in offices and homes
   3. Wireless Metropolitan Area Network:
      1. Installed in cities worldwide to provide access for people outside an office or home network
   4. Wireless Personal Area Network:
      1. cover a very limited area -- typically a maximum of 100 meters for most applications,
      2. <font color="#ff0000">Eg:</font> Bluetooth
   5. Wireless Wide Area Network:
      1. Provide access outside the range of a wireless LAN or metropolitan network.
      2. <font color="#ff0000">Eg:</font> Users can also connect to the internet to access websites or server-based applications.
