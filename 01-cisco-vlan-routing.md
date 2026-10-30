# Project 1 — Cisco VLANs, Trunking & Inter-VLAN Routing

**Type:** Lab demonstration | **Focus:** Cisco switching and Layer 3 connectivity

## Goal
Build a small office network with separate user VLANs and controlled communication through a Layer 3 device.

## Proposed topology
- SW1: access switch
- R1 or Layer 3 switch: gateway/routing device
- VLAN 10 — Admin — 192.168.10.0/24
- VLAN 20 — Operations — 192.168.20.0/24
- VLAN 99 — Management — 192.168.99.0/24

These addresses are examples for a private lab. Change them to match your simulator.

## Build steps
1. Create VLANs 10, 20, and 99.
2. Assign access ports to the correct VLANs.
3. Configure an 802.1Q trunk between the switch and routing device.
4. Configure router subinterfaces or Layer 3 SVIs as appropriate for your equipment.
5. Configure default gateways and DHCP pools if supported by your lab.
6. Verify STP state and ensure there are no unintended loops.
7. Test same-VLAN and inter-VLAN connectivity.

## Example Cisco switch commands
```text
enable
configure terminal
vlan 10
 name ADMIN
vlan 20
 name OPERATIONS
vlan 99
 name MANAGEMENT
interface gigabitEthernet 0/1
 switchport mode trunk
 switchport trunk allowed vlan 10,20,99
end
show vlan brief
show interfaces trunk
show spanning-tree
show ip interface brief
```
Command support varies by switch model and software. Verify syntax before applying.

## Validation checklist
- [ ] Endpoints receive the expected IP address and gateway.
- [ ] Access ports belong to the intended VLAN.
- [ ] Trunk carries only required VLANs.
- [ ] Inter-VLAN traffic works only as intended.
- [ ] STP has stable forwarding/blocking states.
- [ ] Evidence screenshots have no sensitive information.

## Troubleshooting examples
- Wrong VLAN: check access-port assignment.
- No VLAN across uplink: check trunk mode and allowed VLAN list on both ends.
- Gateway unreachable: check SVI/subinterface, IP addressing, and interface status.
- Inter-VLAN ping fails: check routing and endpoint/firewall policy.

## Evidence to add
Add your own topology image, sanitized command output, and a short “issue → checks → root cause → fix → verification” record.

**Disclosure:** This is a lab template. Describe it as completed only after you build and test it.
