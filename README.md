# LeadGenAgent

Reusable Markdown instructions for a human-reviewed B2B lead generation agent.

This repository is not a working software project. It is a set of agent-ready templates for running a careful lead generation workflow from niche definition through market research, account filtering, customer research, data accuracy checks, outreach drafting, and campaign feedback.

## Workflow

1. Define the niche and ICP.
2. Research the market.
3. Filter potential customer accounts.
4. Research business-relevant contacts.
5. Check data accuracy.
6. Draft cold outreach.
7. Capture feedback and improve the next batch.

Each major stage requires human approval before the next stage starts. V1 is designed for small test batches, not automated high-volume outreach.

## Files

- `00_definitions_and_rules.md` - shared glossary, scoring rules, compliance rules, and global guardrails.
- `01_niche_definition_template.md` - required setup template for the campaign niche and ICP.
- `02_market_research_workflow.md` - source-backed market research workflow.
- `03_filtering_potential_customers_workflow.md` - account discovery and qualification workflow.
- `04_customer_research_workflow.md` - business contact research workflow.
- `05_data_accuracy_check_workflow.md` - verification workflow before outreach drafting.
- `06_cold_approach_workflow.md` - draft-only email and LinkedIn outreach workflow.
- `07_campaign_feedback_loop.md` - learning loop for improving future batches.
- `08_run_log_template.md` - audit log for workflow runs and approvals.

## Guardrails

- No automated sending in V1.
- No LinkedIn scraping, bots, auto-connects, or auto-messages.
- No scraping behind logins or bypassing access controls.
- No non-business personal data collection.
- Every lead/contact must include source URLs, confidence level, compliance status, and a human review decision.

## Intended Use

Start with `01_niche_definition_template.md`, then run each workflow in order. Use `08_run_log_template.md` to record approvals, rejected records, and lessons learned during testing.
