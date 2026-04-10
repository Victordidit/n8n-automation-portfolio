# 🎯 Job Application & Recruitment Pipeline

[**📂 View Workflow JSON**](./job-application-recruitment-pipeline.json)

### Overview
This workflow acts as an automated HR assistant, streamlining the initial stages of recruitment. It monitors new applications, applies a custom JavaScript scoring logic to filter candidates by skill, and uses AI to draft personalized communications for both the applicant and the hiring manager—ensuring no candidate is left waiting.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Checks for new applications every 30 minutes to ensure a rapid response time.

**Step 2**
📊 **Google Sheets** — Reads the latest entries from the job application spreadsheet.

**Step 3**
⚙️ **Code in JavaScript** — Scores each candidate based on specific skill requirements and keywords.

**Step 4**
🤖 **OpenAI** — Writes tailored confirmation emails for the candidate and an evaluation summary for the manager.

**Step 5**
⚙️ **Code in JavaScript1** — Cleans and structures the AI-generated text for professional communication.

**Step 6**
📧 **Gmail** — Sends a personalized confirmation draft to the candidate.

**Step 7**
⚙️ **Code in JavaScript2** — Passes the scored data and summary into the manager’s notification block.

**Step 8**
📧 **Gmail1** — Sends a detailed evaluation draft to the hiring manager for review.

**Step 9**
⚙️ **Code in JavaScript3** — Prepares the final data required for the internal status update.

**Step 10**
📊 **Google Sheets1** — Updates the candidate's application status in the master tracker.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript
* **Management:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
