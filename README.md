# small-office-network
small-office-network demonstrating a small office network using cisco packet tracer ,DHCP ,static server , 1 router ,2 switches, 12 PCS


# Small Office Network

## 🏢 Project Scenario
This is a small office network simulation built in Cisco Packet Tracer.  
The network consists of:

- 1 Router (R1)
- 2 Switches (SW1, SW2)
- 12 PCs (PC0–PC11)
- 1 Server (Server0) with static IP
- DHCP service for PCs

The goal is to provide dynamic IPs to all PCs, configure a static IP for the server, and ensure full connectivity across the network.

---

## 🌐 IP Addressing

| Device | IP Address        | Subnet Mask     | Default Gateway |
|--------|-----------------|----------------|----------------|
| Router | 192.168.10.1     | 255.255.255.0  | -              |
| Server | 192.168.10.10    | 255.255.255.0  | 192.168.10.1   |
| DHCP   | 192.168.10.50–100| 255.255.255.0  | 192.168.10.1   |
| PCs    | DHCP assigned    | 255.255.255.0  | 192.168.10.1   |

---

## 🔧 Configuration

**Router (R1):**

- IP address: `192.168.10.1/24` on Gig0/0
- DHCP pool for PCs (`192.168.10.50–100`)
- Basic security:
  - Enable secret: `cisco123`
  - Console password: `admin`
  - VTY password: `admin`
  - Password encryption enabled

**Server (Server0):**

- IP address: `192.168.10.10/24`
- Default gateway: `192.168.10.1`
- DNS: `8.8.8.8`

**PCs (PC0–PC11):**

- Receive IP automatically via DHCP
- Default gateway: `192.168.10.1`

---

## 🛠 Testing

- PCs can ping each other ✅  
- PCs can ping the server ✅  
- Server can ping all PCs ✅  
- Router interface is up ✅

---

## 📁 Files Included

- `PacketTracerFile.pkt` → Cisco Packet Tracer file  
- `topology.png` → Screenshot of the network topology  
- `configs/` → Router and Switch configuration files (R1.txt, SW1.txt)

---

## 🔐 Security Measures

- Password encryption enabled (`service password-encryption`)  
- Enable secret set (`enable secret cisco123`)  
- Console and VTY passwords applied  

---
what i learned 
setting up a basic lan setup ,dhcp config and a static server for a small office which occurs a lot in real life senarios
