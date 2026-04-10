# 🧾 Invoice & Payment Follow-Up

[**📂 View Workflow JSON**](./invoice-payment-follow-up.json)

### Overview
This workflow serves as an automated accounts receivable assistant. It scans for unpaid invoices daily, determines the severity of the delay, and uses AI to draft escalating follow-up emails—ensuring a professional but firm approach to payment collection while keeping internal records updated.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every day at 9am to check for outstanding payments.

**Step 2**
📊 **Google Sheets** — Reads all currently unpaid invoices from the tracking sheet.

**Step 3**
⚙️ **Code in JavaScript** — Calculates precisely how many days each invoice is overdue and assigns an urgency level.

**Step 4**
🤖 **OpenAI** — Writes a personalized follow-up email tailored to the specific urgency level (from polite reminder to firm notice).

**Step 5**
⚙️ **Code in JavaScript1** — Cleans and structures the AI-generated text for professional email formatting.

**Step 6**
📧 **Gmail** — Creates a follow-up draft for each client, ready for a final human review.

**Step 7**
⚙️ **Code in JavaScript2** — Prepares the data required to update the internal tracking system.

**Step 8**
📊 **Google Sheets1** — Updates the "Last Follow Up" date column to prevent duplicate messaging.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript
* **Management:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
