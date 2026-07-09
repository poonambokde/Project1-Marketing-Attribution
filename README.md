Project 1: Multi-Touch Marketing Attribution & ROI Dashboard

Infotact Solutions — Data Analytics Internship 2026

Intern: Poonam Bokade
Duration: 4 Weeks | June 2026
Location: Bengaluru, Karnataka


🎯 Problem Statement

E-commerce and SaaS companies spend significant budgets across multiple advertising channels (Google Search, Meta Facebook, TikTok, LinkedIn, Email, Organic). Customer journeys are complex — a user might click a Meta ad on Monday, read a blog on Wednesday, and convert via Google Search on Friday.

Traditional Last-Click attribution gives 100% of the credit to Google in this example, causing marketing teams to misallocate budgets and undervalue top-of-funnel channels.

This project builds a complete Multi-Touch Attribution Engine that fairly distributes conversion credit across every touchpoint and calculates the true ROAS (Return on Ad Spend) and CAC (Customer Acquisition Cost) per channel — presented through an interactive Power BI dashboard.

Tools & Technologies

Tool                                                           Purpose
Python (Pandas, Seaborn)                                  Data cleaning, EDA, visualizations
SQL (SQLite)                                              Attribution logic using Window Functions
Power BI                                                  (DAX)Interactive dashboard & KPI cards
MS Word                                                   Executive Summary Report
GitHub                                                    Version control & daily commits

Project Structure

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

Dataset

Three synthetic datasets generated using Python, simulating 90 days (Jan–Mar 2024) of marketing activity across 2,000 unique users, 6 channels, and 14 campaigns:

Dataset                         Rows                      Key Columns
ad_spend_data.csv1,             350date,                 channel, campaign, amount_spent_usd, clicks, impressions, cpc
web_analytics_log.csv           6034                     session_id, user_id, timestamp, channel, utm_source, utm_campaign, device
crm_conversion_data.csv         600                      customer_id, conversion_date, revenue_usd, last_touch_channel, product_purchased


🔄 4-Week Sprint Summary

Week 1 — Data Ingestion & EDA

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



📈 Dashboard Preview

<img width="1367" height="797" alt="Screenshot 2026-06-13 124627" src="https://github.com/user-attachments/assets/7f39bff0-80c5-477a-bb89-5bce4fef0ba6" />


Dashboard Components:

Header: "Multi-Touch Marketing Attribution Dashboard"
KPI Cards: Total Spend ($1.24M) | Total Conversions (600) | Best ROAS (Email — 0.31) | Highest CAC (LinkedIn — $4,133.82)
ROAS by Channel — Bar chart
CAC by Channel — Bar chart
Conversions by Channel — Funnel chart
Channel Slicer — Interactive filter across all visuals


Key Findings

Channel                       ROAS                      CAC($)                       CPC($)                       Conversions
Email                         0.31 ⭐ Best              805.43 ✅ Lowest             1.37                          57
TikTok                        0.16                       1,476.18                     1.36                          102
Meta Facebook                 0.14                       2,041.75                     1.35                          149
Google Search                 0.09                       2,894.03                     1.45                          167
LinkedIn                      0.07 ❌ Worst              4,133.82 ❌ Highest         1.31                          61
Organic                       Free                        0.00                        0.00                          64


Business Recommendations

Action                           Channel                             Reason📈 
Increase Budget                  Email, Organic                      Highest ROAS, lowest CAC, near-zero cost
✅ Maintain Budget               TikTok, Meta Facebook               Strong awareness + conversion balance
⚠️ Optimize                      Google Search                       High spend, low ROAS — refine keyword targeting
❌ Reduce Budget                 LinkedIn                            Highest CAC, lowest ROAS — only viable for B2B

Estimated Impact:
Reallocating budget from LinkedIn and broad Google Search toward Email, Organic, and TikTok is projected to improve overall ROAS by 15–25%.

How to Run This Project

# Step 1: Generate synthetic datasets
python generate_marketing_data.py

# Step 2: Run notebooks in order
jupyter notebook 01-EDA.ipynb
jupyter notebook 02_SQL_Attribution.ipynb
jupyter notebook 03_KPI_Metrics.ipynb

# Step 3: Open the Power BI dashboard
# Marketiing_Attribution_Dashboard.pbix

Reports

📕 Executive Summary Report (PDF)


About

Poonam Bokade
Data Analytics Intern — Infotact Solutions, Bengaluru 2026
B.Tech Computer Engineering | MPIT Maharashtra

GitHub Repository: Project1-Marketing-Attribution

Final Project Submitted
