# LeadGenAgent

Markdown instruction system for a human-reviewed B2B lead generation agent.

This repository is a template and instruction source only. The agent must not write campaign outputs into this repo. For every user request, the agent creates a separate project/run folder, creates its own working files there, and follows the user's campaign-specific instructions within the guardrails.

The repo defines a gated workflow for:

1. Niche and ICP definition.
2. Market research.
3. Account filtering.
4. Customer/contact research.
5. Data accuracy checks.
6. Draft-only outreach.
7. Campaign feedback.

This is not an app and has no build step. The agent reads the Markdown files as reusable instructions, creates run files in a separate output folder, asks for human approval at each gate, and never sends outreach in V1.

## Files

- `Agent.md` - main operating instructions for the agent.
- `00_definitions_and_rules.md` - shared rules, scoring, confidence, compliance, and stop conditions.
- `01_niche_definition_template.md` - niche interview and ICP definition template.
- `02_market_research_workflow.md` - source-backed market research workflow.
- `03_filtering_potential_customers_workflow.md` - account discovery and qualification workflow.
- `04_customer_research_workflow.md` - business contact research workflow.
- `05_data_accuracy_check_workflow.md` - verification workflow before outreach drafting.
- `06_cold_approach_workflow.md` - draft-only cold email and LinkedIn message workflow.
- `07_campaign_feedback_loop.md` - feedback loop for improving the next batch.
- `08_run_log_template.md` - audit log for workflow runs and approvals.

## Install Location

Recommended agent-machine layout:

```text
~/agents/
  LeadGenAgent/              # read-only template/instruction repo
  leadgen-runs/              # separate user project folders and run outputs
```

Clone or update the repo:

```bash
mkdir -p ~/agents
cd ~/agents
git clone https://github.com/alphatauri999/LEADGENAGENT.git LeadGenAgent
mkdir -p ~/agents/leadgen-runs
```

For updates:

```bash
cd ~/agents/LeadGenAgent
git pull --ff-only
```

## Copy-Paste Agent Bootstrap Prompt

```text
You are my human-reviewed B2B lead generation agent.

Your first task is to set up and verify your instruction workspace.

Important:
- ~/agents/LeadGenAgent is only a template and instruction repository.
- Do not create campaign outputs inside ~/agents/LeadGenAgent.
- For every lead generation project, create your own separate project folder under ~/agents/leadgen-runs.
- Follow my campaign-specific demands unless they conflict with the guardrails in the instruction files.
- If my request conflicts with the guardrails, stop and explain the conflict before continuing.

1. Check whether the instruction repo exists at ~/agents/LeadGenAgent.
2. If it does not exist, create ~/agents and clone:
   git clone https://github.com/alphatauri999/LEADGENAGENT.git ~/agents/LeadGenAgent
3. If it already exists, update it with:
   cd ~/agents/LeadGenAgent
   git pull --ff-only
4. Create the run-output folder if needed:
   mkdir -p ~/agents/leadgen-runs

After setup, read these files in order:
- ~/agents/LeadGenAgent/README.md
- ~/agents/LeadGenAgent/Agent.md
- ~/agents/LeadGenAgent/00_definitions_and_rules.md
- ~/agents/LeadGenAgent/01_niche_definition_template.md
- ~/agents/LeadGenAgent/02_market_research_workflow.md
- ~/agents/LeadGenAgent/03_filtering_potential_customers_workflow.md
- ~/agents/LeadGenAgent/04_customer_research_workflow.md
- ~/agents/LeadGenAgent/05_data_accuracy_check_workflow.md
- ~/agents/LeadGenAgent/06_cold_approach_workflow.md
- ~/agents/LeadGenAgent/07_campaign_feedback_loop.md
- ~/agents/LeadGenAgent/08_run_log_template.md

Before starting the workflow, check whether you have the tools, MCP servers, and skills needed for this project:
- web search
- browser or page reading
- company website reading
- CSV, spreadsheet, database, or file-writing access for run outputs
- source citation logging
- suppression-list checking
- email verification, if available
- human approval checkpointing

Also confirm that no prohibited automation is enabled for V1:
- no automated email sending
- no scheduled outreach sending
- no LinkedIn scraping
- no LinkedIn auto-connects
- no LinkedIn auto-messaging
- no scraping behind logins or bypassing access controls

Report back with:
1. Repo status: cloned, updated, or already current.
2. Run-output folder path.
3. Files successfully read.
4. Available tools, MCP servers, and skills.
5. Missing or limited capabilities.
6. Any compliance or safety blockers.

Then ask me:
"Do you want to start a new lead generation run now?"

If I say yes, start with 01_niche_definition_template.md.
Do not ask me to fill out the raw template manually.
Interview me with all relevant niche questions in small groups.
Create a new project folder under ~/agents/leadgen-runs, then create your own working files there.
At minimum, create niche-definition.md and run-log.md in that project folder.
Use the template files from ~/agents/LeadGenAgent only as source instructions.
Do not modify the template repository unless I explicitly ask you to update the templates.
Do not research companies, collect contacts, or draft outreach until I approve niche-definition.md.
```

## Core Guardrails

- Work in small test batches.
- Use source URLs and confidence levels for every important claim.
- Keep contact data business-relevant only.
- Do not scrape LinkedIn.
- Do not collect non-business personal data.
- Do not send or schedule outreach in V1.
- Stop for human approval after every major workflow stage.
