# Filtering Potential Customers Workflow

## Objective

Build a small, source-backed list of potential customer accounts from the approved niche and market research.

## Required Inputs

- Approved niche definition.
- Approved market research handoff.
- Shared definitions and global rules.
- Suppression list, if available at account level.

## Tool / MCP Capability Slots

- Web search.
- Browser/page reader.
- Company database.
- CRM or spreadsheet/database.
- Source citation logger.
- Suppression-list checker.
- Human approval tool.

## Workflow Steps

1. Validate that market research is approved.
2. Generate candidate accounts using approved search queries and filters.
3. Collect basic company data.
4. Check account-level disqualifiers.
5. Check duplicate companies.
6. Check account-level suppression-list conflicts.
7. Score each account using the fit scoring rubric.
8. Reject weak-fit accounts.
9. Produce a batch of 10-25 candidate accounts.
10. Stop for human review.

## Subtasks

- Prefer accounts with clear public evidence of ICP fit.
- Record why each account is included or rejected.
- Keep rejected-account notes so future agents avoid repeating poor searches.
- Do not collect contact-level data in this workflow.

## Account Table Schema

| Column | Required | Notes |
|---|---|---|
| Batch ID | Yes | Shared across the run. |
| Company name | Yes | Legal or public business name. |
| Website | Yes | Official website if available. |
| Geography | Yes | Match against approved ICP. |
| Segment | Yes | Approved market segment. |
| Company size | Yes | Exact or estimated. |
| Pain/trigger evidence | Yes | Source-backed. |
| Fit score | Yes | 0-100. |
| Disqualifiers checked | Yes | Include pass/fail notes. |
| Suppression status | Yes | Clear, matched, or unknown. |
| Source URLs | Yes | Minimum one reliable source. |
| Confidence level | Yes | High, medium, or low. |
| Compliance status | Yes | Clear, needs review, or blocked. |
| Next action | Yes | Approve, reject, or review. |

## Scoring / Qualification Rules

- Use the global fit scoring rubric.
- Accounts under 60 must be rejected unless the human reviewer overrides.
- Accounts from low-reliability sources require corroboration.
- Any disqualifier match must reject the account or mark it as needs review.

## Compliance Rules

- Do not collect contact names or emails in this workflow.
- Do not scrape behind logins.
- Do not include suppressed or sensitive accounts without human review.

## Human Review Gate

Stop after producing the account table.

The human reviewer must approve:

- Accounts to advance to contact research.
- Rejected-account reasons.
- Any account with medium or low confidence.
- Any suppression-list uncertainty.

## Stop Conditions

Stop if:

- Fewer than 10 accounts can be found with reliable evidence.
- Too many accounts are low confidence.
- Suppression-list status cannot be checked.
- Filters produce broad or irrelevant accounts.

## Acceptance Criteria

- 10-25 accounts are ready for review.
- Every account has a fit score, sources, confidence, and next action.
- Duplicate and suppression checks are complete.
- Human approval is recorded before customer research starts.
