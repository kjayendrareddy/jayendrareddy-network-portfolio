# Project 2 — FortiGate Firewall Policy, NAT & VPN Lab

**Type:** Lab demonstration | **Focus:** Firewall rules, NAT, secure remote access

## Goal
Create a small simulated office perimeter with a LAN, WAN test network, and a VPN endpoint. Demonstrate least-privilege access and validation.

## Lab design
- LAN: 192.168.10.0/24
- Guest: 192.168.20.0/24
- Management: 192.168.99.0/24
- Use documentation-only or private lab addresses; never expose production addressing.

## Build steps
1. Draw the topology and define trust zones.
2. Configure interface addressing and routes.
3. Create address objects and service objects.
4. Add a LAN-to-WAN policy limited to required services.
5. Configure source NAT where appropriate for the lab.
6. Configure a VPN only in a supported lab environment and restrict access to required subnets.
7. Enable logging on relevant policies.
8. Test allowed and denied flows, then inspect logs and counters.

## Validation checklist
- [ ] Only required services are allowed.
- [ ] Guest network cannot reach management devices unless explicitly required.
- [ ] NAT works for the intended outbound traffic.
- [ ] VPN users can reach only approved resources.
- [ ] Logs show expected allowed/denied sessions.
- [ ] Configuration backup is stored securely.

## Troubleshooting flow
1. Confirm interface/link status and route table.
2. Confirm source/destination addresses and service.
3. Verify policy order and policy match.
4. Check NAT settings and return path.
5. Check VPN negotiation, phase/status, routes, selectors, and authentication.
6. Review logs; make one controlled change at a time.

## Evidence to add
Use sanitized screenshots of the policy table, route table, VPN status, and test results. Never publish passwords, pre-shared keys, tokens, public IPs, or real customer information.

**Disclosure:** The resume lists Fortinet and Sophos firewall work. This write-up is a proposed portfolio lab, not a claim that this exact design was deployed at work.
