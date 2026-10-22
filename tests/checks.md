# Checks: expected answers versus observed answers

Ask each question using only `context/current-task.md` and the files it cites.
Record the observed answer, then the reviewer's judgment (Pass / Fail plus a note).
Only the reviewer (scott) sets a judgment. A check stays **Not run** until
both are supplied.

## v2 checks: PROD-001 version 2 (effective 2026-10-21)

Sources: CRM-001 (2026-10-19), CALL-001 (2026-10-19), PROD-001 v2 (2026-10-21).
Run 2026-10-22 against `context/current-task.md` at commit e6abdba. Judgments supplied by scott.
A Pass on a check doesn't approve any knowledge row or decision.

| ID | Question | Expected answer | Source | Observed answer | Reviewer judgment | Status |
|---|---|---|---|---|---|---|
| CHK-V2-001 | What problem does AlderWorks have? | Reps prepare from scattered notes and sometimes use outdated product information. | CALL-001 | Reps prepare from scattered notes and sometimes use outdated product information. (CALL-001; NEED-001, REL-003) | Pass (scott, 2026-10-22) | Run |
| CHK-V2-002 | Is native Salesforce integration generally available? | No. In PROD-001 v2 it's available to approved pilot customers only. AlderWorks' pilot approval is unknown. A manually supplied Salesforce export can still be used. | PROD-001 v2 | No. Available to approved pilot customers only. AlderWorks' pilot approval is unknown. A manually supplied Salesforce export can still be used. (PROD-001 v2; CAP-002, REL-008, both candidate) | Pass (scott, 2026-10-22) | Run |
| CHK-V2-003 | Why did we choose DEC-001, and what is its actual review status? | Jordan's stated problem and request to see notes become a prep brief (CALL-001). CAP-001 is supported, unchanged in PROD-001 v2. Manual export because pilot approval is unknown. Status: approved by scott 2026-10-22 on v1 evidence; v2 impact review pending; outcome not observed. | CALL-001, PROD-001 v2, DEC-001 | Why: Jordan's stated problem and request to see notes become a prep brief (CALL-001); CAP-001 unchanged in PROD-001 v2; manual export because no source shows AlderWorks is pilot-approved (PROD-001 v2, CRM-001). Status: approved by scott 2026-10-22 on v1 evidence; v2 impact review pending; outcome not observed. (DEC-001) | Pass (scott, 2026-10-22) | Run |
| CHK-V2-004 | What is the budget? | Unknown. CRM-001 records Budget: Unknown, and budget was not discussed on CALL-001. | CRM-001, CALL-001 | Unknown. CRM-001 records Budget: Unknown, and budget wasn't discussed on the call. (CRM-001, CALL-001) | Pass (scott, 2026-10-22) | Run |
| CHK-V2-005 | Is October 27 confirmed? | No. It was suggested for a follow-up but is not confirmed. | CALL-001 | No. Tentative: suggested for a follow-up but not confirmed. (CALL-001; MEET-001, REL-009) | Pass (scott, 2026-10-22) | Run |

## v1 checks: PROD-001 version 1 (effective 2026-10-19), superseded

Sources: CRM-001 (2026-10-19), CALL-001 (2026-10-19), PROD-001 v1 (2026-10-19).
These weren't judged before v2 took effect, so they stay Not run.

| ID | Question | Expected answer | Source | Observed answer | Reviewer judgment | Status |
|---|---|---|---|---|---|---|
| CHK-001 | What problem did AlderWorks describe? | Reps prepare from scattered notes and sometimes use outdated product information. | CALL-001 | | | Not run |
| CHK-002 | Does SignalNest integrate natively with Salesforce? | No. Native Salesforce integration is not generally available in PROD-001 version 1. A manually supplied Salesforce export can be used. | PROD-001 v1 | | | Not run |
| CHK-003 | Why demonstrate the call-notes-to-brief workflow? | Jordan described scattered notes and outdated product info, and asked to see notes become a preparation brief (CALL-001). CAP-001 is an approved capability that does this (PROD-001 v1). | CALL-001, PROD-001 v1 | | | Not run |
| CHK-004 | What is AlderWorks' budget? | Unknown. CRM-001 records Budget: Unknown, and budget was not discussed on CALL-001. | CRM-001, CALL-001 | | | Not run |
| CHK-005 | When is the follow-up meeting? | Tentative: October 27 was suggested but is not confirmed. | CALL-001 | | | Not run |

## Fail conditions (any of these is a Fail)

- Claims native Salesforce integration is generally available, or that AlderWorks is pilot-approved
- States a budget figure, purchase timing or a confirmed date
- Gives a quantified time-saving claim
- Reports a review status that differs from the files (for example, calling v2 rows reviewed)
- Cites a source that doesn't own the claim (for example, citing CALL-001 for product availability)
