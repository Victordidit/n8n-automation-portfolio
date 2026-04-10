# 📱 Social Media Content Scheduler

[**📂 View Workflow JSON**](./social-media-content-scheduler.json)

### Overview
This workflow functions as an automated social media manager. It picks up raw content ideas, applies specific platform constraints via JavaScript, and utilizes AI to craft optimized copy for LinkedIn, Twitter, and Instagram simultaneously—streamlining the content production pipeline from ideation to scheduling.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every day at 7am to prepare the day's social content.

**Step 2**
📊 **Google Sheets** — Reads pending content ideas from the planning spreadsheet.

**Step 3**
⚙️ **Code in JavaScript** — Injects platform-specific guidelines (character limits, hashtag rules) into the prompt logic.

**Step 4**
🤖 **OpenAI** — Writes tailored captions for LinkedIn, Twitter, and Instagram based on the enriched guidelines.

**Step 5**
⚙️ **Code in JavaScript1** — Cleans and structures the multi-platform AI output into distinct data fields.

**Step 6**
📧 **Gmail** — Creates draft posts and notifications for a final editorial review.

**Step 7**
⚙️ **Code in JavaScript2** — Prepares the confirmation data for the content tracker.

**Step 8**
📊 **Google Sheets1** — Updates the status of the ideas to "Scheduled" in the master sheet.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript
* **Social Ops:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
