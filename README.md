# n8n-rss-to-sheets-automation
Automated content curation pipeline built with n8n - continuously monitors a Medium RSS feed and archives new articles into Google Sheets, eliminating manual tracking.
<div align="center">

# 📰 Reading List Automation

### *Turning a RSS feed into a self-updating archive — zero manual effort.*

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![Automation](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

</div>

## Overview

Manually checking a favorite publication for new posts is a small task 
that quietly wastes time. This workflow removes it entirely — it listens 
for new Medium articles the moment they're published, extracts what 
matters, and archives it into a growing spreadsheet automatically.

> **No manual checking. No copy-pasting. Just a living reading list.**
> 
## How It Works

<div align="center">

┌──────────────────┐      ┌──────────────────┐      ┌──────────────────────┐
│  RSS Feed Trigger │ ───▶ │   Edit Fields     │ ───▶ │  Google Sheets        │
│  listens for new  │      │  extracts title,  │      │  appends new row      │
│  articles          │      │  link & date      │      │  to the archive       │
└──────────────────┘      └──────────────────┘      └──────────────────────┘
```

</div>

| Stage | Node | Role |
|:---:|---|---|
| 🎯 | **RSS Feed Trigger** | Polls the Medium feed on a fixed interval |
| 🧹 | **Edit Fields** | Cleans the payload → `title`, `link`, `date` |
| 💾 | **Google Sheets** | Appends a new row — the archive builds itself |

## In Action

<div align="center">

**The complete pipeline, verified end-to-end**
<img src="screenshots/workflow.png" width="700"/>

<br/>

**Articles landing automatically in the sheet**
<img src="screenshots/sheets-result.png" width="500"/>

</div>

## Stack

- **n8n** — visual workflow orchestration
- **Google Sheets API** — lightweight, human-readable storage
- **RSS/Atom** — the content source protocol

## 🚀 Getting Started

```bash
1. Import workflow.json into your n8n instance
   → "..." menu → Import from File
2. Set the RSS Feed Trigger's Feed URL
3. Connect your Google account → pick a target spreadsheet
4. Activate → new articles start flowing in automatically
```

## 💡 Why This Matters

This is a small project, but it demonstrates a pattern used everywhere 
in real automation systems: **trigger → transform → persist**. The same 
three-step logic scales to notifications, data pipelines, CRM syncs, 
and beyond — RSS is just the friendliest place to start.

<div align="center">

*Built while exploring workflow automation with n8n* 🛠️

</div>
