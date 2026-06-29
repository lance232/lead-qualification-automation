# AI Lead Qualification Automation

An AI-powered lead qualification workflow built with n8n and Groq that automatically analyzes inbound sales leads, scores purchase intent, stores qualified leads in Google Sheets, and routes follow-up actions based on AI-generated decisions.

---

## Features

- Accepts lead submissions through a webhook endpoint
- Normalizes incoming lead information
- Uses Groq Llama 3.3 to analyze purchase intent
- Assigns:
  - Lead Score (0–100)
  - Purchase Intent
  - Priority
  - Recommended Action
- Stores all leads in Google Sheets
- Automatically notifies the sales team for qualified leads
- Sends confirmation emails for lower-priority inquiries

---

## Workflow

Webhook
→ Normalize Lead Data
→ AI Lead Qualification
→ Structured Output
→ Google Sheets
→ Decision Logic
→ Email Notifications

---

## Tech Stack

- n8n
- Groq API
- Llama 3.3 70B
- Google Sheets API
- Gmail API
- Webhooks

---

## Sample AI Output

```json
{
  "intent": "High",
  "lead_score": 85,
  "priority": "Hot",
  "action": "SALES_CONTACT",
  "summary": "High purchase intent from an Operations Manager requesting a product demonstration."
}