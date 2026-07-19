
# Networking

## OSI Model


## 1. Physical Layer

- Converts bits into electrical, optical, or radio signals and transmits them through physical media.
## 2. Data Link Layer

- Handles node-to-node data transfer between devices on the same network. 
- Uses MAC addresses for communication within the same network.

### Protocols 

- **Ethernet**: The standard protocol for LANs. It uses MAC addresses to identify physical devices.
- **Wi-Fi**: The standard protocol for WLANs. It manages media access and helps prevent signal collisions using **CSMA/CA**.

## 3. Network Layer

- Routes packets between different networks by determining the most efficient path.

###Protocols

- **IP(Internet Protocol)** : Provides logical addressing and routes packets between different networks.to another.
- **ICMP**: a network layer protocol used by network devices such as routers to send error messages and operational information.
### Example: Used by the ping command to test connectivity.

## 4. Transport Layer

- Handles end-to-end data transmission using **TCP** and **UDP** protocols.

## Protocols ##

### TCP vs UDP

| TCP  | UDP |
|------|------|
| Connection-oriented| Connectionless |
| Reliable              | Less reliable |
| Slower                | Faster |
| Performs error checking and retransmission  | No retransmission |
| Used for HTTP, HTTPS, SSH, FTP | Used for DNS, VoIP, Streaming, Gaming |

## 5. Session Layer

- Responsible for Establishing, managing , and terminating communication sessions between devices.

### Examples
- Zoom
- Microsoft Teams
- Remote Desktop

## 6. Presentation Layer

- Responsible for data translation, encryption, and compression.

 ### Examples
- SSL/TLS
- JPEG
- PNG
- MP3

## 7. Application Layer

- Provides network services directly to end-user applications and enables user interaction with the network.

 ## Protocols ##
- HTTP
- HTTPS
- DNS
- FTP
- SMTP
- SSH

---------
### Data Flow

Sender

Application
↓
Presentation
↓
Session
↓
Transport
↓
Network
↓
Data Link
↓
Physical

Receiver

Physical
↑
Data Link
↑
Network
↑
Transport
↑
Session
↑
Presentation
↑
Application

-----------

## PDU (Protocol Data Unit)

| Layer | PDU |
|-------|-----|
| Application | Data |
| Presentation | Data |
| Session | Data |
| Transport | Segment (TCP) / Datagram (UDP) |
| Network | Packet |
| Data Link | Frame |
| Physical | Bits |