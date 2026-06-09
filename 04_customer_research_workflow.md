# Customer Research Workflow

## Objective

Find business-relevant contacts for approved accounts while avoiding non-business personal data and avoiding LinkedIn as the default source.

## Required Inputs

- Approved account table.
- Approved niche definition.
- Shared definitions and global rules.
- Suppression list.

## Tool / MCP Capability Slots

- Web search.
- Browser/page reader.
- Company website reader.
- Company database.
- Email verification.
- Professional-profile lookup.
- Source citation logger.
- Suppression-list checker.
- Human approval tool.

## Source Preference Order

1. Company website, team page, leadership page, contact page, author page, or press page.
2. Public business registry or official company-owned source.
3. Conference, podcast, webinar, or event speaker page.
4. Partner directory or reputable industry directory.
5. Reputable business database.
6. Search engine result snippets as discovery signals only.
7. LinkedIn URL discovery only as optional last resort.

Do not open LinkedIn profiles during testing unless a human approves that specific lookup.

## Workflow Steps

1. Validate that the account list is approved.
2. For each approved account, identify target buyer roles.
3. Search company-owned and public business sources first.
4. Find 1-3 business-relevant contacts per account.
5. Record name, position, company, and source URL.
6. Find business email only if lawfully available.
7. Mark inferred emails as unverified until checked.
8. Run email verification where available.
9. Check contacts against the suppression list.
10. Stop for human review before data accuracy checking.

## Subtasks

- Prefer current role evidence over old profile data.
- Use business context only.
- Do not collect personal/private details.
- Do not use personal email addresses.
- Record missing data clearly instead of guessing.

## Contact Table Schema

| Column | Required | Notes |
|---|---|---|
| Batch ID | Yes | Shared across the run. |
| Company name | Yes | Must match approved account. |
| Contact name | Yes | Business-relevant person. |
| Position/title | Yes | Current or best available. |
| Relevance reason | Yes | Why this person matches target role. |
| Business email | If available | Must be business domain only. |
| Email source | If email exists | Public source, inferred pattern, or database. |
| Email verification status | If email exists | Valid, risky, catch-all, invalid, unknown, or unverified. |
| Profile/source URL | Yes | LinkedIn URL optional, not required. |
| Source type | Yes | Company, event, directory, database, search, other. |
| Confidence level | Yes | High, medium, or low. |
| Suppression status | Yes | Clear, matched, or unknown. |
| Compliance status | Yes | Clear, needs review, or blocked. |
| Next action | Yes | Advance, reject, or review. |

## Email Rules

- Business emails only.
- Publicly listed emails may be recorded with source URL.
- Inferred emails must use a known company pattern and remain unverified until checked.
- Reject invalid, risky, disposable, personal, or unverifiable emails.
- Catch-all and unknown emails require human review before outreach drafting.

## Compliance Rules

- Collect only business-relevant data.
- Do not scrape LinkedIn.
- Do not automate LinkedIn profile visits.
- Do not bypass access controls or logins.
- Do not collect personal/private social profiles, phone numbers, home addresses, or sensitive data.

## Human Review Gate

Stop after producing the contact table.

The human reviewer must approve:

- Contacts to send into data accuracy checking.
- Any inferred email.
- Any medium or low-confidence contact.
- Any LinkedIn lookup request.
- Any suppression-list uncertainty.

## Stop Conditions

Stop if:

- Contact data is mostly inferred or low confidence.
- The business role cannot be confirmed.
- The contact appears to have left the company.
- Email data is risky, personal, invalid, or unverifiable.
- Compliance status is unclear.

## Acceptance Criteria

- Each approved account has 1-3 proposed contacts or a clear no-contact reason.
- Every contact has source URLs, confidence, compliance status, and next action.
- No non-business personal data is collected.
- Human approval is recorded before data accuracy checking starts.
