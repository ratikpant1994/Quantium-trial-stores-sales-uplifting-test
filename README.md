🛍️ Trial vs Control Store Uplift Analysis - Retail Analytics Project
This repository presents a retail analytics project conducted to evaluate the effectiveness of a store trial rolled out in selected locations. The primary objective was to determine whether the trial led to statistically significant uplifts in key performance metrics such as total sales, customer footfall, and transactions per customer, using uplift modeling and control store comparison.

🧠 Business Problem
A retail chain launched a marketing and operational trial in three stores (77, 86, 88) between February and April 2019. The goal was to test new strategies and evaluate their impact before wider implementation.

To assess performance:

Trial stores were compared with control stores (non-trial) selected using historical similarity metrics.

We calculated monthly uplift in KPIs and tested statistical significance using pre- and post-trial comparisons.

📊 Dataset
The dataset contained transaction-level data with ~250,000 rows from July 2018 to June 2019, with the following fields:

LYLTY_CARD_NBR: Customer loyalty ID

DATE, MONTH, YEAR, DAY

STORE_NBR: Store number

TXN_ID: Transaction ID

TOT_SALES, PROD_QTY, PROD_NAME

LIFESTAGE, PREMIUM_CUSTOMER

PACK_SIZE, price_per_product

🔧 Project Workflow
🧹 1. Data Cleaning & Feature Engineering
Created new fields: total_spend, monthly_sales, product_bought, price_per_product, pack_size_num

Filtered for trial period and corresponding pre-trial data

Converted dates into time series and extracted monthly granularity

📈 2. Monthly Metrics Computed
For each store (trial and control), we computed:

Total sales revenue

Total number of unique customers

Transactions per customer

🤝 3. Control Store Selection
Computed correlation scores on pre-trial metrics (Jul 2018 - Jan 2019)

Selected control stores with highest correlation for each trial store

Ensured matched seasonality and similar transaction profiles

📊 4. Uplift Measurement
Compared trial vs control performance during the trial window (Feb–Apr 2019)

Calculated percentage uplift in each KPI

Performed t-tests and visualized trends to ensure statistical significance

🔍 Key Results


📌 Conclusion: Stores 77 and 86 showed statistically significant uplifts in performance during the trial. Store 88 showed moderate improvement, but the results were not statistically conclusive.

📈 Visualizations
Sales trend lines with trial period highlighted

Uplift bars comparing trial vs control

Heatmaps for customer behavior by month

Pre-trial correlation matrices

