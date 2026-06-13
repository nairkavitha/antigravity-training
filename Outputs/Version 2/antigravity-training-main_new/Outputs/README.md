# Antigravity 2.0 Training & Upskilling Programme

A single-file interactive training portal for upskilling HR professionals in Agentic AI Orchestration at Reliance Jio, built around Google Antigravity 2.0 (the standalone desktop app announced at Google I/O 2026).

---

## 📁 Folder Structure

```
Outputs/
├── index.html              # The training portal, open this in a browser
├── HR_Mission_Control/     # Synthetic sandbox for hands-on exercises
│   ├── data/               # employees.csv, market_rates.csv
│   ├── policies/           # Compensation, leave & remote-work policies
│   ├── templates/          # Compensation letter template
│   ├── context.md          # Standing brief for the agent (team convention)
│   └── handover.md         # Session handover log (team convention)
├── README.md               # This file
└── archived/               # Older standalone files and planning docs
```

---

## 🚀 Getting Started

Open `index.html` in any modern browser. No server or installation needed for the portal itself. Learners will need Antigravity 2.0 installed (antigravity.google/download) for the hands-on exercises.

The portal is self-paced (about 3 hours 20 minutes of guided content) and has 7 tabs:

1. **Home**: programme overview, learning objectives, how to use the portal
2. **Module 1 · Foundations**: chatbots vs agents, the Plan → Act → Verify loop, briefing files vs artifacts, data governance, knowledge check
3. **Module 2 · Setup & Tour**: installation, creating your Project (Step 0), the Antigravity 2.0 interface, your first prompt, knowledge check
4. **Module 3 · Core Skills**: goals vs orders, tools & MCP, subagent orchestration, plus two fullscreen interactives: the **Context Engineering Lab** (brief the same agent six ways, watch the ending change) and the **HR Tool Stack Simulator** (toggle the five layers of a working tool)
5. **Module 4 · Build**: five project options, from guided builds to the governed pay-review capstone (Option E), knowledge check
6. **Module 5 · Help**: the five common failure patterns and how to recover, the HITL commitment
7. **Glossary**: 50+ flip-card terms with corporate-life analogies, searchable and filterable by category

---

## ✨ Built-in Extras

- **📝 Field Notes**: a floating notes drawer on every page. Notes are tagged to the module you're reading, saved automatically in your browser, and export as a formatted PDF (via your browser's Save as PDF) or Markdown.
- **🎓 Facilitator mode**: open the portal as `index.html?facilitator=1` and a floating Facilitator tab appears on the left edge. It opens a panel with timings, talk tracks, common stumbles and the Context Lab demo script for whichever module is on screen, and follows you as you switch tabs. Same file, two products.

---

## 🗂 Sandbox Data

All exercises use synthetic data in `HR_Mission_Control/`. No real employee PII is included. Do not connect to production systems (Workday, SAP, HRMS) without explicit approval.
