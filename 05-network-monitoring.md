# Project 5 — Network Monitoring & Incident Response

**Type:** Lab / monitoring workflow | **Focus:** Availability, alerts, investigation, documentation

## Goal
Create a small monitoring view for routers, switches, servers, and links, then document how alerts become incidents and how recovery is verified.

## Tools from my resume
Observium, Nagios, LibreNMS, UptimeRobot, and WhatsUp Gold are listed in my resume. Choose one tool available to you and build a lab; don't imply every tool was used in the same environment.

## Build steps
1. Choose lab devices or hosts you own/control.
2. Enable only the required monitoring protocol and restrict access to the monitoring host.
3. Add device availability checks and, where supported, interface utilization, errors, CPU, memory, and latency.
4. Set thresholds appropriate to the lab and avoid alert storms.
5. Test a controlled failure, such as disconnecting a lab interface or stopping a test service.
6. Capture the alert time, investigation steps, recovery time, and verification.
7. Tune the alert if it is noisy or not actionable.

## Example incident workflow
Alert → acknowledge → confirm scope → check interface/link → check recent changes → test reachability → inspect logs/counters → resolve or escalate → verify recovery → close with notes.

## Sample incident report
- **Alert:** [Device/link] unavailable
- **Start time:** [timestamp]
- **Impact:** [what was affected]
- **Checks performed:** [evidence]
- **Root cause:** [confirmed cause only]
- **Resolution:** [action taken]
- **Validation:** [successful tests]
- **Follow-up:** [monitoring or preventive change]

## Dashboard ideas
- Device availability
- WAN link status
- Interface utilization
- Errors/discards
- Latency and packet loss
- Open incidents and acknowledgement time

Use lab-only addresses and sanitized screenshots. Add real measurements after testing; do not fabricate uptime or MTTR figures.
