# Antigravity 2.0 Feature Upskilling: 5-Day Detailed Lesson Plan
## Reliance Jio Agentic AI Orchestration Program (HR Upskilling Hub)

This document provides a detailed, step-by-step facilitator guide and lesson plan focused on training HR professionals to navigate and harness the core features of **Antigravity 2.0**. This curriculum moves learners away from "chatting with AI" and guides them toward **Agentic AI Orchestration** in a safe-to-fail, Jio-governed sandbox environment.

---

## 🗺️ Curriculum Overview & Feature Mapping

| Day | Module Title | Core Antigravity 2.0 Features Covered | Reference Materials & Sandbox Files |
| :--- | :--- | :--- | :--- |
| **Day 0** | **Welcome to the Command Desk** | The Integrated Command Desk (IDE), Workspace File Structure, Prompting, Basic Tool Calls, Interactive Glossary | [Syllabus.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/Syllabus.md)<br>[HR_Mission_Control/README.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/README.md)<br>[glossary.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/glossary.html) |
| **Day 1** | **Delegating Goals vs. Orders** | Objective-Based Delegation, Planning Mode, `implementation_plan.md` Checkpoint, Human-in-the-Loop (HITL) Revision | [Detailed Training Content.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/Detailed%20Training%20Content.html#L922-L932) |
| **Day 2** | **Navigating the Workspace & Tools** | Model Context Protocol (MCP), File Viewing/Editing Tools, Permissions Gates, Data Auditing, PII Security | [HR_Mission_Control/data/employees.csv](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data/employees.csv)<br>[HR_Mission_Control/data/market_rates.csv](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data/market_rates.csv) |
| **Day 3** | **Agentic Orchestration & Subagents** | Multi-Agent Spawning, Subagent Lifecycles, Thought Process Auditing, Reconciling Conflicts, Task Logs (`task.md`) | [Detailed Training Content.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/Detailed%20Training%20Content.html#L943-L951) |
| **Day 4** | **Annual Pay Review (Capstone)** | Governed Execution Loop, Policy Guardrails, Multi-Stage Checkpoints, Git Repository Commit, `handover.md` | [HR_Mission_Control/policies/compensation_guidelines.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/policies/compensation_guidelines.md)<br>[HR_Mission_Control/templates/compensation_letter_template.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/templates/compensation_letter_template.md) |

---

## 🌌 Core Antigravity 2.0 Feature Breakdown

Before delivering the daily lessons, facilitators must familiarize themselves with the underlying capabilities of **Antigravity 2.0**:
1. **Integrated Command Desk (IDE)**: Merges the File Explorer (left), Code/Document Editor (center), Browser (internal view), and AI Chat/Prompt Panel (right) into a single workspace. This eliminates tool clutter.
2. **Planning Mode (`implementation_plan.md`)**: The agent does not execute file changes or runs immediately. It must first write a proposal specifying the actions, modified paths, and validation checks. It pauses for human approval.
3. **Task Tracking (`task.md`)**: A living checklist written in standard markdown. The agent lists sub-tasks and uses visual indicators (`[ ]` for pending, `[/]` for in-progress, `[x]` for completed) to show live execution progress.
4. **Model Context Protocol (MCP)**: The protocol enabling the agent to communicate with local tools (reading files, listing directories, writing modifications) through secure API channels.
5. **Human-in-the-Loop (HITL) Gating**: A strict authorization prompt displayed to the user in the Chat Panel before the agent executes code, reads sensitive CSV directories, or makes modifications outside the current workspace.
6. **Subagent Orchestration**: The ability of the primary agent to define, spawn, and direct specialized subagents to tackle concurrent or isolated aspects of a problem.
7. **Thought Process Transparency**: A collapsible reasoning trace visible in the Chat Panel that logs the agent's calculations, path explorations, and internal decision-making in real-time.
8. **Sandbox Boundary Enforcement**: Workspace constraints that prevent the agent from reading or writing paths outside the authorized local project directory, guarding against accidental data leaks.

---

## 📅 Day-by-Day Lesson Plans

---

### 📅 Day 0: Welcome to the Command Desk (IDE & Agent Basics)
**Duration**: 150 Minutes (2.5 Hours)
**Focus Features**: Integrated Command Desk (IDE), Workspace Navigation, Prompting, Basic Tool Calls, Glossary

#### 🎯 Learning Objectives
* Define an Integrated Development Environment (IDE) as a "Command Desk" and identify its primary panels.
* Explain the difference between a conversational chatbot and a tool-capable AI agent.
* Locate and identify the five core context files in a workspace directory.
* Run a setup verification prompt and inspect the agent's tool-calling outputs.

#### 💡 Conceptual Metaphors
* **The Integrated Command Desk**: *Instead of having your file drawers in one room, your typewriter in another, and your mail courier outside, the Command Desk puts your files (File Explorer), your policies (Editor), and your assistant (AI Chat Panel) at arm's reach in a single workstation.*
* **Chatbot (Advisor) vs. Agent (Expert Contractor)**: *A chatbot is a consultant on the phone; you ask for advice, and they tell you how to write a letter. An agent is a contractor sitting at your desk; you give them the target, they open the folder, fetch the template, write the letter, and present it for your signature.*

#### 🗣️ Facilitator Script (Segment 1 — The Big Reframe)
> *"Welcome to the Antigravity 2.0 Upskilling Workshop. Over the next five days, you are not learning how to write code. You are learning how to direct. Your agent is your Expert Contractor—highly capable, extremely fast, but operating with zero institutional knowledge and zero judgment. It will do exactly what you tell it to do, not what you meant. If a human colleague spots a weird salary calculation, they stop and ask. The agent won't. It will calculate a mathematically flawless, completely incorrect number, write it beautifully into a PDF, and wait for your signature. That is why you are in the loop. Your sign-off is the only safeguard in the chain."*

#### 💻 Live Demonstration
1. Open the IDE and project workspace.
2. Point out the **File Explorer** (left), the **Document Editor** (center), and the **Chat Panel** (right).
3. Open [README.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/README.md) inside the editor. Show how it documents the sandbox directory.
4. Open the [glossary.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/glossary.html) file in a browser tab. Flip a few flashcards (e.g., "IDE", "AI Agent") to demonstrate the non-technical analogies.

#### 🏃 Hands-On Exercises
* **Step 1: Workspace Initial Check-In**
  Instruct all participants to click on the Chat Panel Prompt Bar and enter the following prompt:
  ```text
  List the files inside HR_Mission_Control/data/
  ```
  *Watch the agent invoke a file-listing tool. Have participants look at the tool execution output in the chat history.*
* **Step 2: Value Demonstration Prompt**
  Instruct participants to copy and paste the following onboarding task into the prompt bar:
  ```text
  We've just hired Rohan Verma as a new HR Business Partner. List the documents he'll need for onboarding, organised by category. Refer to our readme if needed.
  ```
  *Observe the agent outputting a structured document list.*
* **Step 3: Glossary Deep Dive**
  Have participants open [glossary.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/glossary.html) in their browsers and review at least five cards in the "basics" category.

#### ⚠️ Misconceptions & Stumbling Blocks
* **Stumble**: Participants try to click and move files manually in the Finder/Explorer when the agent fails to find something.
* **Correction**: Teach them to tell the agent where the file is. If the agent gets path-disoriented, prompt: *"Look only inside the folder: HR_Mission_Control/data/"*.
* **Stumble**: Fear of clicking the wrong button and altering critical files.
* **Correction**: Reassure them that the `HR_Mission_Control` sandbox is a "safe-to-fail" local folder backed by Git. We can restore any file instantly.

---

### 📅 Day 1: Delegating Goals vs. Giving Orders (The Mindset Shift)
**Duration**: 120 Minutes (2 Hours)
**Focus Features**: Objective-Based Delegation, Planning Mode, Implementation Plans (`implementation_plan.md`)

#### 🎯 Learning Objectives
* Differentiate between procedural prompts (micro-managing) and declarative prompts (objective delegation).
* Audit an agent-proposed `implementation_plan.md` for logical correctness.
* Provide corrective feedback to the plan and authorize execution.

#### 💡 Conceptual Metaphors
* **The Project Proposal Gate**: *If you hire a contractor to renovate your office, you don't hand them a hammer and tell them where to swing. You tell them you need a conference room with ten chairs. They draw up a blueprint (Implementation Plan) and show it to you. You point out changes on the blueprint, they adjust it, and only when you sign off do they start hammering.*

#### 🗣️ Facilitator Script (The Mindset Shift)
> *"Most people fail with AI because they try to micro-manage it. They write prompts like 'Open column B, copy the third row, create a folder named X.' This is giving orders. It's slow, and it wastes the agent's analytical capabilities. Instead, we delegate the goal: 'Set up an onboarding structure for Rohan Verma with folders for compliance, benefits, and contracts.' Let the contractor figure out the folder tree and show you their blueprint first. If the blueprint is wrong, edit the blueprint, not the wood."*

#### 💻 Live Demonstration
1. Show the contrast between two prompts on screen:
   * **Micro-managing (Bad)**: *"Create a folder named Rohan. Under it, make a contracts folder. Then make a benefits folder."*
   * **Delegation (Good)**: *"Set up an onboarding folder structure for our new hire Rohan Verma, with places for his contracts, benefits, and compliance documents. Show me your plan before creating anything."*
2. Input the delegation prompt in the Chat Panel.
3. Show how the agent halts execution and writes an `implementation_plan.md` file in the workspace. Open it to show the proposed directory structure.

#### 🏃 Hands-On Exercises
* **Step 1: Propose Onboarding Folders**
  Instruct participants to enter the good delegation prompt above.
* **Step 2: The Revision Gate**
  Once the agent generates `implementation_plan.md`, instruct participants **NOT** to approve it yet. They must review it and enter a revision request:
  ```text
  Good start, but compliance documents must go BEFORE benefits, and add a subfolder for his signed offer letter. Update the plan and show me again.
  ```
* **Step 3: Execution Authorization**
  Once the agent updates the plan, read the proposal in [Detailed Training Content.html](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/Detailed%20Training%20Content.html#L922-L932) and prompt:
  ```text
  The plan looks correct. Proceed with the implementation.
  ```
  *Watch the agent create the directory tree under `HR_Mission_Control/exercises/`.*

#### ⚠️ Misconceptions & Stumbling Blocks
* **Stumble**: Learners click "Approve" instantly without looking at `implementation_plan.md`.
* **Correction**: Pause the class. Ask a learner who approved instantly: *"What folders did the agent just propose to create? You signed the contract without reading it. If this was production compensation data, you might have just approved deleting the database."*
* **Stumble**: Trying to write the plan themselves.
* **Correction**: Remind them that the agent writes the plan; the human's job is review, critique, and approval.

---

### 📅 Day 2: Navigating the Workspace & Tool Auditing
**Duration**: 120 Minutes (2 Hours)
**Focus Features**: Model Context Protocol (MCP), File-Read/Write Tools, Permission gates, PII Redaction

#### 🎯 Learning Objectives
* Explain how the Model Context Protocol (MCP) governs agent interactions with databases.
* Audit tool execution logs for potential PII (Personally Identifiable Information) leakage.
* Conduct a basic compensation competitiveness analysis using sandbox data files.

#### 💡 Conceptual Metaphors
* **The Intern's Cabinet Keys**: *MCP is like issuing a key card to your intern. Each time they want to open a filing cabinet (read a CSV) or run a script, they have to tap their card, and a light flashes on your desk. You can check which drawer they are opening and click a button to let them in. They never get free reign over the entire building.*

#### 🗣️ Facilitator Script (Security and Auditing)
> *"Today we look at data. When we analyze employee compensation, we are dealing with PII—emails, grades, salaries. Antigravity 2.0 has tools to open these files directly, but it cannot do so secretly. Under Jio's data governance policies, we must ensure sensitive data stays within the local sandbox. Every tool call the agent makes will ask for your permission. Look at the paths: is it reading `data/employees.csv`? Good. Is it trying to access your personal desktop or download an external script? Deny it. You are the security gate."*

#### 💻 Live Demonstration
1. Open [HR_Mission_Control/data/employees.csv](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data/employees.csv) and [HR_Mission_Control/data/market_rates.csv](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data/market_rates.csv) in the editor.
2. Explain the **Compa-Ratio** formula:
   $$\text{Compa-Ratio} = \frac{\text{Current Salary}}{\text{Market Midpoint}}$$
   *Show how an employee's Grade (1-4) maps to the min/mid/max values in the market rates table.*
3. Run a basic check prompt to show the permission dialog that pops up.

#### 🏃 Hands-On Exercises
* **Step 1: Competitiveness Analysis**
  Instruct participants to delegate the salary gap audit:
  ```text
  Analyse our current compensation in employees.csv against the market bands in market_rates.csv. Flag anyone whose salary sits below the market minimum for their grade, and show me the list with their compa-ratio. Don't change any files — just report.
  ```
* **Step 2: Permitting Tool Calls**
  When the agent requests permission to read `employees.csv` and `market_rates.csv`, have participants inspect the target path and click **Approve**.
* **Step 3: Verification of Output**
  Have participants pick one flagged employee (e.g., *Aarav Sharma*) and calculate their compa-ratio manually to cross-check the agent's math.
  * *Formula validation: Salary / Grade Midpoint.*

#### ⚠️ Misconceptions & Stumbling Blocks
* **Stumble**: The agent asks to install a library or run an external script, and the user gets a CLI permission block.
* **Correction**: Instruct participants to deny the tool and prompt the agent: *"Do not use external scripts or commands. Perform the calculations using local file reads and standard operations only."*

---

### 📅 Day 3: Agentic Orchestration & Subagents
**Duration**: 120 Minutes (2 Hours)
**Focus Features**: Subagent Spawning, Thought Process Logs, Task Tracking (`task.md`), Reconciling Conflicts

#### 🎯 Learning Objectives
* Spawn and configure specialized subagents for parallel analysis tasks.
* Interpret the Thought Process trace to audit the agent's logic.
* Identify logic loops or blocks and apply recovery prompts.

#### 💡 Conceptual Metaphors
* **The HR Department Manager**: *Instead of trying to do everything yourself, you sit at the director's desk. You hire one specialist auditor to review gender pay equity and another analyst to check market positioning. They go to their desks (subagents), run their calculations, and send you their findings. You merge them into the final board report.*

#### 🗣️ Facilitator Script (Orchestration & Reasoning)
> *"As tasks grow complex, a single conversation gets cluttered. The agent's memory gets full, and it starts making mistakes. Antigravity 2.0 solves this with Subagents. You can delegate specialized sub-tasks to separate agent instances that run in the background. While they work, you can watch their 'Thought Process' live. This isn't just cool technology; it's an audit trail. You can see their reasoning step-by-step. If they start going in circles, you can tap them on the shoulder and steer them back."*

#### 💻 Live Demonstration
1. Input a multi-agent orchestration prompt in the chat panel.
2. Expand the **Thought Process** log in the chat UI. Show how the agent documents its intent: *"I will now invoke a subagent to calculate gender pay distribution..."*
3. Show how the subagent session runs in a separate context, keeping the main thread clean.

#### 🏃 Hands-On Exercises
* **Step 1: Multi-Agent Analysis Brief**
  Instruct participants to copy and paste the following orchestration brief:
  ```text
  Deploy two specialist subagents to analyse employees.csv:
    1) a "Gender Pay Equity Auditor" — compare pay of men vs women within the same grade and role, and surface any gaps.
    2) a "Market Positioning Analyst" — compare everyone to their grade market midpoint and group them as below / on / above market.
  Then merge both findings into one summary report under exercises/.
  ```
* **Step 2: Auditing the Thought Process**
  Have participants watch the subagents spin up. Tell them to expand the thought logs and identify which file each subagent is reading.
* **Step 3: Tracking with `task.md`**
  Open the auto-updated `task.md` in the editor. Point out how the checkboxes update live as the subagents finish their analysis.

#### ⚠️ Misconceptions & Stumbling Blocks
* **Stumble**: A subagent gets stuck in an infinite loop because it cannot resolve a role name mismatch.
* **Correction**: Teach the **Recovery Prompt**. Type in the chat: *"Pause and tell me what constraint or mismatch is preventing you from completing the pay gaps calculation."* Once the agent explains, instruct it: *"Treat 'HR Associate' and 'HR Business Partner' as separate roles. Resume calculations."*

---

### 📅 Day 4: Building the Pay Review Tool (Capstone Project)
**Duration**: 150 Minutes (2.5 Hours)
**Focus Features**: Multi-Stage Checkpoint Flow, Policy Guardrails, Repository Commit, `handover.md`

#### 🎯 Learning Objectives
* Execute a multi-stage annual pay review workflow compliant with corporate guidelines.
* Implement complex policy constraints (rating grids, market corrections, and budget caps).
* Generate formatted CSV reports and personalized letters.
* Create a Git repository commit checkpoint to finalize and lock the session work.

#### 💡 Conceptual Metaphors
* **The Annual Review Committee**: *Today is graduation. You are the chairperson of the Review Committee. The agent is your analyst. It will draft the raises and letters according to the company handbook (policy). You will review the numbers at three separate checkpoints, apply budget caps, and then lock the filing cabinet (commit) to submit the results to payroll.*

#### 🗣️ Facilitator Script (The Capstone Challenge)
> *"Today, you combine everything. You will run Jio's annual pay review for FY 2026-27. The rules are strict, and they are located in `policies/compensation_guidelines.md`. There is a performance rating grid, a market correction rule, and a hard 8% department budget cap. You will not write the numbers. You will direct the agent to apply the guidelines, stop at the review checkpoints, confirm the math, generate the letters, and then commit the workspace to Git to save your work. Let's begin."*

#### 💻 Live Demonstration
1. Open [HR_Mission_Control/policies/compensation_guidelines.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/policies/compensation_guidelines.md) and point out the rules:
   * **Rule 1**: Market correction first. If pay is below grade min and rating is $\ge$ Meets, lift to grade min or apply 10% increase (whichever is lower) *before* performance raises.
   * **Rule 2**: Performance rating grid (Outstanding = 12-15%, Exceeds = 8-10%, Meets = 4-6%, Needs Improvement = 0%).
   * **Rule 3**: Over-market cap. If pay is above grade max, cap total raise at 3%.
   * **Rule 4**: Total raise pool budget must not exceed 8% of current payroll.
2. Open [HR_Mission_Control/templates/compensation_letter_template.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/templates/compensation_letter_template.md) to show the template fields.

#### 🏃 Hands-On Exercises (The Capstone Work)
* **Step 1: Briefing the Capstone**
  Instruct all participants to delegate the capstone workflow:
  ```text
  Run the FY 2026-27 pay review for everyone in employees.csv. Follow compensation_guidelines.md exactly — apply market corrections, the performance grid, the over-market cap, and keep the total within the 8% budget cap. Show me your plan and the calculations for sign-off BEFORE writing anything. Then generate pay_review_results.csv and draft individual letters under letters/ using the template.
  ```
* **Step 2: HITL Checkpoint 1 (Plan & Logic Verification)**
  Have participants review the agent's plan. They must verify that the agent plans to apply market corrections *before* performance increases.
* **Step 3: HITL Checkpoint 2 (Math & Budget Audit)**
  When the calculations are complete, the agent will present the totals. Participants must check:
  * *Is the total percentage increase under 8.0%?*
  * *Are individuals below market minimum corrected?*
  Have them type: *"The calculations look correct. Proceed to generate the CSV and letters."*
* **Step 4: HITL Checkpoint 3 (Quality & Tone Audit)**
  Once the letters are drafted in the `letters/` directory, participants must open one letter (e.g., `letters/rohan_verma_letter.md`) and verify the name, rating, and new salary figures.
* **Step 5: Lock the Workspace (Git Commit)**
  Instruct participants to finalize their work by running standard Git commands inside the terminal (or prompts) to commit:
  ```bash
  git add .
  git commit -m "Finalized FY 2026-27 HR Pay Review Sandbox Work"
  ```
  *(Or direct the agent to save the work point: "Commit the finalized pay review work to repository history.")*

#### ⚠️ Misconceptions & Stumbling Blocks
* **Stumble**: The agent runs over budget (e.g., total increase calculates to 8.2%) and stalls.
* **Correction**: Tell participants to prompt the agent to adjust: *"We are over budget. Trim the raise percentage of the 'Meets Expectations' group down by 0.5% to fit within the 8% budget cap, recalculate, and show me the plan again."*

---

## 🔒 Data Governance & Security Standards
As facilitators, you must enforce Jio's security protocols throughout the workshop:
1. **Zero External Copy-Pasting**: Never copy real employee data or database contents into external, public AI chats (e.g., public Web Gemini, ChatGPT). All operations must occur within the **Antigravity 2.0 Local Sandbox**.
2. **Path Auditing**: Always read the paths of proposed file modifications before clicking approve. If an agent tries to modify a system directory, deny the permission immediately.
3. **PII Handling**: Ensure email addresses, employee IDs, and raw phone numbers are redacted or excluded from final public-facing summaries.

---

## 💬 Participant Debrief Questions
At the end of each day, gather the class for a 10-minute debrief:
* *"If the agent delivers a beautiful, error-free salary report to your screen tomorrow, what is the very first thing you do before sending it to your VP?"* (Answer: Audit it against the source CSV to ensure no hallucination occurred).
* *"How does Planning Mode protect us from making mistakes compared to direct prompt execution?"* (Answer: It lets us correct logic errors on paper before folders or data files are modified).
* *"What is the main benefit of spawning subagents for complex tasks?"* (Answer: It breaks down cognitive load and keeps the main conversation context clean).
