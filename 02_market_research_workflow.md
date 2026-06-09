# Market Research Workflow

## Objective

Research the approved niche and produce source-backed market assumptions, priority segments, buying triggers, disqualifiers, and account filtering criteria.

## Required Inputs

- Approved niche definition.
- Shared definitions and global rules.
- Available tool / MCP capability list.

## Tool / MCP Capability Slots

- Web search.
- Browser/page reader.
- Source citation logger.
- Optional company database.
- Human approval tool.

## Workflow Steps

1. Validate that the niche definition is approved.
2. Identify market segments inside the niche.
3. Research common pain points and buying triggers.
4. Identify competitor categories and alternative solutions.
5. Identify terminology used by buyers in this market.
6. Identify account-level qualification signals.
7. Identify account-level disqualification signals.
8. Produce recommended account search queries.
9. Produce filtering criteria for the next workflow.
10. Stop for human review.

## Subtasks

- Collect at least 5 reliable sources for the market summary.
- Separate facts from assumptions.
- Mark every assumption with a confidence level.
- Prefer recent and authoritative sources.
- Record source URLs for every material claim.

## Evidence Requirements

Each market insight must include:

- Claim.
- Source URL.
- Source reliability level.
- Confidence level.
- Relevance to the ICP.

## Handoff Output

| Field | Required |
|---|---|
| Market summary | Yes |
| Priority segments | Yes |
| Buyer pains | Yes |
| Buying triggers | Yes |
| Competitor/alternative categories | Yes |
| Search terminology | Yes |
| Recommended account filters | Yes |
| Recommended disqualifiers | Yes |
| Search queries for account discovery | Yes |
| Source URLs | Yes |
| Confidence levels | Yes |
| Human review status | Yes |

## Compliance Rules

- Do not collect contact-level personal data in this workflow.
- Do not scrape behind logins.
- Do not use sources that violate platform terms.

## Human Review Gate

Stop after producing the market research handoff.

The human reviewer must approve:

- Priority segments.
- Buying triggers.
- Account filters.
- Disqualifiers.
- Any assumptions marked as important.

## Stop Conditions

Stop if:

- The niche definition is incomplete or unapproved.
- Sources are too weak to support filtering criteria.
- Market segments are too broad to produce a focused account list.
- Compliance constraints are unclear.

## Acceptance Criteria

- Research is specific enough to guide account filtering.
- Every important claim has a source URL.
- Filters and disqualifiers are clear.
- Human approval is recorded before account filtering starts.
