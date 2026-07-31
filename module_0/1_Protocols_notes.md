Protocols Networking ನಲ್ಲಿ ಅತ್ಯಂತ ಮುಖ್ಯವಾದ Concept. ಒಮ್ಮೆ ಇದನ್ನು ಅರ್ಥ ಮಾಡಿಕೊಂಡರೆ HTTP, HTTPS, TCP, UDP, DNS ಎಲ್ಲವೂ ಸುಲಭವಾಗಿ ಅರ್ಥವಾಗುತ್ತದೆ.

---

# Protocol ಎಂದರೇನು?

ನೀವು ನಿಮ್ಮ ಸ್ನೇಹಿತನ ಜೊತೆ Cricket ಆಡುತ್ತಿರುವಿರಿ ಎಂದು ಊಹಿಸಿ.

ಆಟ ಆರಂಭಿಸುವ ಮೊದಲು ಎಲ್ಲರೂ ಕೆಲವು Rules ಒಪ್ಪಿಕೊಳ್ಳುತ್ತಾರೆ.

* 6 Ball = 1 Over
* Four = 4 Runs
* Six = 6 Runs
* Three Stumps
* LBW Rule

ಈ Rules ಇಲ್ಲದಿದ್ದರೆ ಆಟ ನಡೆಯುವುದೇ ಇಲ್ಲ.

Networking ಕೂಡ ಇದೇ ರೀತಿ.

ಒಂದು Computer ಮತ್ತೊಂದು Computer ಜೊತೆ ಮಾತನಾಡಬೇಕಾದರೆ ಇಬ್ಬರೂ ಒಂದೇ Rules ಅನುಸರಿಸಬೇಕು.

ಈ Rules ಗಳನ್ನು **Protocols** ಎಂದು ಕರೆಯುತ್ತಾರೆ.

---

## ಒಂದು ನೈಜ ಉದಾಹರಣೆ

ಒಬ್ಬ ವ್ಯಕ್ತಿ Kannada ಮಾತ್ರ ಮಾತನಾಡುತ್ತಾನೆ.

ಇನ್ನೊಬ್ಬ ವ್ಯಕ್ತಿ Japanese ಮಾತ್ರ ಮಾತನಾಡುತ್ತಾನೆ.

ಇಬ್ಬರೂ ಪರಸ್ಪರ ಮಾತನಾಡಲು ಸಾಧ್ಯವೇ?

ಇಲ್ಲ.

ಏಕೆ?

ಯಾಕೆಂದರೆ Common Language ಇಲ್ಲ.

Networking ನಲ್ಲಿಯೂ ಇದೇ ಆಗುತ್ತದೆ.

Windows, Linux, Mac, Azure, AWS, Mobile Phone...

ಇವುಗಳೆಲ್ಲಾ ಬೇರೆಬೇರೆ ಕಂಪನಿಗಳು ತಯಾರಿಸಿದವು.

ಆದರೆ ಇವೆಲ್ಲವೂ ಒಂದೇ Protocol ಗಳನ್ನು ಅನುಸರಿಸುತ್ತವೆ.

ಆದ್ದರಿಂದ ಅವು ಪರಸ್ಪರ Communication ಮಾಡಬಹುದು.

---

# ಉದಾಹರಣೆ

ನೀವು Browser ನಲ್ಲಿ ಟೈಪ್ ಮಾಡುತ್ತೀರಿ

```
https://google.com
```

ಇದೊಂದು ಸಾಲು ಟೈಪ್ ಮಾಡಿದಾಗ ಒಂದೇ Protocol ಬಳಸುವುದಿಲ್ಲ.

ಹಲವಾರು Protocol ಗಳು ಸೇರಿ ಕೆಲಸ ಮಾಡುತ್ತವೆ.

```
Browser

↓

HTTPS

↓

TCP

↓

IP

↓

WiFi / Ethernet

↓

Internet

↓

Google Server
```

ಪ್ರತಿಯೊಂದು Protocol ಗೆ ತನ್ನದೇ ಆದ ಕೆಲಸ ಇದೆ.

---

# 1. HTTP (HyperText Transfer Protocol)

HTTP ಎಂಬುದು Web Pages ಕಳುಹಿಸುವ Protocol.

ನೀವು Browser ನಲ್ಲಿ Website Open ಮಾಡಿದಾಗ,

Browser ಮತ್ತು Server HTTP ಮೂಲಕ ಮಾತನಾಡುತ್ತವೆ.

ಉದಾಹರಣೆ

```
Browser

↓

"ನನಗೆ Home Page ಕೊಡು"

↓

Server

↓

HTML

CSS

JavaScript

Images
```

HTTP ಕೇವಲ Data Transfer ಮಾಡುತ್ತದೆ.

---

### ಸಮಸ್ಯೆ

HTTP ನಲ್ಲಿ Data Encrypt ಆಗುವುದಿಲ್ಲ.

ಅಂದರೆ ಮಧ್ಯದಲ್ಲಿ ಯಾರಾದರೂ Data ಓದಬಹುದು.

ಆದ್ದರಿಂದ ಇಂದಿನ ದಿನಗಳಲ್ಲಿ HTTP ಕಡಿಮೆ ಬಳಸುತ್ತಾರೆ.

---

# 2. HTTPS

HTTPS = HTTP + SSL/TLS Encryption

ಇದು HTTP ಗಿಂತ Secure.

```
Browser

↓

Encrypted Request

↓

Internet

↓

Encrypted Response
```

Password

Credit Card

Bank Details

Login Information

ಇವೆಲ್ಲವೂ HTTPS ಮೂಲಕ ಸುರಕ್ಷಿತವಾಗಿ ಹೋಗುತ್ತವೆ.

---

## ಉದಾಹರಣೆ

Browser ನಲ್ಲಿ

```
https://google.com
```

ಎಂದು ಇದ್ದರೆ ಅದು HTTPS.

```
http://example.com
```

ಎಂದರೆ ಅದು Secure ಅಲ್ಲ.

---

# 3. TCP (Transmission Control Protocol)

TCP ತುಂಬಾ ಪ್ರಮುಖ Protocol.

ಇದರ ಮುಖ್ಯ ಕೆಲಸ

**Data ಸರಿಯಾಗಿ ತಲುಪಿದೆಯೇ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳುವುದು.**

---

ಒಂದು ಉದಾಹರಣೆ

ನೀವು 100 Page PDF ಕಳುಹಿಸಿದ್ದೀರಿ.

ಅದು 100 Packets ಆಗಿ ಹೋಯಿತು.

```
Packet 1

Packet 2

Packet 3

...

Packet 100
```

Packet 45 ಮಧ್ಯದಲ್ಲಿ ಕಳೆದುಹೋಯಿತು.

TCP ಏನು ಮಾಡುತ್ತದೆ?

```
Destination

↓

Packet 45 Missing

↓

Source ಗೆ ಹೇಳುತ್ತದೆ

↓

"Packet 45 ಮತ್ತೆ ಕಳುಹಿಸು"
```

ಆದ್ದರಿಂದ TCP Reliable.

---

TCP ಬಳಸುವ Applications

* HTTP
* HTTPS
* SSH
* FTP
* Email
* MySQL

---

# 4. UDP (User Datagram Protocol)

UDP TCP ಗಿಂತ Fast.

ಆದರೆ Reliable ಅಲ್ಲ.

ಇದು Packet ತಲುಪಿದೆಯೋ ಇಲ್ಲವೋ ಎಂದು Check ಮಾಡುವುದಿಲ್ಲ.

```
Packet

↓

ಕಳುಹಿಸು

↓

ಮುಗಿಯಿತು
```

ಅಷ್ಟೇ.

---

## ಯಾಕೆ UDP ಬೇಕು?

ಕೆಲವು Applications ಗೆ Speed ಮುಖ್ಯ.

Packet ಕಳೆದುಹೋದರೂ ಸಮಸ್ಯೆ ಇಲ್ಲ.

ಉದಾಹರಣೆ

YouTube Live

Voice Call

Video Call

Online Games

---

ಉದಾಹರಣೆ

Video Call ನಲ್ಲಿ

ಒಂದು Frame Miss ಆದರೆ

ನಿಮಗೆ ಗೊತ್ತಾಗುವುದೇ ಇಲ್ಲ.

ಆದರೆ

2 Seconds Delay ಆದರೆ

Call ಬಳಸಲು ಆಗುವುದಿಲ್ಲ.

ಆದ್ದರಿಂದ Video Calls ಸಾಮಾನ್ಯವಾಗಿ UDP ಬಳಸುತ್ತವೆ.

---

# TCP vs UDP

| TCP                    | UDP               |
| ---------------------- | ----------------- |
| Reliable               | Fast              |
| Packet Check ಮಾಡುತ್ತದೆ | Check ಮಾಡುವುದಿಲ್ಲ |
| Slow                   | Very Fast         |
| Banking                | Video Streaming   |
| HTTPS                  | Video Calls       |

---

# 5. IP (Internet Protocol)

IP Protocol ನ ಕೆಲಸ

**Data ಯಾವ Computer ಗೆ ಹೋಗಬೇಕು ಎಂದು ನಿರ್ಧರಿಸುವುದು.**

ಉದಾಹರಣೆ

```
Laptop

↓

192.168.1.10

↓

Internet

↓

142.250.x.x

↓

Google
```

IP Protocol ಗೆ Data ಒಳಗೆ ಏನಿದೆ ಎಂಬುದು ಮುಖ್ಯವಲ್ಲ.

ಅದಕ್ಕೆ Address ಮಾತ್ರ ಮುಖ್ಯ.

ಇದನ್ನು Courier Service ಗೆ ಹೋಲಿಸಬಹುದು.

Courier Boy Parcel ಒಳಗೆ ಏನಿದೆ ಎಂದು ನೋಡುವುದಿಲ್ಲ.

ಅವನಿಗೆ Address ಸಾಕು.

---

# 6. DNS (Domain Name System)

Computer ಗೆ

```
google.com
```

ಅರ್ಥವಾಗುವುದಿಲ್ಲ.

Computer ಗೆ

```
142.250.xxx.xxx
```

ಹಾಗೆ IP Address ಬೇಕು.

DNS ಈ ಕೆಲಸ ಮಾಡುತ್ತದೆ.

```
google.com

↓

DNS Server

↓

142.250.xxx.xxx
```

ಅದರ ನಂತರ Browser ಆ IP Address ಗೆ Request ಕಳುಹಿಸುತ್ತದೆ.

---

# ಇವೆಲ್ಲವೂ ಒಟ್ಟಿಗೆ ಹೇಗೆ ಕೆಲಸ ಮಾಡುತ್ತವೆ?

ನೀವು Browser ನಲ್ಲಿ ಟೈಪ್ ಮಾಡುತ್ತೀರಿ

```
https://google.com
```

ಆಗ ಏನಾಗುತ್ತದೆ?

### Step 1

Browser

↓

DNS

```
google.com

↓

142.250.xxx.xxx
```

DNS Domain Name ಅನ್ನು IP Address ಆಗಿ ಪರಿವರ್ತಿಸುತ್ತದೆ.

---

### Step 2

IP Protocol

Google Server ನ Address ಹುಡುಕುತ್ತದೆ.

```
Destination

↓

142.250.xxx.xxx
```

---

### Step 3

TCP

Google Server ಜೊತೆ Reliable Connection ಸ್ಥಾಪಿಸುತ್ತದೆ.

```
Browser

⇄

Google
```

---

### Step 4

HTTPS

ಎಲ್ಲಾ Data Encrypt ಆಗುತ್ತದೆ.

```
Encrypted Data

↓

Internet
```

---

### Step 5

Google Response ಕಳುಹಿಸುತ್ತದೆ.

HTML

CSS

JavaScript

Images

ಇವೆಲ್ಲವೂ Packets ಆಗಿ ನಿಮ್ಮ Browser ಗೆ ಬರುತ್ತವೆ.

Browser ಅವನ್ನು ಸೇರಿಸಿ Web Page ತೋರಿಸುತ್ತದೆ.

---

# ಒಂದು ಸರಳ ಉಪಮೆ

ಒಂದು Courier Service ಅನ್ನು ಊಹಿಸಿ.

* **DNS** → ವಿಳಾಸ ಹುಡುಕುವ ವ್ಯಕ್ತಿ ("Google Office ಎಲ್ಲಿದೆ?")
* **IP** → Parcel ಅನ್ನು ಸರಿಯಾದ ವಿಳಾಸಕ್ಕೆ ಕೊಂಡೊಯ್ಯುವ ವ್ಯವಸ್ಥೆ.
* **TCP** → ಪ್ರತಿಯೊಂದು ಪೆಟ್ಟಿಗೆಯೂ ಸುರಕ್ಷಿತವಾಗಿ ತಲುಪಿದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸುವ Supervisor.
* **UDP** → "ಸಾಧ್ಯವಾದಷ್ಟು ಬೇಗ ಕಳುಹಿಸು; ಒಂದು-ಎರಡು ಪೆಟ್ಟಿಗೆ ತಪ್ಪಿದರೂ ಪರವಾಗಿಲ್ಲ" ಎನ್ನುವ Express Delivery.
* **HTTP** → Parcel ಒಳಗೆ ಯಾವ ರೀತಿಯ ಮಾಹಿತಿ ಇದೆ ಮತ್ತು ಅದನ್ನು ಹೇಗೆ ಕಳುಹಿಸಬೇಕು ಎಂಬ ನಿಯಮ.
* **HTTPS** → ಅದೇ Parcel ಅನ್ನು Lock ಮಾಡಿ, Seal ಮಾಡಿ ಸುರಕ್ಷಿತವಾಗಿ ಕಳುಹಿಸುವ ವಿಧಾನ.

---

# ನೆನಪಿಡಲು ಒಂದು ಸುಲಭ ಟೇಬಲ್

| Protocol  | ಮುಖ್ಯ ಕೆಲಸ                                           | ಸರಳ ಉದಾಹರಣೆ           |
| --------- | ---------------------------------------------------- | --------------------- |
| **HTTP**  | Web Page Data ಕಳುಹಿಸುವುದು                            | ಸಾಮಾನ್ಯ ಪತ್ರ          |
| **HTTPS** | Web Data ಅನ್ನು Encrypt ಮಾಡಿ ಸುರಕ್ಷಿತವಾಗಿ ಕಳುಹಿಸುವುದು | Lock ಮಾಡಿದ ಪತ್ರ       |
| **TCP**   | Data ಸಂಪೂರ್ಣವಾಗಿ ತಲುಪಿದೆಯೇ ಎಂದು ಖಚಿತಪಡಿಸುವುದು        | Courier Tracking      |
| **UDP**   | ಅತ್ಯಂತ ವೇಗವಾಗಿ Data ಕಳುಹಿಸುವುದು                      | Live TV Broadcast     |
| **IP**    | Data ಯಾವ Computer ಗೆ ಹೋಗಬೇಕು ಎಂದು ನಿರ್ಧರಿಸುವುದು      | ಮನೆಯ ವಿಳಾಸ            |
| **DNS**   | Domain Name ಅನ್ನು IP Address ಆಗಿ ಪರಿವರ್ತಿಸುವುದು      | Phone Book / Contacts |

## ಒಂದು ಮುಖ್ಯ ವಿಷಯ

ಇವು **ಒಂದಕ್ಕೊಂದು ಸ್ಪರ್ಧಿಸುವ Protocol ಗಳು ಅಲ್ಲ**. ಪ್ರತಿಯೊಂದಕ್ಕೂ ತನ್ನದೇ ಆದ ಜವಾಬ್ದಾರಿ ಇದೆ. ಒಂದು Website ಅನ್ನು ತೆರೆದಾಗ ಸಾಮಾನ್ಯವಾಗಿ **DNS + IP + TCP + HTTPS** ಎಲ್ಲವೂ ಸೇರಿ ಕೆಲಸ ಮಾಡುತ್ತವೆ. Networking ನ ಶಕ್ತಿ ಇದೇ—ಪ್ರತಿಯೊಂದು Protocol ತನ್ನ ಕೆಲಸವನ್ನು ಸರಿಯಾಗಿ ಮಾಡಿದಾಗ, ಸಂಪೂರ್ಣ ವ್ಯವಸ್ಥೆ ಸುಗಮವಾಗಿ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆ.
