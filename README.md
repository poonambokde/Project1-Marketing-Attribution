##Multi-Touch Marketing Attribution & ROI Dashboard

Infotact Solutions — Data Analytics Internship 2026
Intern: Poonam Bokade
Duration: 4 Weeks | June 2026
Location: Bengaluru, Karnataka


🎯 Problem Statement

E-commerce companies spend millions across multiple advertising channels (Google Ads, Meta, TikTok, LinkedIn). Traditional Last-Click attribution gives 100% credit to the final ad — causing budget misallocation.

This project builds a Multi-Touch Attribution Engine that fairly distributes conversion credit across all touchpoints and calculates true ROAS and CAC per channel.


🛠️ Tools & Technologies

ToolPurposePython (Pandas, Seaborn)Data cleaning & EDASQL (SQLite)Attribution logic & Window FunctionsPower BIInteractive dashboardGitHubVersion control & collaboration


📁 Project Structure

Project1-Marketing-Attribution/
├── notebooks/
│   ├── 01-EDA.ipynb              ← Week 1: Data cleaning & EDA
│   ├── 02_SQL_Attribution.ipynb  ← Week 2: SQL attribution models
│   └── 03_KPI_Metrics.ipynb      ← Week 3: KPI calculations
├── Data/
│   ├── Raw/                      ← Original synthetic datasets
│   └── Processed/                ← Cleaned & transformed data
├── outputs/
│   ├── channel_distribution.png
│   ├── ad_spend_by_channel.png
│   ├── revenue_by_channel.png
│   ├── cac_by_channel.png
│   ├── roas_by_channel.png
│   └── dashboard_screenshot.png
├── Marketing_Attribution_Dashboard.pbix
├── Executive_Summary_Detailed_Report.docx
├── generate_marketing_data.py
└── README.md


📊 Dataset

Three synthetic datasets generated using Python:

DatasetRowsDescriptionad_spend_data.csv1,350Daily channel-wise spend, clicks, impressionsweb_analytics_log.csv6,034User session touchpoints with UTM parameterscrm_conversion_data.csv600Customer conversions and revenue

Coverage: 2,000 users | 90 days | 6 channels | 14 campaigns


🔄 4-Week Sprint Summary

✅ Week 1 — Data Ingestion & EDA


Loaded 3 datasets using Pandas
Handled missing UTM parameters (10% missing values)
Normalized timestamps to UTC format
Removed duplicate records
Generated 3 EDA visualizations


✅ Week 2 — SQL & Attribution Logic


Loaded cleaned data into SQLite database
Used ROW_NUMBER() OVER (PARTITION BY user_id ORDER BY timestamp) to sequence user journeys
Implemented 3 attribution models:

First-Touch — 100% credit to first touchpoint
Last-Touch — 100% credit to last touchpoint
Linear — Equal credit across all touchpoints





✅ Week 3 — KPI Metric Calculation


Calculated CPC (Cost Per Click)
Calculated CAC (Customer Acquisition Cost)
Calculated ROAS (Return on Ad Spend)
Built KPI Master Table for Power BI


✅ Week 4 — Power BI Dashboard & Report


Connected Power BI to processed CSV files
Built 4 interactive visuals:

ROAS by Channel (Bar Chart)
CAC by Channel (Bar Chart)
Conversions by Channel (Bar Chart)
Channel Slicer (Interactive Filter)



Written Executive Summary Report with findings & recommendations



📈 Key Findings

ChannelROASCAC ($)Top Attribution ModelEmail0.31 ⭐ Best805 ✅ LowestFirst-TouchTikTok0.161,476LinearMeta Facebook0.142,041First-TouchGoogle Search0.092,894Last-TouchLinkedIn0.07 ❌ Worst4,133 ❌ HighestLinearOrganicFree0All Models


💡 Business Recommendations


📈 Increase Email & Organic budget — highest efficiency
✅ Maintain TikTok & Meta Facebook — strong awareness channels
⚠️ Optimize Google Search — reduce broad keywords
❌ Reduce LinkedIn — highest CAC, lowest ROAS



🚀 How to Run

bash# Step 1: Generate datasets
python generate_marketing_data.py

# Step 2: Run notebooks in order
# notebooks/01-EDA.ipynb
# notebooks/02_SQL_Attribution.ipynb
# notebooks/03_KPI_Metrics.ipynb

# Step 3: Open Power BI dashboard
# Marketing_Attribution_Dashboard.pbix


👩‍💻 About

Poonam Bokade
Data Analytics Intern — Infotact Solutions, Bengaluru 2026
B.Tech Computer Engineering | MPIT Maharashtra
