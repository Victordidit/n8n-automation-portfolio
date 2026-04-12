# 🤖 AI Customer Support Agent

[**📂 View Workflow JSON**](./ai-customer-support-agent.md)

### Overview
This workflow serves as a 24/7 intelligent first responder for customer inquiries. It captures support tickets instantly via form submission, cross-references a private knowledge base, and attempts to resolve the issue using AI. If the AI cannot provide a high-confidence solution, the workflow automatically escalates the ticket to a human agent, ensuring no customer is left without an answer.

---

## 🏗️ Workflow Structure

**Step 1**
📝 **On Form Submission** — Receives customer support tickets instantly as they are submitted via the support form.

**Step 2**
📊 **Google Sheets** — Reads existing knowledge base solutions and documentation.

**Step 3**
⚙️ **Code in JavaScript** — Performs a logical match between the customer's issue and available knowledge base articles.

**Step 4**
🤖 **OpenAI** — Generates a personalized, AI-powered support reply based on the matched documentation.

**Step 5**
🔀 **IF** — Evaluates whether the AI successfully resolved the issue based on confidence scoring.

**Step 6**
✅ **TRUE: Code in JavaScript1** — Cleans and formats the resolved ticket data for the final response.

**Step 7**
✅ **TRUE: Gmail** — Sends the finalized resolution draft directly to the customer.

**Step 8**
✅ **TRUE: Code in JavaScript2** — Prepares the data required for internal record-keeping.

**Step 9**
✅ **TRUE: Google Sheets1** — Logs the resolved ticket details into the "Success" database.

**Step 10**
❌ **FALSE: Gmail1** — Automatically sends an escalation alert and the full ticket history to a human agent.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **AI:** OpenAI (GPT-4)
* **Logic:** JavaScript / Form Trigger
* **Support Ops:** Google Sheets & Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
