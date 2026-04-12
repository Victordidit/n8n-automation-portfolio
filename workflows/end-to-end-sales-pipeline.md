# 🎯 End-to-End Sales Pipeline

[**📂 View Workflow JSON**](./end-to-end-sales-pipeline.json)

### Overview
This workflow functions as an autonomous sales development representative. It instantly captures new lead data from form submissions, uses AI to perform a high-level qualification score (1-100), and then branches into two distinct strategies: immediate, high-touch outreach for "Hot" leads and an automated nurture sequence for "Cold" leads—ensuring every lead is logged to the CRM without manual entry.

---

## 🏗️ Workflow Structure

**Step 1**
📝 **On Form Submission** — Receives new lead data via form entry instantly.

**Step 2**
🤖 **OpenAI** — Scores the lead from 1-100 to categorize them as "Hot" or "Cold" based on intent.

**Step 3**
⚙️ **Code in JavaScript** — Cleans and structures the raw lead data for systematic processing.

**Step 4**
🔀 **IF** — Routes the workflow logic to separate paths for hot leads vs. cold leads.

**Step 5**
✅ **TRUE: OpenAI1** — Writes a highly personalized outreach email for the hot lead.

**Step 6**
✅ **TRUE: Code in JavaScript1** — Cleans and formats the hot lead email draft for professional delivery.

**Step 7**
✅ **TRUE: Gmail** — Sends the personalized outreach draft to the hot lead.

**Step 8**
✅ **TRUE: Gmail1** — Sends an urgent alert notification to the internal sales representative.

**Step 9**
✅ **TRUE: Code in JavaScript3** — Prepares the hot lead data for CRM entry.

**Step 10**
✅ **TRUE: Google Sheets** — Logs the hot lead into the CRM as a high-priority entry.

**Step 11**
❌ **FALSE: OpenAI2** — Writes a value-driven nurture email for the cold lead.

**Step 12**
❌ **FALSE: Code in JavaScript2** — Cleans and formats the cold lead nurture email.

**Step 13**
❌ **FALSE: Gmail2** — Sends the nurture sequence draft to the cold lead.

**Step 14**
❌ **FALSE: Code in JavaScript4** — Prepares the cold lead data for CRM entry.

**Step 15**
❌ **FALSE: Google Sheets1** — Logs the cold lead into the CRM for long-term tracking.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript / Form Trigger
* **CRM/Sales:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
