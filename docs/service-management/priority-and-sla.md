# Priority and SLA definitions

Priority is set from **impact** (how many people are affected) and **urgency** (how badly it stops work).

## Priority matrix
| Impact \ Urgency | High: work stopped, no workaround | Medium: degraded, workaround exists | Low: inconvenience or request |
|---|---|---|---|
| **Company-wide or critical service** | P1 | P2 | P3 |
| **Department or group** | P2 | P2 | P3 |
| **Single user** | P2 | P3 | P4 |

<!-- Can you defend every cell? Teck supports executives. Would you raise an executive's single-user issue a level? Change the matrix or add a rule. -->

## SLA targets
| Priority | Name | Example | First response | Resolution target | Coverage |
|---|---|---|---|---|---|
| P1 | Critical | Domain controller down, so no one can sign in | Instant - 15mins | 4 Hours | 24/7 |
| P2 | High | Salesshare unreachable for the whole sales department | 30 mins | 8 Hours | 24/7 |
| P3 | Medium | One User's S: drive missing | 4 business hours | 3 business days | Business hours |
| P4 | Low | User asks for a new desktop shortcut or a software install | 1 business day | 5 business days | Business hours |

<!-- Use lab examples where you can, e.g. DC down = nobody can sign in. -->

## Rules
<!-- 3–4 rules in your own words: who sets priority; when it gets raised (e.g. a second user reports the same thing); what happens when an SLA is about to be missed. -->
1. Who sets the priority?
  The person who logs the ticket (tier 1) sets it using the matrix. The user does not. The user's input is input to the decision, not the decision
2. When does priority go up?
  Issues for executives get bumped up a priority unless executive issue is a low priority request. When a second user reports the exact same problem. It is no longer a single user issue so tickets are linked together and the matrix is rechecked. When the workaround no longer works is another time to increase priority.
3. When can it go down?
   Once a workaround has the user working again.
4. What happens when an SLA is about to be missed?
   Escalate priority before the deadline not after. A common trigger is 75% of the resolution time used up: tell the team lead or the next tier and update the user.



## Tickets in this portfolio
| Ticket | Priority | Why |
|---|---|---|
| TICKET-001 | | |
