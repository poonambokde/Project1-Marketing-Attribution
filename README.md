Project 1: Multi-Touch Marketing Attribution & ROI Dashboard

Infotact Solutions — Data Analytics Internship 2026

Intern: Poonam Bokade
Duration: 4 Weeks | June 2026
Location: Bengaluru, Karnataka


🎯 Problem Statement

E-commerce and SaaS companies spend significant budgets across multiple advertising channels (Google Search, Meta Facebook, TikTok, LinkedIn, Email, Organic). Customer journeys are complex — a user might click a Meta ad on Monday, read a blog on Wednesday, and convert via Google Search on Friday.

Traditional Last-Click attribution gives 100% of the credit to Google in this example, causing marketing teams to misallocate budgets and undervalue top-of-funnel channels.

This project builds a complete Multi-Touch Attribution Engine that fairly distributes conversion credit across every touchpoint and calculates the true ROAS (Return on Ad Spend) and CAC (Customer Acquisition Cost) per channel — presented through an interactive Power BI dashboard.


🛠️ Tools & Technologies

ToolPurposePython (Pandas, Seaborn)Data cleaning, EDA, visualizationsSQL (SQLite)Attribution logic using Window FunctionsPower BI (DAX)Interactive dashboard & KPI cardsMS WordExecutive Summary ReportGitHubVersion control & daily commits


📁 Project Structure

Project1-Marketing-Attribution/
├── 01-EDA.ipynb                              ← Week 1: Data cleaning & EDA
├── 02_SQL_Attribution.ipynb                  ← Week 2: SQL attribution models
├── 03_KPI_Metrics.ipynb                      ← Week 3: KPI calculations
├── Marketiing_Attribution_Dashboard.pbix     ← Week 4: Power BI dashboard
├── Executive_Summary_Final_Report.docx       ← Week 4: Executive report
├── Executive_Summary_Final_Report.pdf        ← Week 4: Executive report (PDF)
├── first_touch_attribution.csv
├── last_touch_attribution.csv
├── linear_attribution.csv
├── generate_marketing_data.py                ← Synthetic dataset generator
├── Data/
│   ├── Row/                                  ← Original synthetic datasets
│   └── Processed/                            ← Cleaned & transformed data
├── outputs/                                  ← All charts & dashboard screenshot
└── README.md


📊 Dataset

Three synthetic datasets generated using Python, simulating 90 days (Jan–Mar 2024) of marketing activity across 2,000 unique users, 6 channels, and 14 campaigns:

DatasetRowsKey Columnsad_spend_data.csv1,350date, channel, campaign, amount_spent_usd, clicks, impressions, cpcweb_analytics_log.csv6,034session_id, user_id, timestamp, channel, utm_source, utm_campaign, devicecrm_conversion_data.csv600customer_id, conversion_date, revenue_usd, last_touch_channel, product_purchased


🔄 4-Week Sprint Summary

✅ Week 1 — Data Ingestion & EDA


Loaded 3 datasets using Pandas
Fixed missing UTM parameters (~10% missing, filled with 'unknown')
Normalized timestamps to UTC using pd.to_datetime()
Removed duplicate records using drop_duplicates()
Generated EDA visualization: User Sessions by Channel


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
Fixed division-by-zero (∞) issue for Organic channel
Built KPI Master Table for Power BI


✅ Week 4 — Power BI Dashboard & Reporting


Built dashboard header and 4 KPI summary cards using DAX measures
Built 4 interactive visuals: ROAS, CAC, Conversions, Channel Slicer
Written detailed Executive Summary Report (Word + PDF)



Dashboard Components:


Header: "Multi-Touch Marketing Attribution Dashboard"
KPI Cards: Total Spend ($1.24M) | Total Conversions (600) | Best ROAS (Email — 0.31) | Highest CAC (LinkedIn — $4,133.82)
ROAS by Channel — Bar chart
CAC by Channel — Bar chart
Conversions by Channel — Funnel chart
Channel Slicer — Interactive filter across all visuals



📊 Key Findings

ChannelROASCAC ($)CPC ($)ConversionsEmail0.31 ⭐ Best805.43 ✅ Lowest1.3757TikTok0.161,476.181.36102Meta Facebook0.142,041.751.35149Google Search0.092,894.031.45167LinkedIn0.07 ❌ Worst4,133.82 ❌ Highest1.3161OrganicFree0.000.0064


💡 Business Recommendations

ActionChannelReason📈 Increase BudgetEmail, OrganicHighest ROAS, lowest CAC, near-zero cost✅ Maintain BudgetTikTok, Meta FacebookStrong awareness + conversion balance⚠️ OptimizeGoogle SearchHigh spend, low ROAS — refine keyword targeting❌ Reduce BudgetLinkedInHighest CAC, lowest ROAS — only viable for B2B

Estimated Impact: Reallocating budget from LinkedIn and broad Google Search toward Email, Organic, and TikTok is projected to improve overall ROAS by 15–25%.


🚀 How to Run This Project

bash# Step 1: Generate synthetic datasets
python generate_marketing_data.py

# Step 2: Run notebooks in order
jupyter notebook 01-EDA.ipynb
jupyter notebook 02_SQL_Attribution.ipynb
jupyter notebook 03_KPI_Metrics.ipynb

# Step 3: Open the Power BI dashboard
# Marketiing_Attribution_Dashboard.pbix


📄 Reports

📕 Executive Summary Report (PDF)



👩‍💻 About

Poonam Bokade
Data Analytics Intern — Infotact Solutions, Bengaluru 2026
B.Tech Computer Engineering | MPIT Maharashtra

GitHub Repository: Project1-Marketing-Attribution
ShareContent01-EDA.ipynbipynb01-EDA (1).ipynbipynb01-EDA.ipynbipynb03_KPI_Metrics.ipynbipynb01-EDA.ipynbipynb03_KPI_Metrics.ipynbipynbMarketiing_Attribution_Dashboard.pbixpbixgenerate_marketing_data.py181 linespy02_SQL_Attribution.ipynb332 linesipynb02_SQL_Attribution.ipynb332 linesipynbparameterscrm_conversion_data.csv600Customer conversions and revenue

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
