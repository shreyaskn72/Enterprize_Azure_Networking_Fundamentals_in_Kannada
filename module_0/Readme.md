
# ಮಾಡ್ಯೂಲ್ 0 – Cloud Networking Fundamentals

> **ಈ ಮಾಡ್ಯೂಲ್‌ನ ಉದ್ದೇಶ**
>
> Azure, AWS ಅಥವಾ ಯಾವುದೇ Cloud Platform ಬಳಸುವ ಮೊದಲು, ಕಂಪ್ಯೂಟರ್‌ಗಳು ಪರಸ್ಪರ ಹೇಗೆ ಮಾತನಾಡುತ್ತವೆ (Communicate) ಎಂಬ ಮೂಲಭೂತ ಕಲ್ಪನೆಗಳನ್ನು ಅರ್ಥಮಾಡಿಕೊಳ್ಳುವುದು.

Cloud Networking ಎಂಬುದು ಹೊಸ ವಿಷಯವಲ್ಲ. ಅದು ನಾವು ಈಗ ಕಲಿಯಲಿರುವ Networking Concepts ಗಳನ್ನೇ Cloud ನಲ್ಲಿ ಬಳಸುತ್ತದೆ.

---

# 0.1 Computers ಹೇಗೆ Communication ಮಾಡುತ್ತವೆ?

ಒಂದು ಸರಳ ಉದಾಹರಣೆ ತೆಗೆದುಕೊಳ್ಳೋಣ.

ನೀವು ನಿಮ್ಮ ಸ್ನೇಹಿತನಿಗೆ ಒಂದು ಉಡುಗೊರೆ (Gift) ಕಳುಹಿಸಬೇಕು ಎಂದು ಊಹಿಸಿ.

ಅದಕ್ಕಾಗಿ ನಿಮಗೆ ಏನು ಬೇಕು?

* ನಿಮ್ಮ ಸ್ನೇಹಿತನ ಮನೆ ವಿಳಾಸ
* ನಿಮ್ಮ ಮನೆ ವಿಳಾಸ
* Courier Service
* ರಸ್ತೆ (Road)
* Parcel

Networking ಕೂಡ ಇದೇ ರೀತಿಯಲ್ಲಿ ಕೆಲಸ ಮಾಡುತ್ತದೆ.

ಇಲ್ಲಿ:

* Parcel = **Data**
* ಮನೆ ವಿಳಾಸ = **IP Address**
* ರಸ್ತೆ = **Network**
* Courier = **Routers ಮತ್ತು Switches**

ಒಂದು Computer ಮತ್ತೊಂದು Computer ಗೆ ಮಾಹಿತಿ ಕಳುಹಿಸುವಾಗ, ಇದೇ ರೀತಿಯ ಪ್ರಕ್ರಿಯೆ ನಡೆಯುತ್ತದೆ.

---

## OSI Model (High Level)

Networking ತುಂಬಾ ದೊಡ್ಡ ವಿಷಯ.

ಅದನ್ನು ಸುಲಭವಾಗಿ ಅರ್ಥಮಾಡಿಕೊಳ್ಳಲು Engineers ಅದನ್ನು **7 Layers** ಆಗಿ ವಿಭಜಿಸಿದ್ದಾರೆ.

```
Application
Presentation
Session
Transport
Network
Data Link
Physical
```

ಈ ಎಲ್ಲ Layers ಅನ್ನು ಈಗ ನೆನಪಿಡುವ ಅಗತ್ಯವಿಲ್ಲ.

Cloud Engineer ಆಗಿ ನಿಮಗೆ ಮುಖ್ಯವಾಗಿ ತಿಳಿದಿರಬೇಕಾದ Layers ಇವು:

### Physical Layer

Data ಯಾವ ಮಾಧ್ಯಮದ ಮೂಲಕ ಹೋಗುತ್ತದೆ?

* Ethernet Cable
* Fiber Cable
* WiFi Signals

ಇದನ್ನು ರಸ್ತೆ (Road) ಎಂದು ಊಹಿಸಿ.

---

### Data Link Layer

ಒಂದೇ Local Network ಒಳಗೆ ಯಾವ Device ಗೆ Data ಹೋಗಬೇಕು ಎಂಬುದನ್ನು ನಿರ್ಧರಿಸುತ್ತದೆ.

ಇದು **MAC Address** ಬಳಸುತ್ತದೆ.

---

### Network Layer

ಬೇರೆ Network ಗಳಿಗೆ Data ಕಳುಹಿಸುವ Layer.

ಇದು **IP Address** ಬಳಸುತ್ತದೆ.

---

### Transport Layer

ಒಂದೇ Computer ನಲ್ಲಿ ಹಲವಾರು Applications ಇರಬಹುದು.

ಯಾವ Application ಗೆ Data ಹೋಗಬೇಕು ಎಂಬುದನ್ನು **Port Number** ಮೂಲಕ ನಿರ್ಧರಿಸುತ್ತದೆ.

---

### Application Layer

ನಾವು ಬಳಸುವ Applications.

ಉದಾಹರಣೆ:

* Chrome
* Firefox
* WhatsApp
* SSH
* Email

---

## TCP/IP Model

Internet ನಲ್ಲಿ OSI Model ನೇರವಾಗಿ ಬಳಸುವುದಿಲ್ಲ.

ಬದಲಿಗೆ TCP/IP Model ಬಳಸುತ್ತಾರೆ.

```
Application

Transport

Internet

Network Access
```

ಇದು OSI Model ನ ಸರಳ ರೂಪ.

Azure, AWS, Linux, Windows ಎಲ್ಲವೂ TCP/IP Model ಆಧರಿಸಿ ಕೆಲಸ ಮಾಡುತ್ತವೆ.

---

## Packet ಎಂದರೇನು?

ನೀವು 2 GB ಗಾತ್ರದ Video ಕಳುಹಿಸಬೇಕು ಎಂದು ಊಹಿಸಿ.

ಅದನ್ನು ಒಂದೇ ದೊಡ್ಡ File ಆಗಿ ಕಳುಹಿಸುವುದಿಲ್ಲ.

ಅದನ್ನು ಹಲವಾರು ಚಿಕ್ಕ ಭಾಗಗಳಾಗಿ ವಿಭಜಿಸಲಾಗುತ್ತದೆ.

```
Video

↓

Packet 1

Packet 2

Packet 3

Packet 4
```

ಈ ಪ್ರತಿಯೊಂದು ಚಿಕ್ಕ ಭಾಗವನ್ನು **Packet** ಎಂದು ಕರೆಯುತ್ತಾರೆ.

Destination ಗೆ ತಲುಪಿದ ನಂತರ ಮತ್ತೆ ಎಲ್ಲಾ Packets ಸೇರಿಸಿ ಮೂಲ File ಅನ್ನು ರಚಿಸಲಾಗುತ್ತದೆ.

---

## Frame ಎಂದರೇನು?

Packet ಒಂದು Network ನಿಂದ ಇನ್ನೊಂದು Network ಗೆ ಹೋಗುತ್ತದೆ.

ಆದರೆ Local Network ಒಳಗೆ Packet ಅನ್ನು **Frame** ರೂಪದಲ್ಲಿ ಕಳುಹಿಸಲಾಗುತ್ತದೆ.

```
Laptop

↓

WiFi Router

↓

Frame

↓

Switch
```

ಸರಳವಾಗಿ ಹೇಳುವುದಾದರೆ,

**Frame = Packet + Local Network ಮಾಹಿತಿ (MAC Address ಇತ್ಯಾದಿ)**

---

## Port ಎಂದರೇನು?

ಒಂದು Apartment Building ನಲ್ಲಿ ಹಲವಾರು ಮನೆಗಳು ಇರುತ್ತವೆ.

```
Building

↓

Flat 101

Flat 102

Flat 103
```

Computer = Building

Application = Flat

Port = Flat Number

ಒಂದು Computer ನಲ್ಲಿ Browser, MySQL, Redis, SSH ಎಲ್ಲವೂ ಒಂದೇ ಸಮಯದಲ್ಲಿ ಓಡಬಹುದು.

Data ಯಾವ Application ಗೆ ಹೋಗಬೇಕು ಎಂಬುದನ್ನು Port Number ತಿಳಿಸುತ್ತದೆ.

ಕೆಲವು ಸಾಮಾನ್ಯ Ports:

| Port | Service    |
| ---- | ---------- |
| 80   | HTTP       |
| 443  | HTTPS      |
| 22   | SSH        |
| 3306 | MySQL      |
| 5432 | PostgreSQL |
| 6379 | Redis      |

Azure NSG (Network Security Group) ಯಲ್ಲಿ ಈ Ports ಆಧರಿಸಿ Traffic ಅನ್ನು Allow ಅಥವಾ Block ಮಾಡಲಾಗುತ್ತದೆ.

---

## IP Address

ಪ್ರತಿಯೊಂದು Network Device ಗೆ ಒಂದು Address ಬೇಕು.

ಉದಾಹರಣೆ:

```
192.168.1.10
```

IP Address ಇಲ್ಲದಿದ್ದರೆ ಬೇರೆ Computer ನಿಮ್ಮನ್ನು ಹುಡುಕಲು ಸಾಧ್ಯವಾಗುವುದಿಲ್ಲ.

ಇದನ್ನು ನಿಮ್ಮ ಮನೆಯ ವಿಳಾಸ ಎಂದು ಊಹಿಸಬಹುದು.

---

## MAC Address

ಪ್ರತಿಯೊಂದು Network Card ಗೆ Manufacturer ನೀಡುವ Unique Hardware Address.

ಉದಾಹರಣೆ:

```
00:1A:2B:3C:4D:5E
```

MAC Address ಅನ್ನು Local Network ಒಳಗೆ ಮಾತ್ರ ಬಳಸುತ್ತಾರೆ.

IP Address ಅನ್ನು Internet ನಲ್ಲಿ ಬಳಸುತ್ತಾರೆ.

---

# 0.2 IP Addressing

## IPv4

IPv4 Address ನಾಲ್ಕು ಸಂಖ್ಯೆಗಳನ್ನೊಳಗೊಂಡಿರುತ್ತದೆ.

ಉದಾಹರಣೆ:

```
192.168.1.25
```

ಪ್ರತಿಯೊಂದು ಸಂಖ್ಯೆ 0 ರಿಂದ 255 ರವರೆಗೆ ಇರಬಹುದು.

---

## Public IP

Internet ನಿಂದ ನೇರವಾಗಿ ತಲುಪಬಹುದಾದ Address.

Azure VM ಗೆ Public IP ಕೊಟ್ಟರೆ, Internet ನಿಂದ SSH ಅಥವಾ Web Request ಕಳುಹಿಸಬಹುದು (Firewall ಅನುಮತಿಸಿದರೆ).

---

## Private IP

Private Network ಒಳಗೆ ಮಾತ್ರ ಬಳಸುವ Address.

ಉದಾಹರಣೆ:

```
10.x.x.x

172.16.x.x

192.168.x.x
```

Internet ನಿಂದ ನೇರವಾಗಿ ತಲುಪಲು ಸಾಧ್ಯವಿಲ್ಲ.

Azure VNet ಒಳಗಿನ VM ಗಳು ಸಾಮಾನ್ಯವಾಗಿ Private IP ಬಳಸಿ ಪರಸ್ಪರ ಮಾತನಾಡುತ್ತವೆ.

---

## CIDR Notation

Subnet ಅನ್ನು ಚಿಕ್ಕ ರೀತಿಯಲ್ಲಿ ಬರೆಯುವ ವಿಧಾನ.

ಉದಾಹರಣೆ:

```
10.0.0.0/24
```

ಇಲ್ಲಿನ **/24** ಎಂದರೆ Network ಭಾಗದ ಉದ್ದ.

Azure ನಲ್ಲಿ VNet ಮತ್ತು Subnet ಸೃಷ್ಟಿಸುವಾಗ CIDR Notation ಅನ್ನು ಬಳಸಲಾಗುತ್ತದೆ.

---

## Subnet Mask

IP Address ನ ಯಾವ ಭಾಗ Network ಅನ್ನು ಸೂಚಿಸುತ್ತದೆ ಮತ್ತು ಯಾವ ಭಾಗ Host ಅನ್ನು ಸೂಚಿಸುತ್ತದೆ ಎಂಬುದನ್ನು ತಿಳಿಸುತ್ತದೆ.

ಉದಾಹರಣೆ:

```
IP Address

192.168.1.25

Subnet Mask

255.255.255.0
```

ಇದರಿಂದ:

```
192.168.1

↓

Network

25

↓

Host
```

---

## Default Gateway

ನಿಮ್ಮ ಮನೆಯ ರಸ್ತೆಯಿಂದ National Highway ಗೆ ಹೋಗಲು ಒಂದು ಮುಖ್ಯ ರಸ್ತೆ ಇರುತ್ತದೆ.

Networking ನಲ್ಲಿ ಅದೇ ಕೆಲಸವನ್ನು **Default Gateway** ಮಾಡುತ್ತದೆ.

ಒಂದು Computer ಗೆ Destination ಎಲ್ಲಿದೆ ಎಂಬುದು ತಿಳಿಯದಿದ್ದರೆ, ಅದು Data ಅನ್ನು Default Gateway ಗೆ ಕಳುಹಿಸುತ್ತದೆ.

Gateway ನಂತರ ಸರಿಯಾದ ದಾರಿಯನ್ನು ಆಯ್ಕೆ ಮಾಡುತ್ತದೆ.

---

# 0.3 DNS

## DNS ಎಂದರೇನು?

ನಾವು Website ಗಳನ್ನು ಹೆಸರಿನಿಂದ ನೆನಪಿಡುತ್ತೇವೆ.

```
google.com
```

ಆದರೆ Computer ಗೆ ಹೆಸರು ಅರ್ಥವಾಗುವುದಿಲ್ಲ.

ಅದಕ್ಕೆ IP Address ಬೇಕು.

```
142.250.x.x
```

ಈ Name ಅನ್ನು IP Address ಗೆ ಪರಿವರ್ತಿಸುವ ವ್ಯವಸ್ಥೆಯೇ **DNS (Domain Name System)**.

ಇದನ್ನು Internet ನ Phone Book ಎಂದು ಊಹಿಸಬಹುದು.

---

## Recursive Lookup

ನೀವು Browser ನಲ್ಲಿ:

```
google.com
```

ಎಂದು ಟೈಪ್ ಮಾಡಿದಾಗ,

ನಿಮ್ಮ Computer ಮೊದಲು DNS Server ಅನ್ನು ಕೇಳುತ್ತದೆ:

> "google.com ಗೆ IP Address ಏನು?"

ಆ DNS Server ಗೆ ಉತ್ತರ ಗೊತ್ತಿಲ್ಲದಿದ್ದರೆ, ಅದು ಬೇರೆ DNS Server ಗಳನ್ನು ಸಂಪರ್ಕಿಸಿ ಸರಿಯಾದ ಉತ್ತರವನ್ನು ಹುಡುಕಿ ನಿಮ್ಮ Computer ಗೆ ನೀಡುತ್ತದೆ.

ಇದನ್ನೇ **Recursive Lookup** ಎನ್ನುತ್ತಾರೆ.

---

## A Record

ಒಂದು Domain Name ಅನ್ನು IPv4 Address ಗೆ ಸಂಪರ್ಕಿಸುತ್ತದೆ.

ಉದಾಹರಣೆ:

```
app.company.com

↓

10.0.0.5
```

---

## CNAME

ಒಂದು Domain Name ಅನ್ನು ಇನ್ನೊಂದು Domain Name ಗೆ ಸಂಪರ್ಕಿಸುತ್ತದೆ.

```
www.company.com

↓

company.com
```

---

## Private DNS

Private Network ಒಳಗೆ ಮಾತ್ರ ಬಳಸುವ DNS.

ಉದಾಹರಣೆ:

```
database.internal

↓

10.0.1.10
```

Azure VNet ಒಳಗಿನ Servers ಮಾತ್ರ ಇದನ್ನು Resolve ಮಾಡಬಹುದು.

---

# 0.4 Routing

Routing ಎಂದರೆ Data ಯಾವ ದಾರಿಯಲ್ಲಿ ಹೋಗಬೇಕು ಎಂದು ನಿರ್ಧರಿಸುವುದು.

ಈ ಕೆಲಸವನ್ನು Router ಮಾಡುತ್ತದೆ.

---

## Static Routing

Routes ಅನ್ನು ನಾವು ಕೈಯಾರೆ Configure ಮಾಡುತ್ತೇವೆ.

ಸರಳ Network ಗಳಲ್ಲಿ ಬಳಸುತ್ತಾರೆ.

---

## Dynamic Routing

Routers ತಾವೇ ಪರಸ್ಪರ Route ಮಾಹಿತಿಯನ್ನು ಹಂಚಿಕೊಳ್ಳುತ್ತವೆ.

ಹೊಸ ದಾರಿ ಸಿಕ್ಕರೆ ಅದನ್ನು ಸ್ವಯಂಚಾಲಿತವಾಗಿ ಬಳಸುತ್ತವೆ.

Cloud Providers ಇದೇ ವಿಧಾನವನ್ನು ವ್ಯಾಪಕವಾಗಿ ಬಳಸುತ್ತಾರೆ.

---

## Longest Prefix Match

ಒಂದು Destination ಗೆ ಹಲವು Routes ಇದ್ದರೆ,

ಅವುಗಳಲ್ಲಿ **ಅತ್ಯಂತ Specific Route** ಆಯ್ಕೆ ಮಾಡಲಾಗುತ್ತದೆ.

ಉದಾಹರಣೆ:

```
10.0.0.0/16

10.0.1.0/24
```

Destination:

```
10.0.1.50
```

ಆಗ `/24` Route ಆಯ್ಕೆ ಆಗುತ್ತದೆ, ಏಕೆಂದರೆ ಅದು ಹೆಚ್ಚು Specific.

---

# 0.5 NAT (Network Address Translation)

Private IP Address ಗಳನ್ನು Internet ಜೊತೆ ಸಂಪರ್ಕಿಸಲು NAT ಬಳಸಲಾಗುತ್ತದೆ.

---

## SNAT

Source IP Address ಅನ್ನು ಬದಲಾಯಿಸುತ್ತದೆ.

ಉದಾಹರಣೆ:

```
Private VM

10.0.0.4

↓

Internet

↓

Public IP

52.x.x.x
```

---

## DNAT

Destination IP Address ಅನ್ನು ಬದಲಾಯಿಸುತ್ತದೆ.

Internet ನಿಂದ Public IP ಗೆ ಬಂದ Request ಅನ್ನು Private VM ಗೆ Forward ಮಾಡುತ್ತದೆ.

---

## PAT

ಒಂದೇ Public IP ಅನ್ನು ಹಲವು Computers ಹಂಚಿಕೊಳ್ಳುವ ವಿಧಾನ.

ಇದಕ್ಕಾಗಿ Port Numbers ಬಳಸಲಾಗುತ್ತದೆ.

---

# 0.6 Firewalls

Firewall ಎಂದರೆ Network Security Guard.

ಯಾವ Traffic ಒಳಗೆ ಬರಬೇಕು ಮತ್ತು ಯಾವುದು ಬರಬಾರದು ಎಂಬುದನ್ನು ನಿರ್ಧರಿಸುತ್ತದೆ.

---

## Stateful Firewall

ಈ Firewall ಗೆ ಹಿಂದಿನ Connection ನೆನಪಿರುತ್ತದೆ.

ನೀವು ಹೊರಗೆ Request ಕಳುಹಿಸಿದರೆ, ಅದರ Response ಅನ್ನು ಸ್ವಯಂಚಾಲಿತವಾಗಿ ಒಳಗೆ ಬಿಡುತ್ತದೆ.

Azure Network Security Groups (NSGs) ಈ ತತ್ವವನ್ನು ಅನುಸರಿಸುತ್ತವೆ.

---

## Stateless Firewall

ಈ Firewall ಗೆ ಹಿಂದಿನ Connection ಬಗ್ಗೆ ನೆನಪಿರುವುದಿಲ್ಲ.

ಪ್ರತಿಯೊಂದು Packet ಅನ್ನು ಪ್ರತ್ಯೇಕವಾಗಿ ಪರಿಶೀಲಿಸುತ್ತದೆ.

---

## Allow / Deny Rules

Firewall ನಲ್ಲಿ Rules ಇರುತ್ತವೆ.

ಉದಾಹರಣೆ:

| Priority | Source   | Port | Action |
| -------- | -------- | ---- | ------ |
| 100      | Internet | 22   | Allow  |
| 200      | Internet | 80   | Allow  |
| 300      | Internet | 443  | Allow  |
| 4096     | Any      | Any  | Deny   |

Firewall ಈ Rules ಗಳನ್ನು ಕ್ರಮವಾಗಿ ಪರಿಶೀಲಿಸಿ, ಮೊದಲಿಗೆ ಹೊಂದುವ Rule ಅನ್ನು ಅನ್ವಯಿಸುತ್ತದೆ.

---

# protocols understanding

Please refer to this detailed explanation [protocols explanation](./1_Protocols_notes.md)

# ಮಾಡ್ಯೂಲ್ 0 ಸಾರಾಂಶ

ಈ ಮಾಡ್ಯೂಲ್ ಮುಗಿದ ನಂತರ ನಿಮಗೆ ಈ ಪ್ರಶ್ನೆಗಳಿಗೆ ಉತ್ತರ ಗೊತ್ತಿರಬೇಕು:

* Computer ಗಳು ಪರಸ್ಪರ ಹೇಗೆ Communication ಮಾಡುತ್ತವೆ?
* Packet ಮತ್ತು Frame ನಡುವಿನ ವ್ಯತ್ಯಾಸವೇನು?
* Port ಯಾಕೆ ಬೇಕು?
* IP Address ಮತ್ತು MAC Address ನಡುವಿನ ವ್ಯತ್ಯಾಸವೇನು?
* Public IP ಮತ್ತು Private IP ಯಾವಾಗ ಬಳಸುತ್ತಾರೆ?
* DNS ಹೇಗೆ ಕೆಲಸ ಮಾಡುತ್ತದೆ?
* Router ಹೇಗೆ Route ಆಯ್ಕೆ ಮಾಡುತ್ತದೆ?
* NAT ಯಾಕೆ ಬೇಕು?
* Firewall Network ಅನ್ನು ಹೇಗೆ ರಕ್ಷಿಸುತ್ತದೆ?

ಈ ಮೂಲಭೂತ Concepts ಅರ್ಥವಾದ ನಂತರ, **Azure Networking** (VNet, Subnet, NSG, Load Balancer, Private Endpoint, AKS Networking) ಕಲಿಯುವುದು ತುಂಬಾ ಸುಲಭವಾಗುತ್ತದೆ.
