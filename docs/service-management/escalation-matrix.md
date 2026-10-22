# Escalation matrix

## Tiers
<!-- One line each in your own words: Tier 1, Tier 2, Tier 3, Security. -->
Tier 1: known fixes, using standard tools
Tier 2: deeper troubleshooting, hardware, on site work
Tier 3: servers, network, group policy and anything that needs a change request
Security: anything suspicious 


| Issue | First owner | Escalate to | Escalate when |
|---|---|---|---|
| Password reset or account unlock | Tier 1 | Tier 2 | User has correct password but still cannot login |
| Repeated lockouts on one account | Tier 1 | Security | suspicious activity |
| Mapped drive or share access | Tier 1 | Tier 2 | Need to change |
| Group Policy not applying |Tier 1 | Tier 3 | Need to edit GPO |
| PC won't boot / hardware fault | Tier 1 | Tier 2 | hardware work |
| New starter or leaver | Tier 1 | Tier 2 | Needs to remove user from security groups |
| Phishing email or suspicious activity | Tier 1 | Security  | Email looks suspicious |
| Server or DC down / many users affected | Tier 1 | Tier 3 | Need to Solve server/ DC issues |
| Microsoft 365 / Outlook issue | Tier 1 | Tier 3 | Change request needed |

## Rules
- During handover, first owner must asses, diagnose and handoff accordingly
- Tier 1 must never click suspicious links
- 
