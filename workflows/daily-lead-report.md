# 📊 Daily Lead Generation Report

[**📂 View Workflow JSON**](./daily-lead-report.json)

### Overview
Checking spreadsheets manually for performance updates breaks focus and wastes time. This automation ensures high-level insights find you, not the other way around. By aggregating data from multiple sources, calculating key performance indicators (KPIs), and delivering a structured summary to Slack, this workflow provides a "CEO-level" view of your lead engine every single day.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **TRIGGER (Schedule)** — Runs automatically every night at 9:00 PM to compile the day's performance.

**Step 2**
📊 **Get LEAD GEN SHEET & GET UNSUBSCRIBE** — Parallel nodes that fetch the latest raw data from two separate NocoDB tables (Leads and Unsubscribes).

**Step 3**
🔗 **MERGE TWO SHEETS** — Unifies the data streams into a single logical block for the reporting engine to process.

**Step 4**
⚙️ **GENERATE LEAD REPORT (DAILY)** — Advanced JavaScript logic that calculates:
* **Engagement:** Breakdown of Hot, Interested, and Not Interested leads.
* **Email Health:** Reachable vs. Unreachable ratios based on verification status.
* **Momentum:** A list of the most recent leads acquired within the last 24 hours.
* **Churn:** Real-time tracking of recent unsubscribes.

**Step 5**
💬 **SEND SLACK MESSAGE** — Formats the calculated data into a high-visibility Slack alert, using emojis and bold formatting for quick readability on mobile or desktop.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **Database:** NocoDB
* **Logic:** JavaScript (ES6) for metric aggregation
* **Communication:** Slack API (OAuth2)
* **Utility:** Schedule Trigger, Merge Node

---
*Developed by **Victordidit** | Design + Autonomy*
