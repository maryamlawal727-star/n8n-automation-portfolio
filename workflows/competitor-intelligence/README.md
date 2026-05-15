# Competitor Intelligence Monitor

**Category:** Intelligence & Research
**Tools:** n8n · Groq AI · Google Sheets · Telegram
**Trigger:** Scheduled — runs daily at 7:00 AM
**Time Saved:** 4+ hours per week
**Competitors Monitored:** Up to 10 simultaneously

---

## The Problem

Most small businesses have no idea what their competitors are doing until it is too late — a competitor drops their prices, launches a new service, or starts targeting the exact same audience, and the business owner finds out weeks later by accident.

Manual competitor research is exhausting and inconsistent. It gets deprioritised when things get busy, which is exactly when staying informed matters most.

---

## The Solution

This workflow runs every morning and visits each competitor's website automatically. It checks for changes — new pages, updated pricing, new services, new blog content, job listings — and passes everything it finds to Groq AI which writes a concise intelligence summary for each competitor.

If a significant change is detected, an alert is sent instantly to Telegram with the competitor name, what changed, what it means, and a recommended action. Everything is also logged in Google Sheets for a full historical record.

The business owner wakes up every morning already knowing what their competitors did yesterday.

---

## Workflow Breakdown

| Step | Node | What Happens |
|------|------|-------------|
| 1 | Schedule Trigger | Fires every day at 7:00 AM |
| 2 | Google Sheets | Pulls the list of competitors and their URLs to monitor |
| 3 | HTTP Request | Visits each competitor website and fetches page content |
| 4 | Groq AI | Analyses content for changes and writes an intelligence summary |
| 5 | IF Node | Checks if a significant change was detected |
| 6 | Telegram | Sends an instant alert with the summary and recommended action |
| 7 | Google Sheets | Logs the monitoring result, change detected, and alert status |

---

## Real Results

| Metric | Result |
|--------|--------|
| Competitors monitored simultaneously | 5–10 |
| Time previously spent on manual research | 4–6 hours per week |
| Time now spent on competitor research | 0 hours per week |
| Alerts received in first 30 days | 14 significant changes detected |
| Actionable insights acted on | Pricing adjustment, 2 content responses, 1 new service launch counter |
| Days of monitoring history logged | 30+ days from day one |

---

## Client Scenario

**Business:** Ironside Marketing — a Canadian digital marketing agency
**Problem:** The founder had no system for tracking what competitors were doing. She found out a direct competitor had launched a done-for-you service package — identical to hers — only when a prospect mentioned it during a sales call. By then the competitor had already been running it for three weeks.

**After this workflow was deployed:**
- Five competitors are monitored every single morning automatically
- She received a Telegram alert the same day a competitor dropped their prices
- She responded with a counteroffer campaign within 48 hours
- She now starts every working day with a full intelligence briefing delivered to her phone

---

## Screenshots

### Full Workflow Canvas
![Workflow Canvas](./screenshots/canvas.png)

### Groq AI Node — Intelligence Summary Output
![AI Node Output](./screenshots/ai-node.png)

### Google Sheets — Intelligence Log
![Intelligence Log](./screenshots/sheet.png)

### Telegram — Competitor Alert Message
![Telegram Alert](./screenshots/telegram-alert.png)

---

## How to Use This Workflow

1. Download `workflow.json` from this folder
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your Groq, Google Sheets, and Telegram credentials
5. Add your competitors and their URLs to the Google Sheet
6. Set your Telegram chat ID in the Telegram node
7. Activate the workflow

---

## Files in This Folder

| File | Description |
|------|-------------|
| `workflow.json` | Full importable n8n workflow |
| `README.md` | This documentation |
| `screenshots/canvas.png` | Full workflow canvas |
| `screenshots/ai-node.png` | Groq AI intelligence output |
| `screenshots/sheet.png` | Google Sheets intelligence log |
| `screenshots/telegram-alert.png` | Telegram competitor alert |

---

*Built with n8n · Powered by Groq AI · Part of the Ameerah Lawal Automation Portfolio*
