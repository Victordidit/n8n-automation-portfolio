# 📍 Google Maps Lead Extractor & Website Scraper

[**📂 View Workflow JSON**](./gmaps-lead-extractor.json)

### Overview
This workflow is a powerful lead generation engine that automates the transition from "local search" to "actionable contact data." It doesn't just pull basic business info; it proactively visits business websites to hunt for hidden emails, social media profiles, and service details that aren't available on Google Maps alone.

---

## 🏗️ Workflow Structure

**Step 1: The Input**
📩 **Webhook** — Accepts a `search_query` (e.g., "Dentists in New York") to kick off the automation via API or external trigger.

**Step 2: Maps Discovery**
🔍 **Search Google Maps (SerpApi)** — Queries Google Maps for up to 22 local businesses, retrieving titles, ratings, phone numbers, and website URLs.
💻 **Process Maps Data** — Normalizes the raw API response into a clean, structured list.

**Step 3: Intelligence & Scraping**
🌐 **Clean Website & Check Exists** — Filters out businesses without websites and formats URLs for safe scraping.
🕷️ **Scrape Website (HTTP Request)** — Visits the homepage of each business to pull raw HTML.
🧠 **Enhanced Data Extraction** — A custom JavaScript engine using Regex to extract:
* **Direct Emails:** Bypasses "Contact Us" forms to find valid email addresses.
* **Social Links:** Identifies Facebook, Instagram, and LinkedIn profiles.
* **Metadata:** Grabs business descriptions and service offerings from meta tags.

**Step 4: The Archive**
💾 **Save to Google Sheets** — Automatically appends or updates the business data in a master spreadsheet, mapping columns for `Business Name`, `Email`, `Social Media`, `Rating`, and more.

---

## 🛠️ Tech Stack
* **Automation:** n8n
* **Search Engine:** SerpApi (Google Maps Engine)
* **Database:** Google Sheets
* **Logic:** Enhanced Regex + JavaScript (ES6)
* **Handling:** Built-in "Wait" states to prevent IP blocking and ensure scraping reliability.

---
*Developed by **Victordidit** | Design + Autonomy*
