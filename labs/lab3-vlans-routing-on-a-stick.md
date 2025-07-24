# Lab 3: VLANs and Routing on a Stick

## Objective
Set up multiple VLANs and configure inter-VLAN routing using a single router interface (Router-on-a-Stick).

## Tools Used
- Cisco Packet Tracer
- 1 switch, 1 router, 6 PCs
- VLANs 10, 20, and 30

## Tasks Performed
- Created VLANs 10, 20, and 30 on Switch0
- Assigned FastEthernet ports to the correct VLANs
- Configured trunking between Switch0 and Router0 on interface G0/1
- Configured Router0 with subinterfaces for each VLAN (using 802.1q encapsulation)
- Assigned static IP addresses and default gateways to PCs based on their VLAN
- Verified connectivity using `ping` across VLANs

## Commands Used (Samples)
```plaintext
Switch(config)# vlan 10
Switch(config)# interface range fa0/1 - 2
Switch(config-if-range)# switchport access vlan 10

Router(config)# interface g0/1.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0
