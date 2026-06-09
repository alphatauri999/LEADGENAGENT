# Agent Usage Instructions

Use this project as a reusable instruction system for a human-reviewed B2B lead generation workflow. This is not a software app and does not require code execution. This repository is a template and instruction source only.

For every user campaign, create a separate project folder for working files and outputs. Do not write campaign-specific files into this instruction repository unless the human reviewer explicitly asks you to update the templates.

## Operating Principles

- Read `00_definitions_and_rules.md` before starting any workflow.
- Work in the file order defined below.
- Treat this repository as reusable source instructions, not as the campaign workspace.
- Create your own working files in the configured project/run folder.
- Follow the user's campaign-specific demands unless they conflict with the global guardrails or stop conditions.
- Do not ask the human reviewer to fill out raw templates. Interview the reviewer with clear questions, then create the completed output file yourself.
- Store completed run files in the configured run-output folder, not in the instruction repository.
- Use small test batches only: 10-25 accounts and 1-3 contacts per approved account.
- Do not skip human review gates.
- Do not send, schedule, auto-connect, auto-message, or automate outreach.
- Do not scrape LinkedIn, scrape behind logins, bypass access controls, or violate platform terms.
- Do not collect non-business personal data.
- Every claim, account, contact, and personalization point must include a source URL and confidence level.
- If data quality, compliance, or source reliability is unclear, stop and ask for human review.

## Required Workflow Order

1. `01_niche_definition_template.md`
   - Interview the human reviewer for all relevant niche, ICP, offer, exclusion, compliance, source, suppression-list, and success-criteria details.
   - Ask concise grouped questions instead of handing over a blank form.
   - Create a completed `niche-definition.md` file in the current run folder.
   - Summarize assumptions and any fields marked `unknown`, `not available`, or `needs review`.
   - Stop for human approval before continuing.

2. `02_market_research_workflow.md`
   - Research market segments, pains, buying triggers, competitors, terminology, filters, and disqualifiers.
   - Stop for human approval before account filtering.

3. `03_filtering_potential_customers_workflow.md`
   - Build and score a small account list.
   - Check disqualifiers, duplicates, and suppression-list conflicts.
   - Stop for human approval before customer research.

4. `04_customer_research_workflow.md`
   - Find business-relevant contacts for approved accounts.
   - Prefer company websites and authoritative public business sources.
   - Treat LinkedIn as optional and last-resort; do not open LinkedIn profiles unless the human reviewer approves that lookup.
   - Stop for human approval before the data accuracy check.

5. `05_data_accuracy_check_workflow.md`
   - Verify name, position, company match, email status, source quality, duplicates, suppression status, and compliance status.
   - Block inaccurate, risky, unverifiable, duplicate, suppressed, or low-confidence records.
   - Stop for human approval before outreach drafting.

6. `06_cold_approach_workflow.md`
   - Produce draft-only outreach messages.
   - Include subject lines, first email, follow-ups, optional LinkedIn notes, personalization evidence, source URLs, and compliance checklist status.
   - Stop for human approval. Do not send outreach.

7. `07_campaign_feedback_loop.md`
   - Capture outcomes, objections, bad fits, bounces, wrong contacts, positive signals, and reviewer feedback.
   - Recommend updates to ICP, scoring, disqualifiers, source quality, and messaging.
   - Stop for human approval before the next batch.

8. `08_run_log_template.md`
   - Maintain the run log throughout the process.
   - Record stage status, reviewer decisions, rejected records, suppression updates, data-quality issues, and final signoff.

## Tool And MCP Usage

Use available tools by capability, not by brand. Before each workflow, identify which tools or MCP servers are available for:

- Web search.
- Browser or page reading.
- Company website reading.
- Company database or CRM access.
- Spreadsheet or database writing.
- Email verification.
- Source citation logging.
- Suppression-list checking.
- Human approval.
- Optional deliverability checking.

If a required capability is unavailable, continue only if the workflow can still meet the acceptance criteria. Otherwise stop and explain the missing capability.

## Human Review Gates

At every review gate, present the human reviewer with:

- Workflow completed.
- Inputs used.
- Output table or summary.
- Source URLs.
- Confidence levels.
- Rejected or blocked records.
- Compliance concerns.
- Recommended next action.

The reviewer must choose one:

- Approved.
- Approved with edits.
- Needs revision.
- Rejected.

Do not continue to the next workflow until approval is recorded in `08_run_log_template.md`.

## Niche Interview Requirements

At the start of a new run, create or confirm the run folder before asking niche questions. Use this pattern unless the human reviewer gives another location:

```text
~/agents/leadgen-runs/<campaign-name-or-draft>/batch-001/
```

Then run an interview to complete `01_niche_definition_template.md`. Ask for the minimum needed to produce a complete niche file, but cover every required area:

- Campaign name, target niche, industry, geography, company size, and company type.
- Ideal account description, poor-fit account description, hard disqualifiers, and required exclusions.
- Target buyer roles, secondary buyer roles, included titles, excluded titles, budget owner, problem owner, and decision influencers.
- Pain points, buying triggers, urgency signals, and public evidence that can be researched.
- Offer, proof points, case studies, differentiators, competitors, and alternatives.
- Preferred source types, restricted source types, allowed tools, and unavailable tools.
- Compliance constraints, suppression-list location, data that must not be collected, and outreach restrictions.
- Batch size, contacts per account, approval owner, and success criteria.

Ask questions in small groups of 5-8 at a time. If the reviewer gives partial answers, continue with follow-up questions only for missing or ambiguous fields. If a field is not applicable, write `not applicable` and explain why in the completed niche file.

After the interview, create:

- `niche-definition.md` from `01_niche_definition_template.md`.
- `run-log.md` from `08_run_log_template.md`.

Do not start `02_market_research_workflow.md` until the reviewer explicitly approves the completed niche definition.

## Data Quality Rules

- Prefer company-owned sources over third-party sources.
- Search snippets are discovery signals, not final proof unless corroborated.
- Inferred emails must be marked unverified until checked.
- Reject personal emails, invalid emails, risky emails, disposable emails, and unverifiable emails.
- Mark conflicting or outdated data as `needs review`.
- Do not guess missing names, positions, emails, or company matches.

## Output Requirements

Every workflow output must include:

- Batch ID.
- Source file or workflow name.
- Date.
- Source URLs.
- Confidence levels.
- Compliance status.
- Human review status.
- Next action.

Use tables where the workflow template defines a table schema. Keep narrative summaries short and source-backed.

## Stop Conditions

Stop immediately if:

- The current workflow input is missing or unapproved.
- A human review gate has not been completed.
- Compliance status is unclear.
- Required source URLs are missing.
- Suppression-list status is unavailable before outreach drafting.
- Data is mostly low-confidence, inferred, conflicting, or unverifiable.
- The task would require scraping LinkedIn, bypassing logins, or automating outreach.

## Success Criteria

A successful run produces:

- A completed and approved niche definition.
- Source-backed market research.
- A reviewed account list with fit scores.
- A reviewed contact list with business-relevant data only.
- A completed data accuracy check.
- Draft-only outreach messages.
- A run log with approvals and rejected records.
- Feedback that improves the next batch.
