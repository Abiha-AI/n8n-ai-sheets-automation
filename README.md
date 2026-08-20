# No-Code AI Automation with n8n

A simple yet powerful n8n workflow that automates AI-powered data processing using Google Sheets and Google's Generative Language API (Gemini) — all without writing a single line of code.

---

## Workflow Overview

| Trigger | Action | AI Processing | Output |
|---------|--------|---------------|--------|
| Google Sheets (New Row) | HTTP Request to Gemini API | Edit Fields (Manual Mapping) | Update Row in Sheet |

---

## Tech Stack

- **n8n** — Visual workflow automation
- **Google Sheets** — Data input & output
- **Google Gemini API** — AI text generation via HTTP Request
- **Edit Fields Node** — Data transformation & mapping

---

## How It Works

1. **Trigger**: A new row is added to Google Sheets → workflow starts automatically
2. **AI Request**: The row data is sent via HTTP POST to `generativelang.googleapis.com` (Gemini API)
3. **Process Response**: The `Edit Fields` node extracts and formats the AI response
4. **Write Back**: The processed result is updated back into the same Google Sheet row

---

## Workflow Preview

![Workflow Screenshot](./assets/workflow-screenshot.png)

---

## ⚙️ Setup Instructions

1. **Import the workflow**: In n8n, go to *Workflows → Import from File* → select `no-code-ai-automation.json`
2. **Add credentials**:
   - Google Sheets (OAuth2)
   - Google Gemini API Key
3. **Configure the sheet ID** in the trigger and update nodes
4. **Activate** the workflow

---

## Security Notes

- All API keys are managed via n8n's built-in **Credential Manager**
- No secrets are hardcoded in the workflow JSON
- Credentials are excluded from version control by design

---

## Use Cases

- Auto-generate product descriptions from raw data
- AI-powered content categorization
- Smart data enrichment & validation
- Automated report summarization

---

## 📄 License

MIT — Feel free to use and modify for your own projects.

---

&gt; Built with 💚 during my internship using [n8n](https://n8n.io)
