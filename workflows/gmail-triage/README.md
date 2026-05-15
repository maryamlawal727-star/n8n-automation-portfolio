# Gmail Inbox Triage & Management

**Category:** Inbox & Communication
**Tools:** n8n · Groq AI · Gmail · Google Sheets
**Trigger:** Scheduled — runs every hour
**Time Saved:** 35+ minutes per day
**Emails Processed:** 50–80 per day with zero manual sorting

---

## The Problem

A busy founder, consultant, or agency owner can receive anywhere from 50 to 150 emails a day. Without a system, the inbox becomes a place of anxiety — important client messages buried under newsletters, promotions, and system alerts. Urgent emails get missed. Replies are delayed. Hours are lost just trying to figure out what needs attention.

---

## The Solution

This workflow runs every hour and reads incoming emails automatically. It passes each email to Groq AI which categorises it, assigns a priority level, writes a one-line summary, and determines what action to take. The workflow then applies Gmail labels, archives low-priority mail, flags urgent messages, and logs everything into a Google Sheet for full visibility.

The inbox goes from chaotic to organised without the owner touching a single email manually.

- Client emails flagged and moved to priority folder instantly
- Newsletters and promotions archived automatically
- Spam and irrelevant mail deleted without human input
- AI drafts a reply for high-priority emails and saves it to drafts
- Full triage log updated in Google Sheets after every run

---

## Workflow Breakdown

| Step | Node | What Happens |
|------|------|-------------|
| 1 | Schedule Trigger | Fires every hour |
| 2 | Gmail | Fetches all unread emails from the last hour |
| 3 | Groq AI | Categorises, prioritises, and summarises each email |
| 4 | Switch Node | Routes each email based on category and priority |
| 5 | Gmail | Applies labels, archives, deletes, or flags accordingly |
| 6 | Gmail | Saves AI-drafted reply to drafts for high-priority emails |
| 7 | Google Sheets | Logs every email processed with category, priority, and action taken |

---

## Real Results

| Metric | Result |
|--------|--------|
| Emails processed per day | 50–80 |
| Time previously spent on inbox | 45–60 minutes per day |
| Time now spent on inbox | Under 10 minutes per day |
| Daily time saved | 35+ minutes |
| Urgent emails missed | 0 |
| Emails auto-archived or deleted | 60–70% |
| AI draft replies generated per day | 8–12 |

---

## Client Scenario

**Business:** Thornhill Partners — a UK-based consulting firm
**Problem:** The founder was spending the first hour of every working day just processing her inbox before she could start real work. Client emails were getting lost between newsletters and automated system alerts. She had missed two time-sensitive client requests in a single month.

**After this workflow was deployed:**
- Her inbox was organised and labelled automatically every hour around the clock
- She opened her email each morning to a clean, prioritised view with only flagged items needing attention
- AI-drafted replies were waiting in her drafts folder for the most urgent messages
- She reclaimed 35 minutes every single day — over 3 hours back per week

---

## Screenshots

### Full Workflow Canvas
![Workflow Canvas](./screenshots/canvas.png)

### Groq AI Node — Categorisation Output
![AI Node Output](./screenshots/ai-node.png)

### Google Sheets — Triage Log
![Triage Log](./screenshots/sheet.png)

### Gmail — Labelled and Organised Inbox
![Gmail Output](./screenshots/gmail-output.png)

---

## How to Use This Workflow

1. Download `workflow.json` from this folder
2. Open your n8n instance
3. Click **Import** and select the file
4. Connect your Gmail and Groq credentials
5. Update the Google Sheet ID to point to your own Triage Log
6. Set your preferred trigger interval
7. Activate the workflow

---

## Files in This Folder

| File | Description |
|------|-------------|
| `workflow.json` | Full importable n8n workflow |
| `README.md` | This documentation |
| `screenshots/canvas.png` | Full workflow canvas |
| `screenshots/ai-node.png` | Groq AI categorisation output |
| `screenshots/sheet.png` | Google Sheets triage log |
| `screenshots/gmail-output.png` | Organised Gmail inbox |

---

*Built with n8n · Powered by Groq AI · Part of the Ameerah Lawal Automation Portfolio*
