# Azure Networking Handbook
### Networking Fundamentals ಇಂದ Production-Ready Azure Architecture ವರೆಗು

> ಇದು Azure Networking ನ ಒಂದು practical handbook — zero ಇಂದ ಕಲಿತುಕೊಳ್ಳೋದಕ್ಕೆ.
> ಈ guide networking fundamentals ಇಂದ start ಆಗಿ, gradually enterprise-grade Azure network architectures design ಮಾಡೋ ಕಡೆಗೆ progress ಆಗುತ್ತೆ.

---

## 📖 ಈ Handbook ಬಗ್ಗೆ

ನಮ್ಮ end goal **Azure VM + AKS** ಆಗಿರೋದ್ರಿಂದ, ಇದನ್ನ CCNA networking course ತರ ಮಾಡ್ಬೇಕು ಅಂತ ಇಲ್ಲ. ಇದನ್ನ **"Cloud Engineers ಗಾಗಿ Networking"** ಅಂತ think ಮಾಡಿ.

ನನ್ನ goal:

* ಪ್ರತಿ concept **ಯಾಕೆ ಇದೆ** ಅಂತ explain ಮಾಡೋದು.
* ಬೇಡದ theory avoid ಮಾಡೋದು.
* Real-world analogies use ಮಾಡೋದು.
* Practical ಆಗಿ ಇಟ್ಟುಕೊಳ್ಳೋದು.
* Memorization ಬದಲು intuition build ಮಾಡೋದು.

---

ಬಹಳ Azure networking resources ನಿಮಗೆ already computer networking ಗೊತ್ತು ಅಂತ assume ಮಾಡ್ತಾವೆ.

ಈ handbook ಇದಕ್ಕೆ different approach ತಗೊಳ್ಳುತ್ತೆ.

ಇದು **computers ಹೇಗೆ communicate ಮಾಡುತ್ತೆ** ಅಂತ explain ಮಾಡೋದ್ರಿಂದ start ಆಗಿ, ಆ ಮೇಲೆ IP addressing, routing, DNS, NAT, firewalls ತರ networking fundamentals introduce ಮಾಡುತ್ತೆ — ಆ ಮೇಲೆ Virtual Networks, Subnets, VNet Peering, Private Link, Private Endpoints, Routing, Network Security, Hybrid Connectivity, ಮತ್ತು enterprise network design ತರ Azure networking concepts ಕಡೆ move ಆಗುತ್ತೆ.

ಪ್ರತಿ topic ಈ ವಿಷಯಗಳಿಂದ explain ಮಾಡಲಾಗುತ್ತೆ:

- Simple language
- Real-world examples
- Visual diagrams
- Architecture thinking
- Production best practices
- Hands-on labs

ಇದರ goal ಕೇವಲ **Azure networking ಹೇಗೆ work ಆಗುತ್ತೆ** ಅಂತ ಕಲಿತುಕೊಳ್ಳೋದಲ್ಲ, ಜೊತೆಗೆ **enterprise cloud architects ಯಾಕೆ ಆ ರೀತಿ design ಮಾಡ್ತಾರೆ** ಅಂತ ಅರಿಯೋ ಹಾಗೆ ಕೂಡ.

---

# 🎯 ಈ Handbook ಯಾರಿಗೆ?

ಈ handbook ಈ ಜನ ಗಾಗಿ design ಮಾಡಲಾಗಿದೆ:

- Cloud networking ಕಲಿತುಕೊಳ್ಳೋ beginners
- Azure Administrators
- Cloud Engineers
- DevOps Engineers
- Platform Engineers
- Azure Solution Architects
- Azure certifications ಗಾಗಿ prepare ಆಗುತ್ತಿರೋ students
- Production Azure networking ಅರ್ಥ ಮಾಡ್ಕೊಳ್ಳೋ ಆಸಕ್ತಿ ಇರೋವರು ಯಾರೇ ಆಗಿರಲಿ

---

# 📚 Learning Path

# Module 0 — Cloud Networking Fundamentals

*(Already networking ಬಗ್ಗೆ comfortable ಇದ್ರೆ skip ಮಾಡಿ.)*

### 0.1 Computers ಹೇಗೆ communicate ಮಾಡುತ್ತೆ

* OSI Model (high level)
* TCP/IP Model
* Packets
* Frames
* Ports
* IP Addresses
* MAC Addresses

### 0.2 IP Addressing

* IPv4
* Public IP
* Private IP
* CIDR notation
* Subnet masks
* Default Gateway

### 0.3 DNS

* DNS ಏನು ಮಾಡುತ್ತೆ
* Recursive lookup
* A Records
* CNAME
* Private DNS

### 0.4 Routing

* Static Routing
* Dynamic Routing (concept)
* Longest Prefix Match

### 0.5 NAT

* SNAT
* DNAT
* PAT

### 0.6 Firewalls

* Stateful vs Stateless
* Allow/Deny rules

[Module 0 — Cloud Networking Fundamentals](./handbook/Part-00-Cloud-Networking-Fundamentals.md)

---

# Module 1 — Azure Networking Basics

### 1.1 Azure Regions

### 1.2 Resource Groups

### 1.3 Azure Virtual Networks

### 1.4 Subnets

### 1.5 Network Interfaces (NIC)

### 1.6 Public IPs

### 1.7 Private IPs

### 1.8 Azure ನಲ್ಲಿ DNS

Lab

* ಒಂದು VNet create ಮಾಡಿ
* ಎರಡು subnets create ಮಾಡಿ
* VM attach ಮಾಡಿ

---

# Module 2 — Virtual Networks Deep Dive

### 2.1 Address Spaces

### 2.2 CIDR Planning

### 2.3 Subnet Design

### 2.4 Reserved Azure IPs

### 2.5 Service Endpoints

### 2.6 Private Endpoints

### 2.7 Private Link

### 2.8 VNet Peering

### 2.9 User Defined Routes

Lab

* Multiple subnets create ಮಾಡಿ
* ಎರಡು VNets peer ಮಾಡಿ
* Route tables configure ಮಾಡಿ

---

# Module 3 — Azure Network Security

### 3.1 Network Security Groups

* Inbound rules
* Outbound rules
* Priorities

### 3.2 Application Security Groups

### 3.3 Azure Firewall

### 3.4 DDoS Protection

### 3.5 Bastion

### 3.6 Just-In-Time VM Access

Lab

* SSH ಮಾತ್ರ allow ಮಾಡಿ
* Internet traffic block ಮಾಡಿ
* Bastion use ಮಾಡಿ connect ಮಾಡಿ

---

# Module 4 — Azure VM Networking

### 4.1 VM Networking Components

### 4.2 NICs

### 4.3 Multiple NICs

### 4.4 Public IP Assignment

### 4.5 Static vs Dynamic IP

### 4.6 Accelerated Networking

### 4.7 VM ಒಳಗೆ DNS

### 4.8 Availability Sets Networking

### 4.9 Availability Zones

Lab

* Linux VM deploy ಮಾಡಿ
* SSH ಮಾಡಿ
* NSG configure ಮಾಡಿ
* Static IP assign ಮಾಡಿ
* Connectivity test ಮಾಡಿ

---

# Module 5 — Load Balancing

### 5.1 Azure Load Balancer

### 5.2 Internal vs Public Load Balancer

### 5.3 Health Probes

### 5.4 Backend Pools

### 5.5 Azure Application Gateway

### 5.6 Layer 4 vs Layer 7

### 5.7 Web Application Firewall

### 5.8 Azure Front Door (overview)

Lab

* ಎರಡು VMs deploy ಮಾಡಿ
* Load Balancer configure ಮಾಡಿ
* Application Gateway configure ಮಾಡಿ

---

# Module 6 — AKS Networking

ಇದು ಎಲ್ಲಾ modules ಗೆ most important ಆಗಿದೆ.

### 6.1 Kubernetes Networking Basics

* Pods
* Services
* ClusterIP
* NodePort
* LoadBalancer
* Ingress

### 6.2 AKS Networking Models

* Kubenet
* Azure CNI
* Azure CNI Overlay

### 6.3 Pod IPs

### 6.4 Node IPs

### 6.5 Service CIDR

### 6.6 DNS Service

### 6.7 Ingress Controllers

### 6.8 Internal Load Balancers

### 6.9 External Load Balancers

### 6.10 Network Policies

### 6.11 Private AKS Cluster

### 6.12 API Server Access

Lab

* AKS deploy ಮಾಡಿ
* nginx deploy ಮಾಡಿ
* ClusterIP expose ಮಾಡಿ
* NodePort expose ಮಾಡಿ
* LoadBalancer expose ಮಾಡಿ
* Ingress install ಮಾಡಿ
* Network Policy test ಮಾಡಿ

---

# Module 7 — Hybrid Networking

### 7.1 VPN Gateway

### 7.2 ExpressRoute (overview)

### 7.3 Hub-Spoke Architecture

### 7.4 Shared Services VNet

### 7.5 Transit Routing

### 7.6 Private DNS Zones

Lab

* Hub create ಮಾಡಿ
* Spokes create ಮಾಡಿ
* VNets peer ಮಾಡಿ

---

# Module 8 — Real-world Azure Architecture

ಈ ವಿಷಯಗಳ ಜೊತೆ ಒಂದು environment design ಮಾಡಿ:

* Hub-Spoke Network
* Management Subnet
* AKS Subnet
* VM Subnet
* Database Subnet
* Bastion
* Application Gateway
* Azure Firewall
* NAT Gateway
* Private Endpoint
* Azure Load Balancer

ಆ ಮೇಲೆ deploy ಮಾಡಿ:

```
Internet
    │
Azure Front Door
    │
Application Gateway (WAF)
    │
──────── Azure VNet ────────
│                           │
AKS Subnet             VM Subnet
│                           │
Pods                    Linux VM
│
Private Endpoint
│
Azure SQL / Storage
```

---

## Suggested Learning Order

1. **Cloud Networking Fundamentals** (1–2 days)
2. **Azure Networking Basics** (2 days)
3. **Virtual Networks** (2–3 days)
4. **Network Security** (2 days)
5. **VM Networking** (2 days)
6. **Load Balancing** (2 days)
7. **AKS Networking** (4–5 days)
8. **Hybrid Networking** (2 days)
9. **Architecture Labs** (3–5 days)

ಈ path, basic networking concepts ಇಂದ start ಆಗಿ secure Azure VMs ಮತ್ತು production-ready AKS clusters confidently deploy ಮಾಡೋ ತನಕ ಕರ್ಕೊಂಡು ಹೋಗುತ್ತೆ.

ನಿಮ್ಮ end goal **cloud-native architect ಅಥವಾ DevOps engineer** ಆಗ್ಬೇಕು ಅಂತ ಇದ್ರೆ, networking ಮುಗಿದ ಮೇಲೆ ಈ ಎರಡು follow-up modules add ಮಾಡಿ:

* **Module 9: Azure Storage & Identity** (Managed Identity, Key Vault, Storage Accounts, Azure Files, Disks)
* **Module 10: AKS Production Architecture** (node pools, autoscaling, ingress, observability, disaster recovery, cost optimization, ಮತ್ತು security best practices)

ಇವು networking knowledge ಗೆ complement ಆಗಿ, real-world Azure deployments ನಲ್ಲಿ frequently encounter ಆಗುವ topics cover ಮಾಡುತ್ತೆ.


# 🏗️ Learning Philosophy

ಈ handbook ಒಂದು simple learning approach follow ಮಾಡುತ್ತೆ:

```
Networking Basics
        ↓
Azure Fundamentals
        ↓
Virtual Networking
        ↓
Secure Connectivity
        ↓
Production Networking
        ↓
Enterprise Architecture
```

ಪ್ರತಿ chapter ಇದೇ structure follow ಮಾಡುತ್ತೆ:

- Concept
- ಯಾಕೆ ಇದು ಇದೆ (Why it exists)
- Real-world example
- Architecture explanation
- Best practices
- Interview questions
- Hands-on lab

---

# 🎯 Goal

ಈ handbook ಮುಗಿದ ಮೇಲೆ ನಿಮಗೆ ಇದು ಸಾಧ್ಯ ಆಗುತ್ತೆ:

- Azure Virtual Networks design ಮಾಡೋಕೆ
- IP Address Spaces plan ಮಾಡೋಕೆ
- Production-ready network architectures build ಮಾಡೋಕೆ
- Azure resources secure ಮಾಡೋಕೆ
- VNets ಮತ್ತು on-premises networks connect ಮಾಡೋಕೆ
- Enterprise Azure networking patterns ಅರ್ಥ ಮಾಡ್ಕೊಳ್ಳೋಕೆ
- ಕೇವಲ Azure resources deploy ಮಾಡೋ ಬಗ್ಗೆ ಅಲ್ಲ, ಒಂದು Cloud Architect ತರ think ಮಾಡೋಕೆ

---

# 📂 Handbook Structure

```
Azure-Networking-Handbook/

│
├── README.md
│
├── handbook/
│   ├── Part-00-Cloud-Networking-Fundamentals.md
│   ├── Part-01-Azure-Networking-Basics.md
│   ├── Part-02-Azure-Virtual-Network-Deep-Dive.md
│   ├── Part-03-Network-Security.md
│   ├── Part-04-Hybrid-Networking.md
│   ├── Part-05-Enterprise-Network-Architecture.md
│   ├── ...
│
└── diagrams/
```

---

# ⭐ Guiding Principle

> **"ಕೇವಲ Azure Networking ಕಲಿಯಬೇಡಿ. Enterprise cloud architects networks ಯಾಕೆ ಆ ರೀತಿ design ಮಾಡ್ತಾರೆ ಅಂತ ಕಲಿತುಕೊಳ್ಳಿ."**

ಈ handbook, Azure networking concepts ಅರ್ಥ ಮಾಡ್ಕೊಳ್ಳೋದು ಮತ್ತು ಅದನ್ನ real-world, production-grade cloud architectures ಗೆ apply ಮಾಡೋದರ ನಡುವೆ ಇರೋ gap ನ bridge ಮಾಡೋಕೆ design ಮಾಡಲಾಗಿದೆ.