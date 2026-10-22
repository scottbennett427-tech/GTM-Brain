# Current task: prepare the next AlderWorks touchpoint

Draft built 2026-10-22 from reviewed knowledge rows and DEC-001.
File status: **draft, awaiting reviewer (scott)**. Saving it doesn't approve it.
Fictional training data only.

## Status at a glance

| Item | Status |
|---|---|
| Knowledge rows used | reviewed (scott, 2026-10-22) |
| DEC-001 next demonstration | **approved** (scott, 2026-10-22) |
| Follow-up date | **tentative**: October 27 suggested, not confirmed |
| Demonstration outcome | **not observed** |

## Source versions

| Source | Version / date | Owner | Owns |
|---|---|---|---|
| CRM-001 | Recorded 2026-10-19 | Revenue Operations | Account identity and CRM fields |
| CALL-001 | Event date 2026-10-19 | Account Executive | What the customer said |
| PROD-001 | Version 1, effective 2026-10-19 | Product Marketing | Approved capabilities and claims |

## Who and what

- Account: ACCT-001 AlderWorks. CRM used: Salesforce (CRM-001, REL-002).
- Contact: PERSON-001 Jordan Lee. Title: Unknown (CRM-001, REL-001).

## Customer problem (CALL-001)

"Jordan Lee says reps prepare from scattered notes and sometimes use outdated product information." (NEED-001, REL-003)

Jordan asked to see "how supplied call notes can become a useful preparation brief." (REL-007, interpretation)

## Decision: what to demonstrate (DEC-001, approved)

Demonstrate CAP-001: SignalNest turning supplied AlderWorks call notes plus
approved product reference (PROD-001 v1) into a preparation brief. Use a
manually supplied Salesforce export (CAP-002) as the CRM input.

## Rationale

1. It's the customer's stated problem (CALL-001).
2. It's exactly what the customer asked to see (CALL-001).
3. CAP-001 is an approved capability (PROD-001 v1).
4. AlderWorks uses Salesforce (CRM-001), so the open Salesforce question needs
   the approved answer (PROD-001 v1).

## Approved answer to the Salesforce question

Jordan asked whether SignalNest connects directly to Salesforce (REQ-001). The
rep said this needs confirmation. The approved answer from PROD-001 v1:
"Native Salesforce integration is not generally available. A manually supplied Salesforce export can be used." (REL-008, interpretation)

Customer interest doesn't make a capability available.

## Do not claim

- Any quantified time saving ("No quantified time-saving claim is approved." PROD-001 v1)
- A native or direct Salesforce connection

## Unknowns (ask; don't assume)

| Unknown | Source showing it's unknown |
|---|---|
| Jordan Lee's title | CRM-001: "Contact title: Unknown" |
| Budget | CRM-001: "Budget: Unknown"; CALL-001: "Budget and purchase timing were not discussed." |
| Purchase timing | CALL-001: "Budget and purchase timing were not discussed." |
| Follow-up date | CALL-001: "October 27 is suggested for a follow-up, but is not confirmed." |
| Whether a manual Salesforce export is acceptable to AlderWorks | Not in any source |

## Limitations

- Based on three fictional sources only. There's no live CRM or call system behind them.
- No connector: the Salesforce data in a demo comes from a manual export.
- The approval covers the demo plan. It doesn't confirm the date or the deal.
- The outcome hasn't been observed. Record it in DEC-001 after the touchpoint.

## Refresh this file when

- PROD-001 gets a new version (especially Salesforce integration status)
- CRM-001 changes (title, budget, contacts)
- A new call or email source is added for ACCT-001
- The follow-up date is confirmed, moved or cancelled
- DEC-001 changes status or records an outcome

After any refresh: rebuild `views/connections.md` and rerun `tests/checks.md`.
