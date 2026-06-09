# Definitions And Global Rules

Use this file as the shared operating standard for every lead generation workflow. Agents must follow these rules unless a human reviewer explicitly overrides them in writing.

## Core Definitions

| Term | Definition |
|---|---|
| ICP | Ideal Customer Profile. The target company and buyer profile most likely to benefit from the offer. |
| Niche | A specific market segment defined by industry, geography, company type, buyer role, pain, and offer fit. |
| Account | A target company or organization. |
| Contact | A business-relevant person at an approved account. |
| Fit Score | A score that estimates how closely an account matches the approved ICP. |
| Confidence Score | A source-backed estimate of how reliable a claim or data point is. |
| Buying Trigger | A public signal that suggests the account may need the offer now. |
| Disqualifier | A reason to reject an account or contact before outreach. |
| Verified Email | A business email confirmed by an email verification tool or authoritative public source. |
| Suppression List | A do-not-contact list that must be checked before outreach drafting. |
| Human Review Gate | A mandatory stop where a human approves, rejects, or requests revisions before the next workflow starts. |
| Stop Condition | A rule that requires the agent to stop instead of continuing with uncertain, risky, or incomplete data. |

## Global Operating Rules

- Work in small test batches: 10-25 accounts and 1-3 contacts per approved account.
- Do not collect non-business personal data.
- Required contact data is limited to name, position, company, business email if lawfully available, source URL, confidence level, and compliance status.
- LinkedIn URLs are optional, not required.
- Prefer company-owned and authoritative public sources.
- Use search engines to discover public business information, but do not treat search snippets as final proof unless corroborated.
- Do not scrape LinkedIn or automate LinkedIn activity.
- Do not scrape behind logins, bypass access controls, or violate platform terms.
- Do not send, schedule, auto-connect, auto-message, or automate outreach in V1.
- Every workflow must end with a human review gate.
- Every approved record must include source URLs, confidence level, compliance status, and next action.

## Source Reliability Ranking

| Reliability | Source Types |
|---|---|
| High | Company website, official press release, public business registry, company-owned profile, verified company-owned source. |
| Medium | Conference page, partner directory, reputable business database, industry publication, podcast/event page. |
| Low | Search snippet, outdated directory, unverifiable third-party listing, copied profile aggregator. |

## Confidence Scoring

| Confidence | Criteria |
|---|---|
| High | Confirmed by a company-owned source or at least two reliable sources. |
| Medium | Confirmed by one reliable third-party source. |
| Low | Inferred, outdated, conflicting, search-snippet-only, or weakly sourced. |

Low-confidence records must not advance to outreach drafting without human approval.

## Fit Scoring Rubric

Score each account from 0 to 100.

| Dimension | Points |
|---|---:|
| Industry and niche fit | 20 |
| Geography fit | 10 |
| Company size fit | 10 |
| Buyer role availability | 10 |
| Pain likelihood | 15 |
| Buying trigger evidence | 15 |
| Offer relevance | 10 |
| Source confidence | 5 |
| Disqualifier risk | 5 |

Recommended interpretation:

- 80-100: strong fit
- 60-79: possible fit, needs review
- 0-59: reject unless human reviewer overrides

## Suppression List Rules

Before outreach drafting, check for:

- Unsubscribed contacts.
- Existing customers.
- Existing active deals.
- Competitors.
- Rejected leads.
- Sensitive accounts.
- Previous negative replies.
- Bounced emails.
- Personal/private email addresses.

Any suppression-list match must stop the workflow unless a human reviewer explicitly approves a non-outreach next action.

## Compliance And Platform Guardrails

- Keep all processing business-relevant and proportional.
- Record the source and purpose for each collected contact data point.
- Do not use deceptive subject lines, fake familiarity, exaggerated claims, or unverifiable personalization.
- Email drafts must include appropriate sender identity and opt-out language.
- Do not use personal emails unless the niche definition and compliance review explicitly allow it.
- If compliance status is unclear, stop and request human review.

## Human Review Decisions

At every review gate, the human reviewer must choose one:

- Approved: continue to the next workflow.
- Approved with edits: apply reviewer changes before continuing.
- Needs revision: repeat the current workflow with reviewer notes.
- Rejected: stop and log the reason.

## Standard Handoff Requirements

Every workflow handoff must include:

- Workflow name.
- Niche or campaign name.
- Date.
- Batch ID.
- Inputs used.
- Outputs produced.
- Source URLs.
- Confidence levels.
- Compliance status.
- Human review status.
- Next action.
