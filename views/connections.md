# Connections view (derived)

This table is **derived** from `knowledge/entities.csv`, `knowledge/relationships.csv`
and `decisions/DEC-001.md`. Don't edit it by hand: rebuild it whenever a source or
knowledge row changes. It is a plain knowledge/context graph written as a table.
It is not a graph database and not an automatic connector.

Rebuilt: 2026-10-22, after review. All rows **reviewed** by scott; DEC-001 **approved**.

## Customer need → capability → decision

| Customer need / request | Evidence | Capability or answer | Evidence | Link type | Decision |
|---|---|---|---|---|---|
| NEED-001: Reps prepare from scattered notes and sometimes use outdated product information | CALL-001 (REL-003) | CAP-001: Creates preparation drafts from supplied notes and approved reference documents | PROD-001 v1 (REL-005) | Interpretation, REL-007 (CALL-001 + PROD-001) | DEC-001 (approved): demo the call-notes-to-brief workflow |
| REQ-001: Asked whether SignalNest connects directly to Salesforce | CALL-001 (REL-004) | CAP-002: Manual Salesforce export. Native integration **not generally available** | PROD-001 v1 (REL-006) | Interpretation, REL-008 (CALL-001 + PROD-001) | DEC-001 (approved): use the export in the demo and state the limitation |
| MEET-001: Follow-up suggested for October 27 | CALL-001 (REL-009) | n/a | n/a | Fact | DEC-001 timing: **tentative**, confirm the date |

## Account context

| From | Relationship | To | Source |
|---|---|---|---|
| PERSON-001 Jordan Lee | contact_at | ACCT-001 AlderWorks | CRM-001 (REL-001) |
| ACCT-001 AlderWorks | uses_crm | SYS-001 Salesforce | CRM-001 (REL-002) |
