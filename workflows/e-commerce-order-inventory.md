# 🛒 E-commerce Order & Inventory

[**📂 View Workflow JSON**](./inventory.json)

### Overview
This workflow automates the stock management cycle. It monitors new orders every 5 minutes, validates inventory availability, notifies the warehouse team of new tasks, and keeps the master inventory sheet perfectly synced.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Schedule Trigger** — Checks for new orders every 5 minutes to ensure rapid fulfillment.

**Step 2**
📊 **Google Sheets** — Reads new orders directly from the Orders Sheet.

**Step 3**
⚙️ **Code in JavaScript** — Processes and parses the raw order details for analysis.

**Step 4**
📊 **Google Sheets1** — Reads current live inventory levels from the Inventory Sheet.

**Step 5**
⚙️ **Code in JavaScript1** — Logic to check stock availability and detect low-stock thresholds.

**Step 6**
📧 **Gmail** — Generates and sends a warehouse notification draft for order picking.

**Step 7**
⚙️ **Code in JavaScript2** — Prepares and structures the final inventory update data.

**Step 8**
📊 **Google Sheets2** — Updates the final stock levels in the Inventory Sheet.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **Logic:** JavaScript
* **Storage:** Google Sheets API
* **Communication:** Gmail API

---
*Developed by **Victordidit** | Design + Autonomy*
