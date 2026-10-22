# Current task: prepare the next AlderWorks touchpoint

Draft rebuilt 2026-10-22 after PROD-001 version 2 (effective 2026-10-21).
File status: **approved by scott, 2026-10-22**.
Fictional training data only.

## Status at a glance

| Item | Status |
|---|---|
| Product source in use | **PROD-001 version 2**, effective 2026-10-21 (supersedes v1, 2026-10-19) |
| Knowledge rows | all 18 reviewed (scott, 2026-10-22); CAP-002, REL-006, REL-008 re-reviewed on v2 |
| DEC-001 next demonstration | **approved** (scott, 2026-10-22) on PROD-001 v1 evidence; **v2 impact note approved** (scott, 2026-10-22) |
| Follow-up date | **tentative**: October 27 suggested, not confirmed |
| Demonstration outcome | **not observed** |

## Source versions

| Source | Version / date | Owner | Owns |
|---|---|---|---|
| CRM-001 | Recorded 2026-10-19 | Revenue Operations | Account identity and CRM fields |
| CALL-001 | Event date 2026-10-19 | Account Executive | What the customer said |
| PROD-001 | **Version 2, effective 2026-10-21** | Product Marketing | Approved capabilities and claims |

## Who and what

- Account: ACCT-001 AlderWorks. CRM used: Salesforce (CRM-001, REL-002).
- Contact: PERSON-001 Jordan Lee. Title: Unknown (CRM-001, REL-001).

## Customer problem (CALL-001)

"Jordan Lee says reps prepare from scattered notes and sometimes use outdated product information." (NEED-001, REL-003)

Jordan asked to see "how supplied call notes can become a useful preparation brief." (REL-007, interpretation)

## Decision: what to demonstrate (DEC-001)

Demonstrate CAP-001: SignalNest turning supplied AlderWorks call notes plus
approved product reference (PROD-001 v2) into a preparation brief. Use a
manually supplied Salesforce export (CAP-002) as the CRM input.

Status: approved by scott on 2026-10-22 on PROD-001 v1 evidence. The v2 impact
note (recommendation unchanged) was approved by scott on 2026-10-22.

## Rationale

1. It's the customer's stated problem (CALL-001).
2. It's exactly what the customer asked to see (CALL-001).
3. CAP-001 is an approved capability, unchanged in PROD-001 v2.
4. AlderWorks uses Salesforce (CRM-001). Native integration is limited to
   approved pilot customers (PROD-001 v2), and no source shows AlderWorks is
   one, so the demo uses the manual export.

## Answer to the Salesforce question (PROD-001 v2; rows reviewed)

Jordan asked whether SignalNest connects directly to Salesforce (REQ-001). The
rep said this needs confirmation. PROD-001 v2:
"Native Salesforce integration is available to approved pilot customers only. A manually supplied Salesforce export can still be used." (REL-008, interpretation, reviewed)

So native integration is **not generally available**. AlderWorks' pilot
approval is **unknown**. Customer interest doesn't establish eligibility.

## Do not claim

- That native Salesforce integration is generally available
- That AlderWorks is approved for, or eligible for, the pilot
- Any quantified time saving ("No quantified time-saving claim is approved." PROD-001 v2)

## Unknowns (ask; don't assume)

| Unknown | Source showing it's unknown |
|---|---|
| Jordan Lee's title | CRM-001: "Contact title: Unknown" |
| Budget | CRM-001: "Budget: Unknown"; CALL-001: "Budget and purchase timing were not discussed." |
| Purchase timing | CALL-001: "Budget and purchase timing were not discussed." |
| Follow-up date | CALL-001: "October 27 is suggested for a follow-up, but is not confirmed." |
| AlderWorks pilot approval for native Salesforce integration | No source records it (noted in the v2 update authorized by scott) |
| Whether a manual Salesforce export is acceptable to AlderWorks | Not in any source |

## Limitations

- Based on three fictional sources only. There's no live CRM or call system behind them.
- No connector: the Salesforce data in a demo comes from a manual export.
- The approval covers the demo plan. It doesn't confirm the date, the deal or pilot eligibility.
- The outcome hasn't been observed. Record it in DEC-001 after the touchpoint.

## Refresh this file when

- PROD-001 gets a new version (last refresh: v2, effective 2026-10-21)
- A source records AlderWorks' pilot approval or rejection
- CRM-001 changes (title, budget, contacts)
- A new call or email source is added for ACCT-001
- The follow-up date is confirmed, moved or cancelled
- DEC-001 changes status, gets its v2 impact reviewed, or records an outcome

After any refresh: rebuild `views/connections.md` and rerun `tests/checks.md`.
