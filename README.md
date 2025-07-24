# Lab 3: VLANs and Router-on-a-Stick

This lab demonstrates how to segment a network using VLANs and route inter-VLAN traffic using a single physical router interface (Router-on-a-Stick).

## 🧠 Objectives

- Create multiple VLANs on a switch
- Assign switch ports to different VLANs
- Configure a trunk link between switch and router
- Implement Router-on-a-Stick using subinterfaces
- Assign static IPs to end devices
- Test network connectivity with ping

---

## 🖼️ Topology

![Topology Diagram](screenshots/lab3-topology.png)

---

## 🔧 Step-by-Step Configuration

### 1. **VLAN Configuration**

We created VLANs 10 and 20 and assigned ports to each VLAN.

![VLAN Config](screenshots/lab3-vlan-config.png)

### 2. **VLAN Verification**

We confirmed VLANs and port assignments with `show vlan brief`.

![VLAN Verification](screenshots/lab3-vlan-verification.png)

---

### 3. **Trunk Port Setup**

The trunk was set on interface Gig0/1 to carry multiple VLANs to the router.

![Trunk Port Config](screenshots/lab3-static-trunk,png.png)

---

### 4. **Router Subinterfaces (Router-on-a-Stick)**

Created subinterfaces on Router0 for each VLAN with appropriate IP addresses.

![Router Config](screenshots/lab3-router-config.png)

### 5. **Router Verification**

Confirmed subinterface IP assignments using `show ip interface brief`.

![Router Interface Verification](screenshots/lab3-router-config-verification.png)

---

### 6. **Static IP Configuration**

PCs were manually assigned IP addresses and gateways within their VLAN ranges.

- **PC1 (VLAN 10):**

  ![PC1 IP](screenshots/lab3-static-ip-pc1.png)

- **PC3 (VLAN 20):**

  ![PC3 IP](screenshots/Lab3-static-ip-pc3.png)

---

### 7. **Connectivity Test**

- PC1 successfully pinged 10.10.10.1

  ![Ping from PC1](screenshots/lab3-ping-test-pc1.png)

- PC3 successfully pinged 10.10.10.2

  ![Ping from PC3](screenshots/lab3-ping-test-pc3.png)

---

## ✅ Outcome

- VLANs successfully segmented the switch
- Trunking and Router-on-a-Stick enabled inter-VLAN routing
- All PCs could communicate within and across VLANs

---

## 💡 Technologies Used

- Cisco Packet Tracer
- Cisco 2960 switch
- Cisco 1941 router
- PC-PT devices
