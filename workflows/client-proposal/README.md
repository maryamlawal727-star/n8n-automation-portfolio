# Client Proposal Automation

**Category:** Client Management
**Tools:** n8n · Groq AI · Notion · Gmail
**Trigger:** Webhook — fires instantly when the intake form is submitted
**Time Saved:** 2 hours per proposal
**Proposal Generation Time:** Under 60 seconds

---

## The Problem

Writing proposals is one of the most time-consuming parts of running a service business. Every prospect needs a tailored document — their name, their problem, a customised solution, pricing, and a compelling reason to say yes. Done manually, one proposal can take two to three hours. Done poorly, it loses the deal.

Most service providers are either sending generic proposals that do not convert or spending half their working week writing documents instead of delivering work.

---

## The Solution

This workflow triggers the moment a prospect submits an intake form. It reads their name, business type, industry, and the problem they described — then passes all of that to Groq AI, which writes a complete, tailored proposal in under 60 seconds.

The proposal is saved automatically to a Notion database and sent to the prospect via Gmail — all without the service provider lifting a finger.

Every proposal is personalised. Every proposal goes out fast. No more losing deals because a competitor responded first.

---

## Workflow Breakdown

| Step | Node | What Happens |
|------|------|-------------|
| 1 | Webhook | Receives intake form submission instantly |
| 2 | Set Node | Extracts and formats prospect data |
| 3 | Groq AI | Generates a full tailored proposal based on the prospect's inputs |
| 4 | Notion | Saves the proposal to the Proposals database with status set to Sent |
| 5 | Gmail | Sends the proposal email to the prospect automatically |

---

## Real Results

| Metric | Result |
|--------|--------|
| Time to generate one proposal manually | 2–3 hours |
| Time to generate one proposal with this workflow | Under 60 seconds |
| Proposals sent in first 30 days | 15 |
| Time saved in first 30 days | 30+ hours |
| Proposal acceptance rate | 67% |
| Average proposal value | £2,100 – £4,400 |

---

## Client Scenario

**Business:** Launchpad Ventures — a UK-based startup advisory firm
**Problem:** The founder was spending two to three hours writing each proposal manually. By the time it was sent, the prospect had already spoken to two other providers. She was losing deals not on quality but on speed.

**After this workflow was deployed:**
- Every new inquiry triggered an automatic proposal within 60 seconds of form submission
- The proposal was personalised to the prospect's exact industry and problem statement
- She became the first provider in the prospect's inbox — every single time
- In the first month, she closed three deals that she attributes directly to response speed

---

## Screenshots

### Full Workflow Canvas
![Workflow Canvas](<img width="1917" height="825" alt="client proposals (1)" src="https://github.com/user-attachments/assets/2e1549a0-9f55-4d36-8944-7f935ef9e324" />)

### Notion or Google Sheet — Proposals Database
![Notion Database](<img width="1919" height="838" alt="client proposals (3)" src="https://github.com/user-attachments/assets/e3447e91-343b-4516-becc-458a5daf74a2" />)

### Gmail or Google Drive  — Auto-Sent Proposal Email
![Email Output](<img width="1908" height="839" alt="client proposals (2)" src="https://github.com/user-attachments/assets/c8ae20df-dc18-415c-bdd4-66ddccb86632" />)  <img width="1134" height="639" alt="client proposal" src="https://github.com/user-attachments/assets/eb67580b-9c90-40f6-806d-8b3bd5134f39" />


---

## How to Use This Workflow

1. Download `workflow.json` from this folder
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your Groq, Notion, and Gmail credentials
5. Update the Notion database ID to point to your own Proposals database
6. Set up your intake form to post to the webhook URL
7. Activate the workflow

---

## Files in This Folder

| File | Description |
|------|-------------|
| `workflow.json` | Full importable n8n workflow |
| `README.md` | This documentation |
| `screenshots/canvas.png` | Full workflow canvas |
| `screenshots/ai-node.png` | Groq AI proposal output |
| `screenshots/notion-output.png` | Notion proposals database |
| `screenshots/email-output.png` | Auto-sent proposal email |

---

*Built with n8n · Powered by Groq AI · Part of the Ameerah Lawal Automation Portfolio*
