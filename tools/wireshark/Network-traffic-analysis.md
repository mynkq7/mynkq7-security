
# Network Traffic Analysis

## Network Traffic Analysis — Wireshark

### Overview

- **Wireshark**: Packet analyzer / traffic sniffer
- **Type**: Open-source
- **Platform**: Cross-platform
- **Interface**: GUI-based

---

## Data Packet Capturing Structure

### Top Frame (Packet List)

| Field | Description |
| --- | --- |
| Number | Packet sequence number |
| Time | Timestamp when packet was captured |
| Source | Source IP address |
| Destination | Destination IP address |
| Protocol | Communication protocol used |
| Length | Packet size in bytes |
| Info | Summary of packet contents |

---

### Middle Frame (Packet Details)

- **Frame** — General frame information
- **Linux Cooked Capture** — Link-layer information
- **Internet Protocol Version (IPv4/IPv6)** — Source & Destination IP addresses
- **Transmission Control Protocol (TCP)** — Source port, Destination port, Sequence number, Length

---

### Bottom Frame (Packet Data)

- Displays **raw data / payload** in hexadecimal and ASCII formats

---

## Wireshark Filters

### Filter Types

- **Display Filter**: Filters packets displayed in the capture window
- **Capture Filter**: Filters packets before they are captured
- **GUI Filter Builder**: Create filters visually using the GUI

---

## Common Filter Examples

### TCP/UDP Filters

```
tcp.port == 80
tcp.srcport == 443
tcp.port == 443 or tcp.port == 80
tcp.port in {80 443 8080}
tcp
udp

```

---

### IP Address Filters

```
ip.addr == 192.168.1.1
!(ip.addr == 192.168.1.1)

```

---

### Web Traffic Filters

```
http.request.url == "https://demo.testfire.net"
http.host matches "acme.(org|com|net)"
http.response.code == 200
http.request.method == "GET"
tcp contains "admin"

```

---

### Example Target IP

```
ip.addr == 172.16.2.36

```

capturing traffc from any specific file 

first do ping to the site you wnat to cpature the traffic by using 

ping 
ping [www.google.com](http://www.google.com) result (ip address of site →142.250.193.36)

then filter in wireshark 
ip.addr == 142.250.193.36

tcp and ip.addr == 142.250.193.36 or udp and  ip.addr == 142.250.193.36
capturing passsword