# Asset Register

Last reviewed: 2026-10-29 · Maintained by: Jamie Saraza
Status values: In service · Under repair · Retired · Disposed

| Asset ID | Hostname | Role | OS / edition | Build (winver) | Last patch (KB, date) | vCPU / RAM / Disk | IP | Owner | In service | Status | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| LAB-SRV-001 | AD-DC01 | Domain controller | Windows Server 2022 Standard Evaluation | 20348.587 | KB5011497, 2022-03-03 | 2 / 4 GB / 70 GB | 192.168.10.10 | IT (J. Saraza) | 2026-05-15 | In service | 2026-11-04 |
| LAB-WS-001 | AD-CL01 | Workstation | Windows 10 Pro | 19045.6456 | KB5066791, 2026-05-23 | 2 / 4 GB / 60 GB | 192.168.10.20 | IT (J. Saraza) | 2026-05-15 | In service | 2027-04-08 |
| LAB-HOST-001 | LAPTOP-EB1L9Q6I | Hypervisor host | Windows 11 Home 25H2 | 26200.9711 | KB127648, 2026-10-16 | i5-1335U/ 16GB / ? | 192.168.1.186 | J. Saraza | ? | In service | 2027-04-29 |

## Findings
- Build 20348.587 = the March 2022 update from the install media. Nothing installed since setup (2026-05-15). Isolated network, no update server. Production: an update server such as WSUS. Lab: accepted risk.
- Evaluation edition, about 2026-11-11, 6 extensions left. Fix: CR-002, extend before expiry.
- KB5066791 = the final Windows 10 update (October 14, 2025). No security fixes since. Options: Windows 11, or paid Extended Security Updates. Lab: accepted risk.
