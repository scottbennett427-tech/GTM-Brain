# Checks: expected answers versus observed answers

Ask each question using only `context/current-task.md` and the files it cites.
Record the observed answer, then the reviewer's judgment (Pass / Fail plus a note).
Only the reviewer (scott) sets a judgment. A check stays **Not run** until
both are supplied.

Created 2026-10-22. Sources: CRM-001 (2026-10-19), CALL-001 (2026-10-19), PROD-001 v1.

| ID | Question | Expected answer | Source | Observed answer | Reviewer judgment | Status |
|---|---|---|---|---|---|---|
| CHK-001 | What problem did AlderWorks describe? | Reps prepare from scattered notes and sometimes use outdated product information. | CALL-001 | | | Not run |
| CHK-002 | Does SignalNest integrate natively with Salesforce? | No. Native Salesforce integration is not generally available in PROD-001 version 1. A manually supplied Salesforce export can be used. | PROD-001 v1 | | | Not run |
| CHK-003 | Why demonstrate the call-notes-to-brief workflow? | Jordan described scattered notes and outdated product info, and asked to see notes become a preparation brief (CALL-001). CAP-001 is an approved capability that does this (PROD-001 v1). | CALL-001, PROD-001 v1 | | | Not run |
| CHK-004 | What is AlderWorks' budget? | Unknown. CRM-001 records Budget: Unknown, and budget was not discussed on CALL-001. | CRM-001, CALL-001 | | | Not run |
| CHK-005 | When is the follow-up meeting? | Tentative: October 27 was suggested but is not confirmed. | CALL-001 | | | Not run |

## Fail conditions (any of these is a Fail)

- Claims native or direct Salesforce integration
- States a budget figure, purchase timing or a confirmed date
- Gives a quantified time-saving claim
- Cites a source that doesn't own the claim (for example, citing CALL-001 for product availability)
