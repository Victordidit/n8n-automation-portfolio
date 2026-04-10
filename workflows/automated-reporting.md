# 📊 Automated Reporting Dashboard

[**📂 View Workflow JSON**](./reporting.json)

### Overview
This workflow pulls lead data from Google Sheets, calculates key stats using custom logic, and leverages AI to write a professional financial/performance report delivered directly to your Gmail drafts every Monday.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every Monday at 8am.

**Step 2**
📊 **Google Sheets** — Pulls all leads data from the master database.

**Step 3**
⚙️ **Code in JavaScript** — Calculates stats, averages, and performance metrics.

**Step 4**
🤖 **OpenAI** — Writes a professional report summary based on the calculated stats.

**Step 5**
⚙️ **Code in JavaScript1** — Cleans and structures the AI report output for formatting.

**Step 6**
📧 **Gmail** — Delivers the final report as a Gmail draft for review.

---

### 🛠️ Tech Stack
*   **Automation:** n8n
*   **AI:** OpenAI (GPT-4)
*   **Data Handling:** JavaScript
*   **Storage/Comm:** Google Sheets & Gmail

---
*Developed by **Victordidit** | Design + Autonomy*
