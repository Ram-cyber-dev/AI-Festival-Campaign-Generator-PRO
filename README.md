# 🎁 AI Festival Campaign Generator PRO — 4-Agent Production Engine

One form. One festival. 90 seconds. A complete D2C festival campaign — strategy, 50+ assets, 3 AI visuals, 4 languages, competitive intelligence, ROI prediction, QA scored, delivered.


## 🎯 What It Does

Takes a single festival campaign form and automatically generates:
- **Festival intelligence** — cultural psychology, emotional triggers, shopping behaviour, hashtags, colour palette
- **50+ marketing assets** — FB/IG/Google ads, 9-email sequence, social posts, WhatsApp, banners, influencer brief, content calendar
- **3 AI-generated festival visuals** — product shot, Instagram story, ad banner — uploaded to Google Drive
- **4-language regional pack** — Hindi, Tamil, Bengali, Marathi
- **Competitor ad spy** — what rivals are running + counter-ads that attack their weaknesses
- **Festival ROI prediction** — projected revenue, CAC, ROAS, break-even units, peak sales window
- **QA scorecard** — 6-dimension quality review before delivery
- **Dual email delivery** — mega kit to agency + executive brief to brand owner
- **Google Sheets CRM** — every campaign logged automatically


## 🤖 4 AI Agents + 3 Enhancement Agents

| Agent | Role | Model |
|-------|------|-------|
| Agent 1: Festival Intelligence | Cultural strategy, emotional triggers, image prompts | Gemini 2.0 Flash |
| Agent 2: Festival Copywriter | 50+ assets across all channels | Gemini 2.5 Flash |
| Agent 3: Visual Generator ×3 | Product shot, story, ad banner | gpt-image-2 |
| Agent 4: QA Reviewer | 6-dimension quality scorecard | Gemini 2.5 Flash |
| Regional Language Pack | Hindi + Tamil + Bengali + Marathi | GPT-4o-mini |
| Competitor Ad Spy | Counter-ads against competitor weaknesses | GPT-4o-mini |
| Festival ROI Predictor | Revenue, CAC, ROAS, break-even forecast | GPT-4o-mini |


## 🏗️ Architecture (31 nodes)

Form → Parse+CampaignID → Agent1:Intel → Parse Intel → Build Agent2 Prompt →
Agent2:50+Copy → Parse Kit → Agent3:FestVisual + Agent3b:StoryVisual + Agent3c:AdBanner →
Package Images → Create Drive Folder → Attach Binary+FolderID →
Upload Festival + Story + Banner (parallel) → Wait for All Uploads →
Build QA Prompt → Agent4:QA → Parse QA+DriveLink →
Regional Language Pack → Parse Languages →
Competitor Ad Spy → Parse Competitor Intel →
Festival ROI Predictor → Parse ROI →
Log to Sheets → Build Campaign Kit Email → Send to Agent →
Build Owner Brief → Send to Owner


## ⚙️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Automation | n8n (self-hosted) |
| Festival Intel + Copy + QA | Gemini 2.0/2.5 Flash |
| Image Generation | gpt-image-2 (OpenAI) |
| Languages + Spy + ROI | GPT-4o-mini |
| Asset Storage | Google Drive |
| CRM Logging | Google Sheets |
| Email Delivery | Gmail API |


## 🚀 Key Features

- **31 nodes** — most advanced workflow in the cohort
- **20 festivals** in one dropdown — Diwali, Holi, Christmas, Eid, Navratri, Big Billion Days + 14 more
- **Auto Campaign ID** — FEST-GLOWVEDA-DIWALI-XXXXXX ties Drive, Sheets, emails together
- **3 AI visuals** uploaded to dedicated Drive folder per campaign
- **4-language regional pack** — not just translation, cultural adaptation
- **Competitor ad spy** — counter-ads that exploit competitor weaknesses
- **ROI prediction** — data-driven forecast before any spend
- **QA gate** — campaign scored before delivery
- **Error resilience** — fallbacks at every AI parsing stage


## 💡 Business Value

**Agency cost per festival:** ₹50,000 – ₹2,00,000 · 4 weeks  
**8-10 festivals a year:** ₹5,00,000+  
**This system costs:** nearly ₹0 · 90 seconds


## 🔧 Setup

1. Import `AI_Festival_Campaign_Generator_PRO.json` into n8n
2. Configure credentials:
   - **Google Gemini** — Query Auth with Gemini API key
   - **OpenAI** — API key (gpt-4o-mini + gpt-image-2 access required)
   - **Gmail** — OAuth2
   - **Google Sheets** — OAuth2, create sheet named "Festival Campaigns" with tab "Festival_Campaigns_Tab"
   - **Google Drive** — OAuth2, create parent folder "AI Festival Campaigns"
3. Sheet columns: festival, productName, category, productDesc, price, targetAudience, brandName, brandVoice, campaignDuration, competitors, availableOn, ownerName, ownerEmail, agentName, agencyName, agentEmail, campaignId, timestamp, dateGenerated, intel, kit, hasFestImg, hasStoryImg, hasBannerImg, imageCount, qa, driveFolderId, driveFolderLink


## 🎬 Demo Product

**GlowVeda 24K Gold Radiance Face Serum** — Diwali campaign. MRP ₹1,299, festival price ₹799. Competitors: Minimalist, Plum, Dot & Key, The Derma Co, Forest Essentials.


## 👤 Author

Built by Ram
Founder, MissedCallRecovery.org — AI voice receptionist 
platform for US plumbing and HVAC businesses
Available for freelance AI automation projects 
Building done-for-you AI systems for D2C brands and service businesses  
[GitHub](https://github.com/Ram-cyber-dev)
