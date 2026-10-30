# Project 3 — ISP Leased-Line Troubleshooting Runbook

**Type:** Operational runbook / anonymized scenario | **Focus:** WAN, VLAN, routing, customer connectivity

## Context
My resume describes support for 100+ leased-line circuits and approximately 1,000 broadband customers at Nettlinx. This project turns that type of work into a repeatable troubleshooting workflow. Do not include customer names, real circuit IDs, or live addresses.

## Incident scenario
A site reports that its leased-line connection is down. Treat this as a simulated scenario unless you document a real incident with all sensitive details removed.

## Triage steps
1. Confirm scope: one endpoint, one site, multiple sites, or upstream outage.
2. Check monitoring alerts and the incident start time.
3. Check CPE/router power, link lights, interface status, and cabling.
4. Verify WAN IP, subnet, gateway, VLAN tag, and handoff details against approved records.
5. Ping the local gateway, provider next hop, and approved external test target.
6. Check interface errors, drops, speed/duplex, and optical levels if relevant and supported.
7. Review routing table, ARP/neighbor table, and recent configuration changes.
8. Escalate to the carrier with timestamp, circuit reference, test results, and impact.
9. After restoration, verify customer traffic and monitor for recurrence.
10. Record root cause, resolution, and preventive action.

## Example incident record
- **Impact:** One site unable to reach upstream services.
- **Checks:** Physical status, VLAN tag, addressing, gateway reachability, interface counters, route table.
- **Root cause:** Fill in only after evidence confirms it.
- **Resolution:** Record the actual approved change or carrier action.
- **Verification:** Record successful tests and monitoring status.

## Useful commands (platform dependent)
```text
show ip interface brief
show interfaces
show ip route
show arp
ping <approved-test-address>
traceroute <approved-test-address>
```

## Metrics to track
- Time to acknowledge
- Time to restore
- Number of affected sites/users
- Repeat incidents
- Packet loss/latency before and after

Do not invent improvement percentages. Add measured values only when you have real evidence.
