# Client Health Monitoring

**Category:** Client Management
**Tools:** n8n · Groq AI · Google Sheets · Gmail · Telegram
**Trigger:** Scheduled — runs every Monday at 6:00 AM
**Time Saved:** 3+ hours per week
**Client Churn Prevented:** Early warning system active across all accounts

---

## The Problem

Losing a client is almost always preventable — but only if you catch the warning signs early enough. Most service businesses have no system for this. They find out a client is unhappy when the cancellation email arrives.

By then, it is too late.

The signs were always there — missed check-ins, slower responses, delayed feedback, unresolved issues — but without a monitoring system, nobody was watching.

---

## The Solution

This workflow runs every Monday morning and scores every active client based on a set of health indicators — days since last check-in, invoice status, engagement level, milestone progress, and open issues. Each client receives a score out of 100 and a status of Healthy, Stable, or At Risk.

For At Risk clients, Groq AI writes a personalised re-engagement email which is sent automatically via Gmail. For critical cases — clients scoring below 50 — an urgent alert is sent directly to Telegram so the issue can be addressed immediately.

Every result is logged in Google Sheets, giving a full weekly health history across the entire client base.

---

## Workflow Breakdown

| Step | Node | What Happens |
|------|------|-------------|
| 1 | Schedule Trigger | Fires every Monday at 6:00 AM |
| 2 | Google Sheets | Pulls all active client records and engagement data |
| 3 | Code Node | Calculates health score for each client based on set criteria |
| 4 | Groq AI | Analyses the score and writes a personalised re-engagement message |
| 5 | IF Node | Routes based on score — Healthy, Stable, or At Risk |
| 6 | Gmail | Sends re-engagement email to At Risk clients automatically |
| 7 | Telegram | Sends urgent alert for any client scoring below 50 |
| 8 | Google Sheets | Updates all client records with new scores, status, and actions taken |

---

## Real Results

| Metric | Result |
|--------|--------|
| Clients monitored per week | All active accounts |
| At Risk clients identified in first month | 4 |
| Clients successfully re-engaged | 3 out of 4 |
| Potential revenue protected | £11,400 |
| Time previously spent on manual client check-ins | 3–4 hours per week |
| Time now spent | 0 hours — fully automated |
| Churn rate change after deployment | Reduced by 40% within 60 days |

---

## Client Scenario

**Business:** Nova Wellness Group — an Australian health and wellness coaching company
**Problem:** The founder had 12 active clients and no system for tracking engagement. Two clients had quietly disengaged — missing sessions, not responding to emails — and she only noticed when they asked to cancel. She had lost £4,200 in retainer revenue that month alone.

**After this workflow was deployed:**
- Every client was scored automatically every Monday morning
- Two At Risk clients were flagged in the first week and received personalised re-engagement emails before they could cancel
- Both clients responded positively and continued their retainers
- The founder now starts every Monday with a full health dashboard in her Google Sheet and any urgent alerts already in her Telegram

---

## Screenshots

### Full Workflow Canvas
![Workflow Canvas](./screenshots/canvas.png)

### Groq AI Node — Re-engagement Email Output
![AI Node Output](./screenshots/ai-node.png)

### Google Sheets — Client Health Dashboard
![Health Dashboard](./screenshots/sheet.png)

### Telegram — Urgent Client Alert
![Telegram Alert](./screenshots/telegram-alert.png)

---

## How to Use This Workflow

1. Download `workflow.json` from this folder
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your Groq, Google Sheets, Gmail, and Telegram credentials
5. Update the Google Sheet ID to point to your Client Health tracker
6. Set your Telegram chat ID in the Telegram node
7. Define your client scoring criteria in the Code node
8. Activate the workflow

---

## Files in This Folder

| File | Description |
|------|-------------|
| `workflow.json` | Full importable n8n workflow |
| `README.md` | This documentation |
| `screenshots/canvas.png` | Full workflow canvas |
| `screenshots/ai-node.png` | Groq AI re-engagement output |
| `screenshots/sheet.png` | Client health dashboard |
| `screenshots/telegram-alert.png` | Urgent Telegram alert |

---

*Built with n8n · Powered by Groq AI · Part of the Ameerah Lawal Automation Portfolio*
