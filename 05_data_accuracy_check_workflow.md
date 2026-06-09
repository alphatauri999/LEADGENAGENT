# Data Accuracy Check Workflow

## Objective

Verify that account and contact data is accurate enough to support outreach drafting.

## Required Inputs

- Approved contact table.
- Approved account table.
- Niche definition.
- Shared definitions and global rules.
- Suppression list.

## Tool / MCP Capability Slots

- Web search.
- Browser/page reader.
- Company website reader.
- Email verification.
- CRM or spreadsheet/database.
- Source citation logger.
- Suppression-list checker.
- Human approval tool.

## Workflow Steps

1. Validate that customer research is approved.
2. Check company-account match.
3. Check contact name accuracy.
4. Check position/title accuracy.
5. Check current company employment evidence.
6. Check email source and verification status.
7. Check duplicate contacts and duplicate companies.
8. Check suppression-list conflicts.
9. Assign final confidence and compliance status.
10. Block records that do not pass accuracy requirements.
11. Stop for human review before outreach drafting.

## Accuracy Checks

| Check | Pass Criteria | Fail Action |
|---|---|---|
| Name accuracy | Name appears on a reliable business source. | Mark needs review or reject. |
| Position accuracy | Current role is confirmed by recent or authoritative source. | Mark needs review. |
| Company match | Contact clearly works at the approved account. | Reject. |
| Email accuracy | Business email is valid or approved for review. | Reject or needs review. |
| Source quality | Key fields have source URLs. | Needs review. |
| Duplicate check | No duplicate company/contact in batch or CRM. | Merge or reject duplicate. |
| Suppression check | No suppression-list match. | Block. |
| Compliance check | Business-relevant and permitted. | Block or needs review. |

## Final Status Values

| Status | Meaning |
|---|---|
| Approved for drafting | Record may move to cold approach drafting. |
| Needs human review | Record has uncertainty that must be resolved. |
| Rejected | Record must not be used. |
| Blocked | Record violates suppression, compliance, or data-quality rules. |

## Data Accuracy Output Schema

| Column | Required |
|---|---|
| Batch ID | Yes |
| Company name | Yes |
| Contact name | Yes |
| Position/title | Yes |
| Business email | If available |
| Email verification status | If email exists |
| Name source URL | Yes |
| Position source URL | Yes |
| Company match source URL | Yes |
| Source reliability | Yes |
| Confidence level | Yes |
| Duplicate status | Yes |
| Suppression status | Yes |
| Compliance status | Yes |
| Final status | Yes |
| Reviewer notes | If applicable |

## Compliance Rules

- Do not repair weak data by guessing.
- Do not use search snippets as final proof unless corroborated.
- Do not use personal emails.
- Do not advance blocked, suppressed, invalid, or unverifiable contacts.

## Human Review Gate

Stop after producing the data accuracy output.

The human reviewer must approve:

- Contacts approved for outreach drafting.
- Any medium-confidence records.
- Any catch-all or unknown email statuses.
- Any record with conflicting sources.

## Stop Conditions

Stop if:

- Most records fail accuracy checks.
- Suppression-list access is unavailable.
- Email verification is unavailable and emails are mostly inferred.
- Key source URLs are missing.
- Compliance status is unclear.

## Acceptance Criteria

- Only accurate, source-backed, compliant records advance.
- Bad records are rejected or blocked with reasons.
- Duplicate and suppression checks are complete.
- Human approval is recorded before outreach drafting starts.
