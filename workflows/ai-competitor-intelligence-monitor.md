# 🔍 AI Competitor Intelligence Monitor

[**📂 View Workflow JSON**](./ai-competitor-intelligence-monitor.json)

### Overview
This workflow functions as an automated market analyst. It scrapes competitor websites weekly to detect shifts in pricing, new feature rollouts, or changes in brand positioning. Using AI to compare current data against historical records, it ensures your team is the first to know about market changes through automated alerts and comprehensive intelligence logs.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every Monday at 8am to start the week with fresh market insights.

**Step 2**
🌐 **HTTP Request** — Scrapes target pages (e.g., Zapier’s pricing page) for live data.

**Step 3**
⚙️ **Extract Key Info** — Custom logic to extract specific features, prices, and marketing copy from the raw HTML.

**Step 4**
🤖 **OpenAI** — Analyzes the extracted data to identify changes in positioning or pricing strategy.

**Step 5**
⚙️ **CleanUp** — Cleans and structures the AI analysis into a professional, readable format.

**Step 6**
🔀 **IF** — Evaluates whether the detected changes constitute an "Urgent" competitive threat.

**Step 7**
✅ **TRUE: Gmail** — Sends an urgent competitor alert draft to the leadership team.

**Step 8**
✅ **TRUE: Code in JavaScript** — Prepares the critical update data for historical tracking.

**Step 9**
✅ **TRUE: Google Sheets** — Logs the intelligence report into the high-priority database.

**Step 10**
❌ **FALSE: Gmail1** — Sends a standard weekly intelligence summary for routine review.

**Step 11**
❌ **FALSE: Code in JavaScript1** — Prepares the standard intelligence data for logging.

**Step 12**
❌ **FALSE: Google Sheets1** — Logs the intelligence report into the standard database.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript / Web Scraping
* **Market Intel:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
