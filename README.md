# UPI Digital Payments analysis

An end-to-end data analytics project that transforms raw UPI (Unified Payments Interface) transaction data into actionable insights.

## 📖 Project Overview

This project analyzes the **UPI Transactions Dataset** (2,50,000 records | 17 features) covering digital payment transactions made across Indian states throughout 2024. The analysis focuses on identifying transaction reliability issues, fraud patterns, and spending behavior to support data-driven decisions for payment platforms and banks.

## 🎯 Business Problem

As UPI transaction volumes continue to grow, ensuring transaction reliability and minimizing fraud have become critical for digital payment platforms. This project identifies transaction failures, fraud hotspots, customer spending patterns, and operational trends to support data-driven business decisions.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| MySQL | Data Cleaning, SQL querying, exploratory data analysis, and business analysis |
| MySQL Workbench | Database management and query execution |

## 📂 Dataset

**Source:** UPI Transactions 2024 Dataset
**Size:** 2,50,000 rows × 17 columns
**Time Period:** 2024
**Grain:** One row per UPI transaction (no customer-level ID)

**Dataset Includes**
- Transaction Type (P2P, P2M, Bill Payment, Recharge)
- Merchant Categories
- Sender/Receiver Banks
- Transaction Status & Fraud Flag
- Sender/Receiver Age Groups
- Sender State (Geographic Region)
- Device Type & Network Type
- Timestamp, Hour of Day, Day of Week, Weekend Flag

## 🔄 Project Workflow

Raw Dataset (250,000 Records)

⬇️

Manual Import into MySQL

⬇️

Data Exploration (SQL)

⬇️

Data Quality Assessment & Cleaning (SQL)

⬇️

Exploratory Data Analysis (SQL)

⬇️

Business Analysis (SQL)

⬇️

Insights & Recommendations

## 🗃️ SQL Analysis

* Data Exploration – Examined the dataset structure, transaction volume, time period, and key dimensions.
* Data Quality Assessment & Cleaning – Validated data integrity by checking for null values, duplicates, invalid records, and standardized text fields.
* Exploratory Data Analysis (EDA) – Analyzed transaction distribution across states, banks, merchant categories, devices, age groups, and time-based patterns.
* Business Analysis – Evaluated transaction value, success rates, fraud exposure, customer spending behavior, and banking performance using aggregations, CTEs, 
  and window functions.
* Business Insights & Recommendations – Converted analytical findings into actionable recommendations to improve transaction reliability, fraud monitoring, and 
  operational decision-making.

## 💡 Key Insights

- **SBI** leads on both transaction volume and value, contributing ~₹82.8M in total value — roughly ₹33M ahead of the #2 bank (HDFC, ~₹49.8M).
- Bank success rates are tightly clustered (94.9%–95.2%), meaning reliability is not a major differentiator between banks.
- **Shopping** drives the highest total transaction value (~₹76.9M), while **Education** has the highest average ticket size per transaction.
- Overall fraud rate is low at ~0.19% (480 of 250,000 transactions), with **Karnataka** and **Rajasthan** showing the highest state-level fraud rates (~0.23%).
- **Transport** and **Education** categories have the highest category-level fraud rates (~0.21%), despite not being the highest-value categories.
- Spending peaks in the **36–45 age group** (~₹1,424 avg/transaction) and declines for both younger and older senders.
- Evening hours (**18:00–20:00**) dominate both transaction volume and value, with hour 19 alone contributing ~₹28.2M.

## 🚀 Business Recommendations

- Focus reliability engineering on closing the small success-rate gap at Yes Bank/ICICI rather than treating it as a major outage risk.
- Scale infrastructure and fraud-review staffing specifically for the 18:00–20:00 window, the single heaviest period for volume and value.
- Apply tighter fraud-detection thresholds to Education and Transport transactions, which combine above-average fraud rates with meaningful transaction values.
- Run state-specific fraud monitoring for Karnataka and Rajasthan given their consistently elevated fraud rates.
- Design retention offers around the 36–45 age segment (highest average spend) and acquisition-style incentives for the 18–25 and 56+ segments.
- Treat weekend dips as a volume problem, not a behavior-change problem — weekend promotions should aim to drive more transactions rather than bigger ones.

## 👩‍💻 Author

**Vaishnavi V**

Aspiring Data Analyst
