# Connections view (derived)

This table is **derived** from `knowledge/entities.csv`, `knowledge/relationships.csv`
and `decisions/DEC-001.md`. Don't edit it by hand: rebuild it whenever a source or
knowledge row changes. It is a plain knowledge/context graph written as a table.
It is not a graph database and not an automatic connector.

Rebuilt: 2026-10-22 after PROD-001 v2 (effective 2026-10-21).
Statuses are shown per row. Rows changed by v2 are **candidate** until reviewed.

## Customer need → capability → decision

| Customer need / request | Evidence | Capability or answer | Evidence | Link type (status) | Decision |
|---|---|---|---|---|---|
| NEED-001: Reps prepare from scattered notes and sometimes use outdated product information (reviewed) | CALL-001 (REL-003) | CAP-001: Creates preparation drafts from supplied notes and approved reference documents (reviewed) | PROD-001 v2, text unchanged from v1 (REL-005) | Interpretation, REL-007 (reviewed) | DEC-001 (approved on v1; v2 impact pending): demo the call-notes-to-brief workflow |
| REQ-001: Asked whether SignalNest connects directly to Salesforce (reviewed) | CALL-001 (REL-004) | CAP-002: Native integration for **approved pilot customers only**; manual export still supported (**candidate**) | PROD-001 v2 (REL-006, candidate) | Interpretation, REL-008 (**candidate**) | DEC-001: use the manual export. AlderWorks pilot approval **unknown**. |
| MEET-001: Follow-up suggested for October 27 (reviewed) | CALL-001 (REL-009) | n/a | n/a | Fact | DEC-001 timing: **tentative**, confirm the date |

## Account context

| From | Relationship | To | Source | Status |
|---|---|---|---|---|
| PERSON-001 Jordan Lee | contact_at | ACCT-001 AlderWorks | CRM-001 (REL-001) | reviewed |
| ACCT-001 AlderWorks | uses_crm | SYS-001 Salesforce | CRM-001 (REL-002) | reviewed |
