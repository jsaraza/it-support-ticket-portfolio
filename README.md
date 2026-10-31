# IT Support Ticket Portfolio

A service desk portfolio built on my [Active Directory Help Desk Lab](https://github.com/jsaraza/ad-help-desk-labs)
and a Microsoft 365 trial tenant. Project 1 showed I can build a Windows domain; this
project shows I can **run** one as a service: work tickets from diagnosis to verified
fix, prioritise and escalate against defined SLAs, keep asset records, and change
production settings through a controlled change process.

> **Status: in progress.** Each item below is marked done or planned. Nothing is listed
> as done until its write-up and evidence are in this repository.

---

## Environment

| Component | Details |
|---|---|
| **AD-DC01** | Windows Server 2022 domain controller (AD DS, DNS, file services) — `192.168.10.10` |
| **AD-CL01** | Windows 10 Pro domain workstation — `192.168.10.20` |
| **Domain** | `adlab.local`, on an isolated VirtualBox internal network (no internet access) |
| **Microsoft 365** | Personal Business Standard **trial** tenant (`SFU204.onmicrosoft.com`), used for the cloud tickets. Not affiliated with Simon Fraser University. |
| **Host** | Windows 11 laptop running VirtualBox |

Full asset details are in the [asset register](docs/asset-register.md).

---

## What's here

### Service management
| Document | What it covers |
|---|---|
| [Priority and SLA definitions](docs/service-management/priority-and-sla.md) | P1–P4 priority matrix (impact × urgency), response and resolution targets, priority rules |
| [Escalation matrix](docs/service-management/escalation-matrix.md) | Tier 1, Tier 2, Tier 3 and Security responsibilities, with an escalation trigger per issue type |
| [Asset register](docs/asset-register.md) | OS build, patch level and lifecycle dates for each device, plus three findings: an unpatched domain controller, an expiring evaluation licence, and an end-of-support Windows 10 client |

### Change requests
| CR | Change | Result |
|---|---|---|
| [CR-001](docs/change-requests/CR-001-lockout-threshold.md) | Raise the domain account lockout threshold from 3 to 10 | Completed; verified before and after with `net accounts /domain` and a user-side lockout test |

Change requests follow a [template](docs/change-requests/TEMPLATE.md): risk rating,
backout plan, and verification from the user's side.

### Tickets
| # | Ticket | Type | Priority | Source |
|---|---|---|---|---|
| [001](docs/tickets/TICKET-001-mapped-drive-missing.md) | Mapped drive missing after logon | Incident | P2 | Reproduced in AD lab |
| [009](docs/tickets/TICKET-009-m365-new-starter.md) | New starter: Microsoft 365 account, mailbox and SharePoint access | Service request | P4 | Reproduced in Microsoft 365 tenant |

Every ticket uses the same structure: **Request → Diagnosis** (each check, its result,
and what it ruled out) **→ Actions taken → Verification from the user's side →
Resolution → Notes / prevention.**

**Reproduced vs. scenario:** tickets marked *Reproduced* were broken and fixed in the lab,
with screenshots as evidence. Any ticket that can't be reproduced in this environment
will be clearly labelled *Scenario* and contains no simulated evidence.

---

## Planned

| Area | Item |
|---|---|
| Lab upgrades | DHCP scope and reservation · Windows Server Backup and restore · PowerShell for bulk account creation and lockout reporting |
| Tickets | DNS fault presenting as "no internet" · repeated lockouts from a stale saved credential · APIPA address · broken domain trust · deleted file restore · bulk account creation and audit · Microsoft 365 leaver offboarding · reported phishing email (scenario) · laptop won't boot (scenario) |
| Service management | Triage decision trees for "I can't log in" and "I can't reach a resource" |

---

## Repository layout

```
.
├── README.md
├── docs/
│   ├── asset-register.md
│   ├── change-requests/        CR-00X write-ups and the CR template
│   ├── service-management/     Priority/SLA definitions, escalation matrix
│   └── tickets/                TICKET-0XX write-ups
└── screenshots/                Evidence, one folder per item (a1, a2, t001, t009 …)
```

---

*Last updated: 2026-10-30*
