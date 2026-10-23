# Escalation matrix

## Tiers
- Tier 1: known fixes, using standard tools
- Tier 2: deeper troubleshooting, hardware, on site work
- Tier 3: servers, network, group policy and anything that needs a change request
- Security: anything suspicious 

| Issue | First owner | Escalate to | Escalate when |
|---|---|---|---|
| Password reset or account unlock | Tier 1 | Tier 2 | User has correct password but still cannot login |
| Repeated lockouts on one account | Tier 1 | Tier 2 | Each lockout writes event 4740 to the DC's Security log |
| Mapped drive or share access | Tier 1 | Tier 2 | Need to change OU to different place |
| Group Policy not applying |Tier 1 | Tier 3 | Need to edit GPO |
| PC won't boot / hardware fault | Tier 1 | Tier 2 | Won't boot after checking all power, cables and unplugging peripherals. |
| New starter or leaver | Tier 1 | Tier 2 | User is planned to start or to leave or urgent i.e. someone was fired |
| Phishing email or suspicious activity | Tier 1 | Security  | Email looks suspicious as other staff have received the same email, security needs the original email to investigate and examining malicious email safely is specialist work |
| Server or DC down / many users affected | Tier 1 | Tier 3 | Need to Solve server/ DC issues |
| Microsoft 365 / Outlook issue | Tier 1 | Tier 3 | Change request needed |

## Rules
- During handover, first owner must asses what the user reported, check and see what each check rules out and list it, list what has already been tried and the priority and how many users were affected
- Tier 1 must never click suspicious links, forward suspicious links or delete it before security has had a chance to check it out.
