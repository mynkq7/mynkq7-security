# **Network Concepts + Wireshark

---

## **1. TCP (Transmission Control Protocol)**

### **What is TCP?**

- TCP stands for Transmission Control Protocol.
- It is connection-oriented and ensures reliable, ordered, and accurate data delivery.
- Uses the **Three-Way Handshake**:
    - `SYN → SYN-ACK → ACK`

---

### **Advantages of TCP**

| Feature | Explanation |
| --- | --- |
| Reliable Data Transfer | Breaks data into segments and ensures delivery. |
| Error Recovery | Only missing segments are retransmitted. |
| Ordered Delivery | Reassembles segments in correct order. |
| Flow Control | Stops sender from overwhelming receiver. |
| Congestion Control | Adjusts sending speed during network congestion. |

---

### **TCP ACKs (Acknowledgments)**

- TCP does not send an ACK for each packet.
- Uses:
    - **Cumulative ACK** – Confirms all data received up to a point.
    - **Delayed ACK (~200ms)** – Waits briefly to send combined ACKs.

**Key Point:**

TCP may collect multiple packets and send a single cumulative ACK to reduce traffic.

---

### **Sequence and Acknowledgment Numbers**

```
Sequence Number: First byte of data being sent.
Acknowledgment Number: Next expected byte from sender.

Example:
Seq = 1 | Ack = 1 | Source Port = 4016 | Destination Port = 80

```

---

## **2. UDP (User Datagram Protocol)**

| TCP | UDP |
| --- | --- |
| Reliable, connection-oriented | Fast, connectionless |
| Error recovery and ordering | No retransmission, no ordering |
| Slower but accurate | Faster but less reliable |
| Used in web, file transfer | Used in streaming, games, VoIP |

---

## **3. Why Wireshark?**

- Manual packet analysis is not possible.
- Wireshark captures live network traffic and shows packet details such as:
    - TCP handshake
    - Sequence and ACK numbers
    - UDP, DNS, ICMP packets
    - Ports, IPs, and protocol-level data

---

## **4. Common Wireshark Filters**

| Filter | Purpose |
| --- | --- |
| tcp | Show all TCP packets |
| udp | Show all UDP packets |
| icmp | Show ping packets |
| dns | DNS requests and responses |
| !tcp | Show all non-TCP packets |
| dns.count.queries | Display DNS query count |

---

## **5. ICMP (Ping Process)**

- Sends 4 ICMP Echo Request packets.
- Destination replies with Echo Reply packets.
- Used to test host reachability.

---

## **6. DNS Query Process (google.com)**

1. You type `google.com` in the browser.
2. System checks local cache; if not found, sends DNS query.
3. DNS server replies with the IP address.
4. Browser uses this IP to start a TCP handshake.

---

## **7. Traceroute**

- Displays the path packets take across routers (hops).
- Helps identify where delay or failure occurs.

---

## **8. Complete Network Flow**

| Step | Description |
| --- | --- |
| DNS | Resolves domain name to IP address |
| TCP Handshake | Establishes reliable connection (SYN, SYN-ACK, ACK) |
| Data Transfer | Actual data sent using TCP or UDP |
| Termination | Connection closed using FIN/ACK |

---

## **9. OSI Model vs TCP/IP vs Wireshark**

| OSI Layer | TCP/IP Layer | What You See in Wireshark |
| --- | --- | --- |
| Application (HTTP, DNS) | Application | HTTP data, DNS queries, HTTPS info |
| Presentation | - | Encryption/formatting inside application data |
| Session | - | TCP sessions, port-to-port communication |
| Transport (TCP/UDP) | Transport | TCP segments, UDP datagrams, Seq/Ack, handshakes |
| Network (IP) | Internet | IP packets, IP addresses, TTL, ICMP |
| Data Link (Ethernet, MAC) | Network Access | Frames, MAC addresses, ARP |
| Physical | Physical | Not visible (electrical signals, cables) |

---

### **How Wireshark Maps Layers**

- Frame → Data Link Layer
- IP Packet → Network Layer
- TCP Segment or UDP Datagram → Transport Layer
- HTTP/DNS Data → Application Layer

---

## **Summary of Today's Learning**

- Understood TCP handshake, ACKs, sequence numbers.
- Learned how UDP differs from TCP.
- Understood DNS, ICMP (ping), and Traceroute.
- Mapped OSI and TCP/IP models and connected them with Wireshark.
- Now you know exactly which protocol and layer you studied and how Wireshark displays them.
