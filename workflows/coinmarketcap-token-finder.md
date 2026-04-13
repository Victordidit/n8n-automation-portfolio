# 📈 CoinMarketCap Token Finder (Automated Alpha)

[**📂 View Workflow JSON**](./coinmarketcap-token-finder.json)

### Overview
This high-performance workflow is designed to discover and log cryptocurrency tokens automatically. It bypasses manual searching by programmatically cycling through CoinMarketCap listings, fetching deep-level token details (like official websites and social links), and cleaning the data through rigorous JavaScript logic. The final, verified data is then synced to a NocoDB database, creating a clean "alpha" list for further analysis.

---

## 🏗️ Workflow Structure

**Step 1**
▶ **Every 2 Days At 9AM** — A schedule trigger that keeps the database fresh by running the discovery cycle every 48 hours.

**Step 2**
⚙️ **Generate Random Page** — Custom JavaScript that randomizes API query parameters (sort direction, limit, and offset) to ensure the workflow discovers a wide variety of tokens rather than just the top 100.

**Step 3**
🌐 **Get 100 Tokens From CMC** — An HTTP Request that calls the CoinMarketCap API to retrieve the randomized batch of tokens.

**Step 4**
⚙️ **Split Out & CLEAN CMC FIELDS** — These nodes break the large API response into individual items and filter for essential identifiers like Name, Symbol, Slug, and CMC ID.

**Step 5**
⚙️ **CMC SPLIT IN BATCHES** — A loop mechanism that processes tokens in batches of 10 to respect API rate limits and ensure stable data fetching.

**Step 6**
🌐 **Get Token Details From CMC** — A secondary API call that uses the specific Token ID to fetch deep metadata, specifically looking for official project URLs.

**Step 7**
⚙️ **EXTRACT & CLEAN WEBSITE** — Advanced JavaScript logic that sanitizes messy URL data, forces HTTPS protocols, and discards broken or empty links.

**Step 8**
⏳ **Wait 1 Min** — A built-in delay to prevent rate-limiting (429 errors) during high-volume metadata retrieval.

**Step 9**
⚙️ **Clean up Output / DATA** — Final formatting nodes that prepare the token, ticker, source, and timestamp for database insertion.

**Step 10**
📊 **ADD TO CMC Sheet (NocoDB)** — The final storage step that logs the verified, cleaned token data into a central repository for easy viewing.

---

### 🛠️ Tech Stack
* **Automation:** n8n
* **API:** CoinMarketCap Professional API
* **Logic:** Advanced JavaScript (ES6)
* **Database:** NocoDB (Self-hosted or Cloud)
* **Utilities:** HTTP Request, Split in Batches, Wait Node

---
*Developed by **Victordidit** | Design + Autonomy*
