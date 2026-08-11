# 📊 Electronics Retail Sales Analytics — Power BI Dashboard
> A comprehensive **multi-channel electronics retail sales analytics** dashboard built with Power BI, covering 15,000 transactions across 13 Indian stores and one online platform over a 2-year period (Jan 2024 – Jan 2026).
---
## 📸 Dashboard Preview
### 🖥️ Executive Dashboard
![Executive Dashboard](./Executive%20Dashboard.png)

### 📊 Sales Analysis
![Sales Analysis](./Sales%20Analysis.png)

### 🛍️ Product Deep Dive
![Product Deep Dive](./Product%20Deep%20Dive.png)

### 🏬 Store Performance
![Store Performance](./Store%20Performance.png)

### 👤 Customer Analytics
![Customer Analytics](./Customer%20Analytics.png)

### 🗄️ Database Structure (Star Schema)
![DB Structure](./db%20structure.png)
---

## 🚀 Project Overview

**Business Context:**  
This project analyzes the sales performance of an electronics retail chain with **13 physical stores** and **1 online platform** across major Indian cities. The business sells **190 products** across **7 categories** from **10+ premium brands** including Samsung, Apple, Xiaomi, OnePlus, LG, Sony, boAt, and more.

**Project Objectives:**
- Monitor real-time sales performance across products, stores, and channels
- Identify top-performing products and optimize product mix strategy
- Analyze customer purchasing behavior and lifetime value
- Evaluate store-level profitability and operational efficiency
- Track seasonal trends and enable demand forecasting
- Compare online vs. in-store channel performance

---

## 🔢 Key Metrics at a Glance

| Metric | Value |
|---|---|
| 💰 Total Revenue | ₹60.5 Crore (~$7.26M USD) |
| 📈 Total Profit | ₹3.64 Crore (~$437K USD) |
| 📊 Profit Margin | 6.0% |
| 🛒 Total Orders | 15,000 |
| 🧾 Avg Order Value | ₹40,335 |
| 👤 Unique Customers | 1,000 |
| 📦 Product SKUs | 190 |
| 🏬 Stores | 13 Physical + 1 Online |

---

## 📁 Dataset Structure (Star Schema)

```
📦 Dataset
├── 📄 fact_sales.csv          → 15,000 transactions (central fact table)
├── 📄 dim_product.csv         → 190 products across 7 categories
├── 📄 dim_customer.csv        → 1,000 customers with segments
├── 📄 dim_store.csv           → 13 stores + 1 online platform
├── 📄 dim_order.csv           → Order status and channel details
├── 📄 dim_salesperson.csv     → 80 sales representatives
├── 📄 dim_date.csv            → 731 date records (Jan 2024 – Jan 2026)
├── 📄 dim_payment_method.csv  → 14 payment methods
├── 📄 dim_address.csv         → Address details
├── 📄 dim_city.csv            → City mapping
├── 📄 dim_state.csv           → State mapping
├── 📄 dim_country.csv         → Country reference
├── 📄 verify_data.py          → Data validation script
└── 📄 DAX_Measures.txt        → All Power BI DAX formulas
```

---

## 📊 Dashboard Pages (6 Pages)

1. **Executive Summary** — High-level KPIs, revenue, profit, orders
2. **Sales by Product & Category** — Category-wise performance with margin analysis
3. **Store Performance** — Revenue by store, store type comparison
4. **Channel Analysis** — Online vs. In-Store comparison
5. **Customer Insights** — Segments, LTV, loyalty trends
6. **Time Intelligence** — MoM, YoY growth, seasonal patterns

---

## 💡 Key Insights

- **Mobile Phones** dominate revenue at 36.6% (₹221M) but carry moderate margin (5.6%)
- **Accessories** have the highest margin (29.4%) but lowest revenue — a growth opportunity
- **Online channel** drives 69.5% of orders with lower AOV (₹39,371)
- **In-Store** has 8.5% higher AOV (₹42,716) — better for premium products
- **October 2024** was the peak month (784 orders, ₹30.5M) driven by Diwali festival
- **75.7% delivery rate** with a low 1.9% return rate — strong operational efficiency
- Average customer places **15 orders** — exceptional loyalty metric

---

## 🏬 Top Performing Stores

| Rank | Store | Revenue |
|------|-------|---------|
| 🥇 | Mumbai Inorbit Mall | ₹16.9M |
| 🥈 | Delhi Saket | ₹16.6M |
| 🥉 | Bengaluru Orion Flagship | ₹16.3M |

> 🌐 Online Store alone accounts for **₹420M (71% of total revenue)**

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black) | Dashboard & Visualization |
| DAX | Custom measures & calculations |
| Star Schema | Data modeling |
| CSV / Python | Data storage & validation |
| SQL | Data querying (optional) |

---

## ⚡ Getting Started

### Power BI Users

```
1. Clone/download this repository
2. Open Power BI Desktop
3. Import all CSV files from the /data folder
4. Set up relationships using the star schema diagram
5. Import DAX measures from DAX_Measures.txt
6. Build your visualizations!
```

### Python Users

```python
import pandas as pd

# Load core tables
fact_sales = pd.read_csv('fact_sales.csv')
dim_product = pd.read_csv('dim_product.csv')
dim_customer = pd.read_csv('dim_customer.csv')

# Merge and analyze
sales_data = fact_sales.merge(dim_product, on='product_id')
revenue_by_category = sales_data.groupby('category')['line_total'].sum().sort_values(ascending=False)
print(revenue_by_category)
```

---

## 📐 DAX Measures Included

- Total Revenue, Total Profit, Profit Margin %
- Average Order Value, Revenue per Customer
- YoY Growth %, MoM Growth %
- Rolling 3-Month Average
- Year-to-Date Revenue
- Customer Lifetime Value
- Order Fulfillment Rate, Return Rate, Cancellation Rate
- And 10+ more...

---

## ✅ Data Quality

| Check | Status |
|-------|--------|
| Missing values in critical fields | ✅ None |
| Date continuity | ✅ Verified |
| Referential integrity (FK checks) | ✅ Passed |
| Financial accuracy | ✅ Verified |
| Logical consistency (margins) | ✅ Within range |

---

## 📅 Dataset Info

| Property | Value |
|----------|-------|
| Date Range | Jan 12, 2024 – Jan 11, 2026 |
| Records | 15,000 transactions |
| Currency | Indian Rupees (₹) |
| Format | CSV, UTF-8 |
| Schema | Star Schema |
| Complexity | Intermediate – Advanced |

---

## 🤝 Connect With Me

| Platform | Link |
|----------|------|
| 📊 Kaggle | https://www.kaggle.com/datasets/mayur2303/ |
| 💼 LinkedIn | https://www.linkedin.com/in/sd-mmendhule/ |
| 🐙 GitHub | https://github.com/mayurmendhule/ |
| 📧 Email | mayurmendhule03@gmail.com |

---

## 📄 License

This project is licensed under **CC BY-NC-SA 4.0** (Attribution-NonCommercial-ShareAlike).  
All data is **synthetic** and created for educational/portfolio purposes only.

---

> ⭐ If you found this useful, please **star this repo** and share your dashboard screenshots!  
> 💬 Open an issue or discussion if you have questions or suggestions.
