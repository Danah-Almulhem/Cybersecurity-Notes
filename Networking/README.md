
#Networking

##OSI Model


## 1. Physical Layer

- Converts data into bits and transmits them across physical network media.

## 2. Data Link Layer

- Handles node-to-node data transfer between devices on the same network.

##Protocols##

- **Ethernet**: The standard protocol for LANs. It uses MAC addresses to identify physical devices.
- **Wi-Fi**: The standard protocol for WLANs. It manages media access and helps prevent signal collisions using **CSMA/CA**.

## 3. Network Layer

- Routes packets between different networks by determining the most efficient path.

##Protocols##

-**IP**: set of rules that allows computers and other devices to communicate over the Internet.and ensures that information sent from one divice to another.
-**ICMP**: a network layer protocol used by network devices such as routers to send error messages and operational information.


## 4. Transport Layer

- Handles end-to-end data transmission using **TCP** and **UDP** protocols.

##Protocols##

### TCP vs UDP

| TCP                   | UDP |
|------|                ------|
| Connection-oriented   | Connectionless |
| Reliable              | Less reliable |
| Slower                | Faster |
| Performs error checking and retransmission  | No retransmission |
| Used for HTTP, HTTPS, SSH, FTP | Used for DNS, VoIP, Streaming, Gaming |

## 5. Session Layer

- Establishes, manages, and terminates communication sessions between devices.

##Examples##
- Zoom
- Microsoft Teams
- Remote Desktop

## 6. Presentation Layer

- Translates, encrypts, and compresses data into a format that applications can understand.

 ##Examples##
- SSL/TLS
- JPEG
- PNG
- MP3

## 7. Application Layer

- Provides network services directly to end-user applications.

 ##Protocols##
- HTTP
- HTTPS
- DNS
- FTP
- SMTP
- SSH