# HR Mission Control · Local Sandbox

Welcome to the **HR Mission Control** sandbox: your safe-to-fail environment for practising **Agentic AI Orchestration** with **Antigravity 2.0**, alongside the training portal (`../index.html`).

You will not write code here. You will work like a director: delegating business goals to your agent, reviewing its plans, and auditing its output.

## Directory Structure

- 📁 `data/`
  - 📄 `employees.csv`: 10 synthetic employee records, names, roles, grades, performance ratings, salaries, emails.
  - 📄 `market_rates.csv`: market salary bands (min / midpoint / max) for Grades 1–4, in INR.
- 📁 `policies/`
  - 📄 `compensation_guidelines.md`: budget caps, the performance increase grid, market-correction and over-market rules, and the three human sign-off checkpoints.
  - 📄 `leave_and_encashment_policy.md`: leave entitlements and encashment rules. *(Its review date has passed, deliberately. One of your exercises will find it.)*
  - 📄 `remote_work_policy.md`: hybrid working rules.
- 📁 `templates/`
  - 📄 `compensation_letter_template.md`: the annual compensation letter, used in the Build capstone.
- 📄 `context.md`: the **standing brief**, our team convention. Rules the agent must follow on every task. Reference it in prompts: *"follow the rules in context.md"*.
- 📄 `handover.md`: the **session handover log**, our team convention for continuity between sessions.
- 📁 `exercises/` *(created during the training)*: every output you and the agent produce lands here.

## How to Connect This Sandbox (do this first)

Antigravity 2.0 is **Project-centric**: the agent can only see folders you add to a Project.

1. Open Antigravity 2.0 → **Select Project → New Project**
2. **Add Folder** → choose this `HR_Mission_Control` folder → **Create**
3. Keep **review-before-execute** ON in the project security settings
4. **Start first conversation**, you're live

## The Core Agentic Workflow

1. **Goal**: describe the outcome you want (not the steps).
2. **Plan review**: the agent writes an **Implementation Plan** artifact, read it in the **Auxiliary Pane**, comment if needed, then click **Proceed**.
3. **Execution**: watch the **Task Plan** artifact tick off steps live; approve permission prompts after reading the paths.
4. **Audit**: read the **Walkthrough** artifact, then verify the output files against the source data before using anything.

## House Rules

- Synthetic data only, never paste real employee data into any agent.
- Outputs go to `exercises/`. Nothing leaves this folder.
- Every number in a deliverable must be traceable to a file here. When in doubt, audit.
