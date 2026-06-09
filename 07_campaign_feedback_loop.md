# Campaign Feedback Loop

## Objective

Capture test outcomes and convert them into better ICP rules, source choices, scoring, disqualifiers, and outreach messaging.

## Required Inputs

- Run log.
- Approved outreach drafts.
- Human reviewer notes.
- Campaign results, if outreach was sent manually outside V1.

## Tool / MCP Capability Slots

- CRM or spreadsheet/database.
- Source citation logger.
- Human approval tool.
- Optional email deliverability report.

## Feedback Categories

| Category | Values |
|---|---|
| Account outcome | Good fit, bad fit, duplicate, competitor, customer, active deal, rejected. |
| Contact outcome | Correct contact, wrong role, left company, duplicate, suppressed, bounced, invalid. |
| Outreach outcome | Not sent, sent manually, replied, no reply, positive reply, negative reply, meeting booked. |
| Objection type | Not relevant, no budget, wrong timing, wrong person, already solved, unclear offer, other. |
| Data issue | Bad email, outdated role, weak source, duplicate, missing source, compliance concern. |
| Message issue | Too generic, weak pain, weak proof, unclear CTA, too long, wrong tone. |

## Workflow Steps

1. Collect outcomes for each account and contact.
2. Identify rejected segments and repeated disqualifiers.
3. Identify source types that produced accurate data.
4. Identify source types that produced bad data.
5. Review fit scores against actual outcomes.
6. Review message angles against replies or reviewer feedback.
7. Update campaign memory.
8. Recommend changes for the next test batch.
9. Stop for human review.

## Campaign Memory Schema

| Field | Required |
|---|---|
| Campaign name | Yes |
| Batch ID | Yes |
| Date | Yes |
| What worked | Yes |
| What failed | Yes |
| Good segments | Yes |
| Bad segments | Yes |
| Good source types | Yes |
| Bad source types | Yes |
| Scoring changes | Yes |
| Disqualifier changes | Yes |
| Message angle changes | Yes |
| Compliance notes | Yes |
| Next test recommendation | Yes |

## Quality Rules

- Do not generalize from one result unless marked as an assumption.
- Separate reviewer opinion from measured outcome.
- Preserve negative findings so agents do not repeat them.
- Update source reliability notes when data accuracy fails.
- Update suppression list when contacts opt out, bounce, or respond negatively.

## Human Review Gate

Stop after producing feedback recommendations.

The human reviewer must approve:

- ICP changes.
- Scoring changes.
- Disqualifier changes.
- Message angle changes.
- Suppression-list updates.
- Next batch recommendation.

## Stop Conditions

Stop if:

- Outcome data is missing or unreliable.
- Suppression-list updates are unclear.
- Feedback would expand outreach volume without evidence of quality.

## Acceptance Criteria

- Feedback is recorded in structured form.
- Next batch recommendations are specific.
- Lessons learned are reusable by future agents.
- Human approval is recorded.
