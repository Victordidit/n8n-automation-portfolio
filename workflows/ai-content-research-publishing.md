# 📝 AI Content Research & Publishing

[**📂 View Workflow JSON**](./ai-content-research-publishing.json)

### Overview
This workflow operates as an automated content department. It monitors the VentureBeat RSS feed daily, uses AI to select the most impactful tech news, and generates a comprehensive 800-word blog post along with optimized social media captions. The result is a fully drafted content calendar logged into a central pipeline.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Runs every morning at 6am to capture the latest news.

**Step 2**
🌐 **HTTP Request** — Fetches the live VentureBeat RSS news feed.

**Step 3**
⚙️ **Code in JavaScript** — Parses the raw XML and extracts individual article data.

**Step 4**
🤖 **OpenAI** — Analyzes headlines to select the most relevant article for the target audience.

**Step 5**
⚙️ **Code in JavaScript1** — Cleans and prepares the selected article data for writing.

**Step 6**
🤖 **OpenAI1** — Writes a full, SEO-optimized 800-word blog post based on the news item.

**Step 7**
⚙️ **Code in JavaScript2** — Cleans and structures the blog post output for draft formatting.

**Step 8**
📧 **Gmail** — Delivers the completed blog post draft to the editor's review queue.

**Step 9**
🤖 **OpenAI2** — Writes tailored promotional posts for LinkedIn, Twitter, and Instagram.

**Step 10**
⚙️ **Code in JavaScript3** — Cleans and separates the social media captions into distinct fields.

**Step 11**
📊 **Google Sheets** — Logs the article, blog content, and social posts to the master pipeline sheet.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript / RSS
* **Output:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
