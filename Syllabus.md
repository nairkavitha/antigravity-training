# Reliance Jio Agentic AI Upskilling Workshop
## 5-Day (Day 0-4) Syllabus & Hands-on Sandbox Exercises

This folder contains the local sandbox `HR_Mission_Control` for the training program. Below is the syllabus schedule and instructions for each day.

---

## Daily Schedule

### Day 0: Welcome to the Command Deck (IDE & Agent Basics)
- **Goal**: Understand what an IDE and an AI Agent are, why they are used together, differentiate key context files, and run a basic check-in with the agent.
- **Analogy**: The "Integrated Command Desk" (IDE) where everything is within arm's reach, and the "Digital Intern" (AI Agent) who works at the desk under your supervision.
- **Key Context Files**:
  - 📄 `README.md` (The Welcome Sign): Explains the project folder structure.
  - 📄 `context.md` (The Standing Brief): Company policies and guidelines.
  - 📄 `implementation_plan.md` (The Project Proposal): Plan drafted by the agent for human sign-off.
  - 📄 `task.md` (The Whiteboard): Live progress tracking checklist (`[ ]` / `[/]` / `[x]`).
  - 📄 `handover.md` (The Shift Report): Transition summary when changing tasks.
- **Exercise**: Open the IDE, locate and read [README.md](HR_Mission_Control/README.md), open the interactive [glossary.html](glossary.html) in your browser to study the terms, and send a welcome prompt in the Chat Panel asking the agent to list the files inside `HR_Mission_Control/data/`.


### Day 1: Delegating Goals vs. Giving Orders (The Mindset Shift)
- **Goal**: Move from telling the agent *how* to do a task to telling it *what* you want to achieve.
- **Analogy**: The "Digital Intern" who handles the details. You review their "Project Proposal" (`implementation_plan.md`) before signing off.
- **Exercise**: Create an onboarding structure under `HR_Mission_Control/onboarding` for a new employee named *Rohan Verma*. Ask the agent to plan folders for 'contracts', 'benefits', and 'compliance', modify it via feedback, and then approve.

### Day 2: Navigating the Workspace and Tool Understanding (The Office Setup)
- **Goal**: Learn how the agent uses file and search tools, and how to grant permissions safely.
- **Analogy**: Giving the intern the office cabinet keys. **MCP (Model Context Protocol)** acts as their temporary gate pass.
- **Exercise**: Ask the agent to analyze the current compensation database (`data/employees.csv`) and compare employee salaries against the `market_rates.csv` bands to flag anyone underpaid.

### Day 3: Agentic Orchestration and Subagents (The Department Structure)
- **Goal**: Coordinate multiple subagents to solve complex tasks concurrently.
- **Analogy**: The HR Manager coordinating specialist team members (Comp, Equity, L&D).
- **Exercise**: Deploy two specialized subagents—a "Gender Pay Equity Auditor" and a "Market Positioning Analyst"—to analyze different aspects of the employee database and merge their findings.

### Day 4: Building the Pay Review Tool (Capstone Project)
- **Goal**: Build and run an end-to-end annual pay review workflow.
- **Analogy**: The Annual Review Committee.
- **Exercise**: Prompt the agent to run the pay review for FY 2026-27 by combining data, market benchmarks, and guidelines in `policies/compensation_guidelines.md`. It must generate a final CSV report and draft individual compensation adjustment letters under `letters/` using the template.

---

## Safe-to-Fail Troubleshooting Cheat Sheet

1. **Agent Gets Lost (Path Disorientation)**: If the agent reports it cannot find files, type:
   > *"Look only inside the folder: /Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04 My Projects/Antigravity 2.0 Training/HR_Mission_Control"*
2. **Permission Blocked**: If a tool fails due to permissions, prompt:
   > *"I rejected that tool run because the path was incorrect. Please target `HR_Mission_Control/data/pay_review_results.csv` and try again."*
3. **Infinite Loop**: If the agent gets stuck in a loop:
   > *"Pause and tell me what constraint or rule in the guidelines is preventing you from completing the calculations."* Override or adjust the guidelines accordingly.

---

## Success Criteria & Transition Metrics
- **Objective Delegation**: Prompts describe the final outcome rather than step-by-step instructions.
- **HITL Checkpoints**: The HR professional reviews and signs off on plans before letting the agent write files.
- **Data Security**: Auditing all proposed tool calls for potential PII leakage.
- **Orchestration**: Successfully managing subagents to compile aggregated analyses.
