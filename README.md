# GTM-Brain

A small, reviewable GTM brain built from **fictional training data** (account
AlderWorks, contact Jordan Lee, product SignalNest). Plain Markdown and CSV
files only: no scripts, no database, no connectors.

Lab owner / reviewer: **scott**

## Architecture

```
original sources  →  reviewed knowledge  →  decision + rationale  →  task context  →  checked answer
  sources/            knowledge/            decisions/              context/          tests/
  governance/         views/ (derived)
```

| Layer | What it holds | Why it exists |
|---|---|---|
| 1. Original sources | CRM record, call notes and approved product information, kept word for word | It's the evidence. It's never rewritten, so anything can be traced back to what was recorded. |
| 2. Reviewed knowledge | Entities and relationships, each tied to a source ID and an exact excerpt | Turns raw text into checkable facts. Everything starts as `candidate` until a human reviews it. |
| 3. Decision and rationale | DEC-001: what to do next, why, alternatives and unknowns | Keeps a recommendation separate from the facts it's based on, and keeps "proposed" separate from "approved". |
| 4. Task context | `context/current-task.md`: only what's needed for the next touchpoint | Gives a person or an AI a focused, sourced brief instead of every file. |
| 5. Checked answer | `tests/checks.md`: expected answers versus observed answers | Shows whether answers built from this context are correct before anyone relies on them. |

## Files

| Path | Layer | Status |
|---|---|---|
| `sources/account.md` | Source: CRM-001 | Verbatim |
| `sources/call.md` | Source: CALL-001 | Verbatim |
| `sources/product.md` | Source: PROD-001 v2 (effective 2026-10-21) | Authorized fictional update; v1 kept in git history and DEC-001 |
| `governance/rules.md` | Rules | Verbatim except reviewer name |
| `knowledge/entities.csv` | Knowledge | reviewed (scott, 2026-10-22); CAP-002 re-reviewed on v2 |
| `knowledge/relationships.csv` | Knowledge | reviewed (scott, 2026-10-22); REL-006, REL-008 re-reviewed on v2 |
| `decisions/DEC-001.md` | Decision | approved (scott, 2026-10-22) on v1 evidence; v2 impact note approved; outcome not observed |
| `views/connections.md` | Derived view | Rebuilt from knowledge |
| `context/current-task.md` | Task context | Approved (scott, 2026-10-22); uses PROD-001 v2 |
| `tests/checks.md` | Checks | v2: 5 Run, all Pass (scott, 2026-10-22); v1: 5 Not run (superseded) |

### Evidence format in `relationships.csv`

- `evidence_excerpt` holds exact source text. When a row needs more than one
  quote, the quotes are joined by ` || `.
- When a row draws on two sources, `source_id` lists both (for example
  `CALL-001;PROD-001`), and the quotes appear in the same order.
- Relationships starting with `interpretation_` are judgments that connect a
  customer need to a capability. They're not facts stated by any one source.

## Which source owns which claims

| Source | Owner | Authoritative for | Not authoritative for |
|---|---|---|---|
| CRM-001 | Revenue Operations | Account identity and CRM fields (name, contact, CRM used, budget = Unknown) | What the customer said, product facts |
| CALL-001 | Account Executive | What the customer said and asked | Product availability or capabilities |
| PROD-001 v2 | Product Marketing | Approved capabilities and claims | Customer needs, account fields or a customer's pilot eligibility |

**Customer interest doesn't establish product availability or eligibility.** Jordan
asked about a direct Salesforce connection (CALL-001). PROD-001 v2 says native
Salesforce integration is available to approved pilot customers only, and no
source shows AlderWorks is one. A manual export is still supported.

## Review workflow

1. AI-generated rows start as `candidate`.
2. The reviewer (scott) checks each row against its source excerpt.
3. Only rows the reviewer explicitly approves move to `reviewed`.
4. Decisions stay `proposed` until approval is recorded explicitly.
5. Commit messages record the reviewer and the date.
6. When a source changes: inspect the affected rows, decisions and context, rebuild
   `views/connections.md`, then rerun `tests/checks.md`.

## Safety

Fictional lab data only. No credentials. No external actions. Real customer data
needs approval for storage and model processing first.
