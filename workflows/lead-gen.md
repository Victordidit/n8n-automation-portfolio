# 🤖 AI Lead Generation Workflow

### Overview
This automation serves as an autonomous lead scout. It scrapes raw business data, passes it through an AI scoring model to determine quality, and organizes the high-value results into a CRM-ready Google Sheet.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Manual Trigger** — Initiates the scraping sequence.

**Step 2**
🌐 **HTTP Request** — Targets the data source (e.g., books.toscrape.com) to pull live information.

**Step 3**
⚙️ **Code in JavaScript** — Custom logic to parse the HTML and extract core data points like Name, Price, and Rating.

**Step 4**
🤖 **OpenAI** — The AI engine analyzes the extracted data to score and summarize the potential lead.

**Step 5**
⚙️ **Code in JavaScript1** — Sanitizes the AI output to ensure it fits the database schema perfectly.

**Step 6**
📊 **Google Sheets** — Commits the enriched, qualified lead to the final CRM spreadsheet.

---

### 🛠️ Tech Stack
*   **Automation:** n8n
*   **AI:** OpenAI (GPT-4)
*   **Data:** JavaScript / HTTP Requests
*   **Storage:** Google Sheets

---
*Developed by **Victordidit** | Design + Autonomy*
