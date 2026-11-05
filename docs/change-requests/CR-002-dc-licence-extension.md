# CR-002 — Extend domain controller evaluation licence

| Field | Value |
|---|---|
| Requested by | J. Saraza (IT) |
| Implemented by | J. Saraza |
| Approved by | Self (lab). In production: |
| Date / window | 2026-11-05, |
| Change type | |
| Risk | |
| Systems affected | AD-DC01: Windows Server 2022 Standard Evaluation licence (requires a restart) |
| Users affected | |

<!-- Approved by: who signs off on restarting a domain controller in a real company? -->
<!-- Window: when would you reboot a DC in production, and why not mid-morning? -->
<!-- Change type: Standard, Normal or Emergency? You haven't done this before. -->
<!-- Risk: the command is low risk; the restart isn't. Who loses what, and for how long? -->
<!-- Users affected: what can't anyone do while the only DC is restarting? -->

## Reason for change
<!-- 2–3 sentences: link to the asset register finding. What happens if the licence expires, and why is this a stopgap rather than a real fix? -->

## Current state (before), with evidence
`slmgr /dlv` on AD-DC01, 2026-11-05:

    Timebased activation expiration:
    Remaining Windows rearm count:

<!-- Fill in both values from your screenshot. -->
![Licence status before the change](../../screenshots/cr-002/cr-002-before-dlv.png)

## Implementation steps
1. Take a VirtualBox snapshot of AD-DC01 named `pre-CR-002`.
2. Run `slmgr /dlv` as administrator and record the expiry and rearm count.
3. Run `slmgr /rearm` as administrator.
4. Restart AD-DC01 from inside Windows.
5. Run `slmgr /dlv` again and confirm the evaluation period was restored.

## Backout plan
Rollback trigger:
<!-- What result would make you roll back? E.g. the DC doesn't boot, or users can't sign in afterwards. -->

1.
<!-- A rearm can't be undone, so what's the backout, and what does using it cost you? -->

## Verification, from the user's side
**Test:** after the restart, sign in to AD-CL01 as `agarcia` and open the S: drive.
**Expected:** sign-in succeeds and S: opens. On the DC, `slmgr /dlv` shows the evaluation period restored and the rearm count reduced by one.

**Result:**

![Licence status after the change](../../screenshots/cr-002/cr-002-after-dlv.png)
![User-side check](../../screenshots/cr-002/cr-002-user-check.png)

## Outcome
<!-- Completed / Rolled back / Partial; the new expiry date; anything unexpected; what happens to the pre-CR-002 snapshot; and when this has to be done again. -->