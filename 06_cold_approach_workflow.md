# Cold Approach Workflow

## Objective

Create personalized B2B outreach drafts for approved contacts. Do not send, schedule, auto-connect, auto-message, or automate outreach in V1.

## Required Inputs

- Human-approved data accuracy output.
- Approved niche definition.
- Approved market research.
- Shared definitions and global rules.
- Offer and proof points.
- Suppression list confirmation.

## Tool / MCP Capability Slots

- CRM or spreadsheet/database.
- Source citation logger.
- Optional deliverability checker.
- Human approval tool.

## Workflow Steps

1. Validate that contacts are approved for drafting.
2. Confirm suppression-list status is clear.
3. Select a message angle based on the ICP, account evidence, and contact role.
4. Draft one cold email.
5. Draft 2-3 subject line options.
6. Draft one LinkedIn connection note if LinkedIn is an approved channel.
7. Draft one LinkedIn follow-up if LinkedIn is an approved channel.
8. Draft 1-2 email follow-ups.
9. Record personalization evidence and source URLs.
10. Run compliance and quality checks.
11. Stop for human review.

## Outreach Draft Rules

- Drafts only.
- Use plain, direct business language.
- Mention only source-backed business context.
- Do not use fake familiarity.
- Do not exaggerate proof points.
- Do not mention private or sensitive data.
- Include opt-out language where appropriate.
- Keep messages concise.
- Make the call to action low-friction and relevant.

## Deliverability Readiness Check

Before any future sending outside V1, a human must confirm:

- SPF is configured.
- DKIM is configured.
- DMARC is configured.
- Sender identity is accurate.
- Opt-out handling exists.
- Sending volume is controlled.
- Bounce risk is low.
- Emails are verified.

If any item is unclear, do not send.

## Outreach Draft Table Schema

| Column | Required |
|---|---|
| Batch ID | Yes |
| Company | Yes |
| Contact | Yes |
| Position/title | Yes |
| Channel | Yes |
| Message angle | Yes |
| Subject line options | For email |
| Draft message | Yes |
| Follow-up draft | Yes |
| Personalization evidence | Yes |
| Source URLs | Yes |
| Compliance checklist status | Yes |
| Suppression status | Yes |
| Human approval status | Yes |
| Next action | Yes |

## Compliance Checklist

| Check | Status |
|---|---|
| Contact approved by data accuracy workflow |  |
| Suppression-list status clear |  |
| Business context only |  |
| No personal/private data |  |
| No deceptive subject line |  |
| Sender identity clear |  |
| Opt-out language included where appropriate |  |
| Source-backed personalization only |  |
| No sending automation |  |

## Human Review Gate

Stop after producing drafts.

The human reviewer must approve, edit, or reject:

- Message angle.
- Email draft.
- Subject lines.
- Follow-ups.
- LinkedIn note, if included.
- Compliance checklist.

No outreach may be sent from this workflow.

## Stop Conditions

Stop if:

- Contact approval is missing.
- Suppression status is unclear.
- Personalization evidence is weak or unverifiable.
- Drafts require claims not supported by sources.
- Compliance checklist fails.

## Acceptance Criteria

- Drafts are specific, source-backed, concise, and business-relevant.
- Every draft has a compliance checklist.
- No sending or scheduling occurs.
- Human approval is recorded.
