# Antigravity 2.0 Interface & Feature Walkthrough
## Reliance Jio Agentic AI Orchestration Workshop

Welcome to your command desk! This guide provides a visual walkthrough of the **Antigravity 2.0** interface. Use the screenshot below to identify each component as you complete the checklist.

---

## 🖥️ Antigravity 2.0 Command Desk Mockup

![Antigravity 2.0 User Interface Mockup](/Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/assets/antigravity_ui.png)

---

## 🔍 Interface Component Breakdown

### 📂 Left Sidebar: File Explorer
* **What it is**: The file tree displaying your local workspace directory.
* **On the Screenshot**: Shows the [HR_Mission_Control](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control) directory structure. You can see the `data/employees.csv` spreadsheet and `policies/compensation_guidelines.md` file ready for auditing.
* **How to use it**: Use this sidebar to open data tables and verify that the agent is modifying files strictly inside the sandbox boundaries.

### 📝 Center Pane: Code/Markdown Editor
* **What it is**: The main work desk where files and plans are opened.
* **On the Screenshot**: Displays [implementation_plan.md](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/exercises/implementation_plan.md) with active checklists.
* **How to use it**: Before approving changes, the agent writes its plan here. Read the checklist items in this editor to confirm the agent's calculations follow Jio guidelines before signing off.

### 💬 Right Panel: AI Chat & Prompt Input
* **What it is**: Your main interaction panel to guide the agent using natural language.
* **On the Screenshot**: The chat thread shows your prompt at the bottom (*“Type a message...”*) and the agent's responses at the top.
* **How to use it**: Avoid micromanaging. Describe your final business goal and constraints here, and let the agent propose the steps.

### 🧠 Collapsible Log: Thought Process Reasoning
* **What it is**: A transparency pane inside the Chat Panel showing the agent's internal reasoning in real-time.
* **On the Screenshot**: Titled **Thought Process** on the right side. It reveals the calculations and path checks before any tool is run.
* **How to use it**: Expand this log to check that the agent is using correct formulas (e.g. compa-ratio calculations) before it touches database files.

### 🔒 Interactive Overlay: The Permission Gate
* **What it is**: A security pop-up card that intercepts agent requests to read/write directories or execute terminal scripts.
* **On the Screenshot**: A floating box in the lower-right quadrant titled **Permission Gate** with glowing green **Approve** and red **Reject** buttons.
* **How to use it**: Look at the path the agent wants to touch. If it stays inside the sandbox, click **Approve**. If the path is incorrect, click **Reject** and tell the agent what to correct.

### 💻 Bottom Panel: Terminal Console
* **What it is**: The engine room of the IDE.
* **On the Screenshot**: Displayed at the bottom, logging system events and Git save points.
* **How to use it**: You do not write commands here. Watch this log to verify that the agent is compiling reports or finalizing a Git commit snapshot.

---

## 🏃 Interface Sandbox Exercises
1. Expand the [data](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data) folder on the left.
2. Double-click [employees.csv](file:///Users/kavitha.nair/Library/CloudStorage/OneDrive-RelianceCorporateITParkLimited/Documents/04%20My%20Projects/Antigravity%202.0%20Training/HR_Mission_Control/data/employees.csv) to open it in the editor pane.
3. Paste this check-in prompt in the Prompt Bar:
   ```text
   Verify the files inside the HR_Mission_Control folder and read the guidelines in context.md.
   ```
4. Watch the collapsible **Thought Process** log expand and monitor the **Permission Gate** popup. Click **Approve** to let the agent read the workspace.
