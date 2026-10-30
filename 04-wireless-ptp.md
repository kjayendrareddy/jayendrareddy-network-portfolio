# Project 4 — Wireless Point-to-Point Link Design

**Type:** Lab/design exercise | **Focus:** Wireless bridge planning and troubleshooting

## Goal
Design a point-to-point wireless link between two buildings and document alignment, capacity, security, and acceptance testing.

## Relevant experience
My resume mentions Mimosa, Ubiquiti PowerBeam, and AirGrid point-to-point equipment. This project is a lab/design exercise unless you add a sanitized description of a real deployment.

## Design checklist
1. Confirm line of sight and Fresnel-zone clearance.
2. Check local regulations and permitted frequency/power settings.
3. Select compatible radios, antennas, mounting, grounding, and surge protection.
4. Plan management IPs and the VLAN(s) carried across the bridge.
5. Use strong device credentials and supported encryption.
6. Plan channel width and frequency based on local interference and applicable rules.
7. Align radios and record signal strength, noise floor, SNR, and negotiated link rate.
8. Test throughput, latency, packet loss, and stability during a defined period.
9. Document failover or repair access if the link is business critical.

## Troubleshooting flow
- No link: power, cabling/PoE, alignment, channel, configuration compatibility.
- Weak signal: alignment, obstructions, Fresnel clearance, antenna/cable issues.
- High packet loss: interference, poor SNR, congestion, channel width, hardware/cabling.
- Management unreachable: management VLAN/IP, routing, ACL/firewall, credentials.
- Link works but VLAN does not: bridge mode, VLAN tagging, switch trunk configuration.

## Results table to complete
| Test | Expected | Actual |
|---|---|---|
| Signal/SNR | Within vendor design guidance | Add your measurement |
| Throughput | Meets requirement | Add measured result |
| Latency | Meets application need | Add measured result |
| Packet loss | Acceptable for use case | Add measured result |
| Stability | No unexpected drops during test | Add observation |

Add your own topology, screenshots, measurements, and equipment model. Do not claim a field deployment unless it happened.
