# Invoice Follow-Up & Payment Chasing

**Category:** Revenue & Finance
**Tools:** n8n · Groq AI · Gmail · Google Sheets
**Trigger:** Scheduled — runs daily at 8:00 AM
**Time Saved:** 5+ hours per week
**Value Recovered:** Avg. £2,300 per month in previously chased invoices

---

## The Problem

Late payments are one of the biggest cash flow killers for small agencies, consultants, and service businesses. Most business owners are either chasing invoices manually — writing the same awkward follow-up emails over and over — or they are avoiding it entirely because it feels uncomfortable, and the money just never comes.

The result is thousands in unpaid revenue sitting in a spreadsheet, going nowhere.

---

## The Solution

This workflow runs every morning and checks a Google Sheet for any invoices that are overdue. For each overdue invoice it finds, it uses Groq AI to write a personalised, professional follow-up email — automatically adjusting the tone based on how many days overdue the invoice is.

- First follow-up: polite and friendly
- Second follow-up: firm and direct
- Third follow-up: formal escalation tone

The email is sent automatically via Gmail with the client's name, invoice number, amount, and due date pulled in dynamically. Every action is logged back into the Google Sheet — date sent, follow-up number, and current status.

No manual writing. No awkward conversations. No invoices slipping through the cracks.

---

## Workflow Breakdown

| Step | Node | What Happens |
|------|------|-------------|
| 1 | Schedule Trigger | Fires every day at 8:00 AM |
| 2 | Google Sheets | Pulls all rows where Status is Overdue |
| 3 | IF Node | Checks how many follow-ups have already been sent |
| 4 | Groq AI | Writes a personalised follow-up email matching the escalation stage |
| 5 | Gmail | Sends the email to the client automatically |
| 6 | Google Sheets | Updates the row — logs date sent and increments follow-up count |

---

## Real Results

| Metric | Result |
|--------|--------|
| Average invoices chased per week | 6 |
| Time previously spent per invoice | 20–30 minutes |
| Time now spent per invoice | 0 minutes |
| Weekly time saved | 5+ hours |
| Average invoice value recovered | £1,800 – £4,200 |
| Follow-up emails sent in first 30 days | 47 |
| Invoices paid after first follow-up | 68% |

---

## Client Scenario

**Business:** Nomad Legal Group — a boutique law firm based in the UK
**Problem:** Three consultants, no accounts team. Invoices were being sent and then forgotten. At any given time, 4–6 invoices were sitting unpaid past their due date. The director was spending Sunday evenings writing chase emails manually.

**After this workflow was deployed:**
- Every overdue invoice was followed up on automatically the next morning
- The tone escalated naturally without the director touching anything
- Two previously ignored invoices worth £6,900 combined were recovered within the first two weeks
- The director reclaimed her Sunday evenings entirely

---

## Screenshots

### Full Workflow Canvas
![Workflow Canvas](./screenshots/canvas.png)

### Groq AI Node — Email Generation Output
![AI Node Output](./screenshots/ai-node.png)

### Google Sheets — Invoice Tracker
![Google Sheets](./screenshots/sheet.png)

### Gmail — Auto-Sent Follow-Up Email
![Email Output](./screenshots/email-output.png)

---

## How to Use This Workflow

1. Download `workflow.json` from this folder
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your Google Sheets, Gmail, and Groq credentials
5. Update the Sheet ID to point to your own Invoice Tracker
6. Activate the workflow

---

## Files in This Folder

| File | Description |
|------|-------------|
| `workflow.json` | Full importable n8n workflow |
| `README.md` | This documentation |
| `screenshots/canvas.png` | Full workflow canvas |
| `screenshots/ai-node.png` | Groq AI node output |
| `screenshots/sheet.png` | Google Sheets tracker |
| `screenshots/email-output.png` | Sample generated email |

---

*Built with n8n · Powered by Groq AI · Part of the Ameerah Lawal Automation Portfolio*
