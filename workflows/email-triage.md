# 📧 Email Triage & Auto-Response

[**📂 View Workflow JSON**](./email-triage.json)

### Overview
This workflow acts as an intelligent gatekeeper for your inbox. It monitors incoming emails, uses AI to categorize them (Support, Sales, Spam, or Urgent), and either drafts a response or routes the data to the appropriate department.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Gmail Trigger** — Watches for new emails in real-time.

**Step 2**
🤖 **OpenAI** — Analyzes the email body to determine intent and sentiment.

**Step 3**
⚙️ **Code in JavaScript** — Extracts the sender's details and cleans the AI's category label.

**Step 4**
🔀 **IF** — Routes the workflow based on the category (e.g., "Support" goes to one path, "Sales" to another).

**Step 5**
📧 **Gmail (Reply)** — Automatically creates a draft reply based on the AI’s suggested response.

**Step 6**
📊 **Google Sheets** — Logs the transaction and category for weekly reporting.

---

### 🛠️ Tech Stack
*   **Automation:** n8n
*   **AI:** OpenAI (GPT-4)
*   **Communication:** Gmail API
*   **Tracking:** Google Sheets

---
*Developed by **Victordidit** | Design + Autonomy*
