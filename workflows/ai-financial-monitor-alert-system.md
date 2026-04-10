# 💰 AI Financial Monitor & Alert System

[**📂 View Workflow JSON**](./ai-financial-monitor-alert-system.json)

### Overview
This workflow acts as an automated financial auditor. It reviews daily transactions to identify spending patterns, flag duplicate charges, and detect anomalies. Using AI, it generates a comprehensive financial health report and prioritizes communication by sending urgent alerts for suspicious activity while maintaining a routine logging system.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every day at 7am to analyze the previous day's financial activity.

**Step 2**
📊 **Google Sheets** — Reads all transaction data from the primary financial ledger.

**Step 3**
⚙️ **Analyze Spending** — Custom logic that calculates totals and identifies statistical anomalies or duplicates.

**Step 4**
🤖 **OpenAI** — Writes a professional financial health report based on the analyzed data trends.

**Step 5**
⚙️ **CleanUp** — Cleans and structures the AI report output for clear presentation.

**Step 6**
🔀 **IF** — Evaluates whether any high-priority anomalies were detected during the analysis.

**Step 7**
✅ **TRUE: Gmail** — Sends an urgent financial alert draft to the user regarding the detected anomalies.

**Step 8**
✅ **TRUE: Code in JavaScript** — Prepares the specific anomaly data for historical logging.

**Step 9**
✅ **TRUE: Google Sheets1** — Logs the high-priority report into the master Reports tab.

**Step 10**
❌ **FALSE: Gmail1** — Sends a standard daily/weekly summary draft when no issues are found.

**Step 11**
❌ **FALSE: Code in JavaScript1** — Prepares the standard summary data for logging.

**Step 12**
❌ **FALSE: Google Sheets2** — Logs the routine report into the master Reports tab.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript
* **Finance Ops:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
