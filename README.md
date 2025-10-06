# Autoblog Engine 🚀

An AI-powered, fully automated blogging pipeline leveraging n8n, Google Sheets, and Gemini for end-to-end content creation and social media distribution. This project turns a simple Google Sheet into a powerful content strategy and generation dashboard.



## ✨ Overview

Manually handling SEO research, writing articles, and crafting social media posts is time-consuming. **Autoblog Engine** automates the entire process. It starts with a cron job, performs in-depth SEO research, generates high-quality articles, creates corresponding social media posts, and then publishes them, all with minimal human intervention.

The entire workflow is orchestrated by **n8n**, with **Google Sheets** acting as the central "brain" and control panel, updated in real-time via webhooks and enhanced with **Google Apps Script**.

---

## 核心功能 (Core Features)

* **🤖 Automated SEO Research:** Uses **DataForSEO** and **Gemini** to analyze target audiences, find primary keywords, and conduct other foundational research.
* **📊 Centralized Control via Google Sheets:** All research data, content ideas, and status updates are managed in a Google Sheet, which acts as the project's single source of truth.
* **⚡️ High-Frequency Triggers:** A **Google Apps Script** function triggers every 5 minutes to process data within the sheet.
* **✍️ AI-Powered Article Generation:** Leverages **RightBlogger** to write complete, SEO-optimized articles based on the research data.
* **📱 Smart Social Media Generation:** **Gemini** analyzes the final article to generate contextually relevant posts for various social media platforms.
* **🔄 End-to-End Orchestration:** **n8n** manages the entire workflow, from the initial cron trigger to the final API calls for uploading content.

---

## 🛠️ Tech Stack

* **Orchestration:** n8n
* **Database / Control Panel:** Google Sheets
* **Custom Functions:** Google Apps Script
* **AI Brain / Social Posts:** Google Gemini
* **SEO Data:** DataForSEO API
* **Article Generation:** RightBlogger
* **Connectivity:** Webhooks

---

## ⚙️ How It Works (Workflow)

1.  **Trigger:** An **n8n** cron job initiates the workflow on a set schedule.
2.  **Research:** n8n calls **DataForSEO** and **Gemini** APIs to gather SEO data, keywords, and audience insights for a given topic in a particular neeche.
3.  **Sheet Update:** The research data is sent to **Google Sheets** via a webhook.
4.  **Internal Processing:** A time-based **Google Apps Script** trigger runs, processing the new data, perhaps refining topics, preparing content briefs.
5.  **Content Generation:** Based on the cells filled, a status section updates automatically, the researched data is put into RightBlogger to develop the article, SEO optimization, etc. and the link is posted back in the sheet.
6.  **Social Media Creation:** The generated article text is sent to the **Gemini** API, which returns formatted posts for social media, images are generated seperately curated for each social media.
7.  **Distribution:** n8n takes the social posts and uploads them to respective social media accounts.

---

## 🚀 Getting Started

### Prerequisites

* An [n8n](https://n8n.io/) instance (cloud or self-hosted).
* Google Account (for Sheets and Apps Script).
* API keys for:
    * Google Gemini
    * DataForSEO
    * Your social media platforms.
* Account for RightBlogger
