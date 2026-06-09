# Niche Definition Template

Complete this template before running any lead generation workflow. The agent must not ask the human reviewer to fill out this raw template manually. The agent must interview the reviewer, ask all relevant questions, and create a completed niche-definition file in the run-output folder.

## Objective

Define the specific B2B niche, ICP, offer, boundaries, and success criteria for the lead generation run.

## Required Inputs

| Field | Value |
|---|---|
| Campaign name |  |
| Niche / market |  |
| Industry |  |
| Geography |  |
| Company size |  |
| Company type |  |
| Target buyer roles |  |
| Secondary buyer roles |  |
| Pain points |  |
| Buying triggers |  |
| Offer |  |
| Proof points |  |
| Competitors or alternatives |  |
| Required exclusions |  |
| Hard disqualifiers |  |
| Preferred source types |  |
| Restricted source types |  |
| Compliance constraints |  |
| Suppression list location |  |
| Success criteria |  |

## Agent Interview Procedure

Before completing the table, the agent must ask the reviewer concise questions that cover every required input. Ask in small groups of 5-8 questions at a time, then follow up only on missing or ambiguous answers.

The agent must ask about:

- Campaign name and where the run output should be stored.
- Target niche, industry, geography, company size, and company type.
- Ideal account characteristics and poor-fit account characteristics.
- Target buyer roles, secondary buyer roles, titles to include, and titles to exclude.
- The business pain, buying triggers, urgency signals, and public evidence that can be researched.
- The offer, proof points, differentiators, competitors, and alternatives.
- Required exclusions, hard disqualifiers, suppression-list location, and compliance constraints.
- Preferred source types, restricted source types, available tools, and unavailable tools.
- Batch size, contacts per account, approval owner, and success criteria.

If the reviewer does not know an answer, the agent should either:

- Propose a conservative default and ask for approval.
- Mark the field as `unknown`, `not available`, `not applicable`, or `needs review`.
- Stop if the missing field blocks safe execution.

After the interview, the agent must create a completed file named:

```text
niche-definition.md
```

Save it in the active run folder, for example:

```text
~/agents/leadgen-runs/<campaign-name>/batch-001/niche-definition.md
```

Do not edit `01_niche_definition_template.md` during a campaign run.

## ICP Detail

Describe the ideal account:

- What does the company do?
- Who do they serve?
- Why would they need this offer?
- What public signals suggest timing or need?
- What makes an account a poor fit?

Describe the ideal contact:

- Which role owns the problem?
- Which role controls budget?
- Which role influences the decision?
- Which titles should be included?
- Which titles should be excluded?

## Tool / MCP Capability Slots

Declare available tools before execution:

| Capability | Available Tool Or MCP Server | Notes |
|---|---|---|
| Web search |  |  |
| Browser/page reader |  |  |
| Company database |  |  |
| CRM or spreadsheet/database |  |  |
| Email verification |  |  |
| Source citation logger |  |  |
| Suppression-list checker |  |  |
| Human approval tool |  |  |
| Optional deliverability checker |  |  |

## Quality Rules

- The niche must be specific enough to generate account search queries.
- The ICP must include both qualification and disqualification criteria.
- The offer must be clear enough to produce relevant outreach angles.
- Compliance boundaries must be explicit before collecting contact data.
- The suppression list must be available before outreach drafting.

## Human Review Gate

Stop after completing this template.

Present the completed `niche-definition.md` to the reviewer and ask for one of these decisions:

- `Approved`
- `Approved with edits: [specific edits]`
- `Needs revision: [what to change]`
- `Rejected: [reason]`

Reviewer decision:

| Decision | Reviewer | Date | Notes |
|---|---|---|---|
|  |  |  |  |

The next workflow may start only after the niche definition is approved.

## Acceptance Criteria

- All required fields are complete.
- Buyer roles and disqualifiers are unambiguous.
- The source strategy is clear.
- Compliance and suppression-list requirements are documented.
- Human approval is recorded.
