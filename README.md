<h1 align="center">🛍️ Customer Behavior Analysis</h1>

<p align="center">
An end-to-end data analytics project uncovering customer shopping behavior, spending patterns, and revenue drivers from 3,900 retail transactions.
</p>

<p align="center">
<img src="https://img.shields.io/badge/Python-pandas-3776AB?logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/Dashboard-Power%20BI-F2C811?logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/Report-PowerPoint-B7472A?logo=microsoftpowerpoint&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Completed-2E8B57" />
</p>

---

## 📌 Overview

This project analyzes **customer shopping behavior** using transactional data from **3,900 purchases** across multiple product categories. The objective is to uncover meaningful insights into spending patterns, customer segments, product preferences, and subscription behavior — turning raw data into **actionable business recommendations**.

The project follows the complete analytics lifecycle:

<p align="center">
<b>Data Loading → EDA → Data Cleaning → SQL Analysis → Power BI Dashboard → Business Report</b>
</p>

---

## 📁 Project Files

| File | Description |
|---|---|
| 📊 [`customer_shopping_behavior.csv`](customer_shopping_behavior.csv) | Cleaned dataset used for analysis |
| 🗄️ [`customer_behavior_sql.sql`](customer_behavior_sql.sql) | SQL queries used for business analysis in MySQL |
| 📈 [`customer_behavior_dashboard.pbix`](customer_behavior_dashboard.pbix) | Interactive Power BI dashboard file |
| 🖼️ [`powerbi_dashboard.png`](powerbi_dashboard.png) | Dashboard preview image |
| 📄 [`Customer_Shopping_Behavior_Analysis_pptx.pptx`](Customer_Shopping_Behavior_Analysis_pptx.pptx) | Final project report & presentation |

---

## 🗂️ Dataset

| Detail | Description |
|---|---|
| **Records** | 3,900 customer transactions |
| **Columns** | 18 |
| **Demographics** | Age, Gender, Location, Subscription Status |
| **Purchase Details** | Item Purchased, Category, Purchase Amount, Season, Size, Color |
| **Shopping Behavior** | Discount Applied, Promo Code Used, Previous Purchases, Purchase Frequency, Review Rating, Shipping Type |
| **Data Quality Issue** | 37 missing values in Review Rating — imputed using category-wise median |

📄 Full dataset: [`customer_shopping_behavior.csv`](customer_shopping_behavior.csv)

---

## 🛠️ Tools & Technologies

| Stage | Tool / Technology |
|---|---|
| 🐍 Data Loading & Cleaning | Python (pandas) |
| 📊 Exploratory Data Analysis | Python (pandas, matplotlib, seaborn) |
| 🗄️ Database & Querying | MySQL Server |
| 📈 Dashboarding | Power BI |
| 📄 Reporting | Microsoft PowerPoint |

---

## 🔍 Project Workflow

### 1️⃣ Data Loading
Imported the raw dataset into Python using `pandas` and performed an initial structural check.

### 2️⃣ Exploratory Data Analysis (EDA)
Used `df.info()` and `.describe()` to understand data types, distributions, and summary statistics across all 18 columns.

### 3️⃣ Data Cleaning & Feature Engineering
- Identified and handled 37 missing values in **Review Rating** (imputed with category-wise median)
- Standardized all column names to `snake_case` for consistency
- Engineered new features: **`age_group`** (binned age ranges) and **`purchase_frequency_days`**
- Detected redundancy between `discount_applied` and `promo_code_used`, and dropped the redundant column
- Final cleaned dataset: [`customer_shopping_behavior.csv`](customer_shopping_behavior.csv)

### 4️⃣ Database Integration
Loaded the cleaned dataset into **MySQL Server**, enabling structured, query-based analysis.

### 5️⃣ SQL-Based Business Analysis
Wrote targeted SQL queries — see the full file: [`customer_behavior_sql.sql`](customer_behavior_sql.sql)

| # | Business Question |
|---|---|
| 1 | Revenue comparison by gender |
| 2 | High-spending customers who used discounts |
| 3 | Top 5 products by average review rating |
| 4 | Shipping type comparison (Standard vs. Express) |
| 5 | Subscribers vs. non-subscribers — spend & revenue |
| 6 | Products most dependent on discounts |
| 7 | Customer segmentation — New, Returning, Loyal |
| 8 | Top 3 best-selling products per category |
| 9 | Repeat buyers vs. subscription status |
| 10 | Revenue contribution by age group |

### 6️⃣ Dashboard Design
Designed an interactive **Power BI dashboard** consolidating all insights into a single, filterable, business-ready view.
📈 Dashboard file: [`customer_behavior_dashboard.pbix`](customer_behavior_dashboard.pbix)

### 7️⃣ Reporting
Compiled the full analysis into a polished PowerPoint report, complete with visuals and strategic business recommendations.
📄 Full report: [`Customer_Shopping_Behavior_Analysis_pptx.pptx`](Customer_Shopping_Behavior_Analysis_pptx.pptx)

---

## 📊 Power BI Dashboard

An interactive dashboard was built to present the insights visually for business stakeholders, with filters for **subscription status, gender, category, shipping type, and payment method**.

![Power BI Dashboard](powerbi_dashboard.png)

🔗 Open the live file: [`customer_behavior_dashboard.pbix`](customer_behavior_dashboard.pbix)

### Dashboard Highlights
| Metric | Value |
|---|---|
| Total Customers | **3.9K** |
| Average Rating | **3.75 / 5** |
| Average Purchase Amount | **$59.76** |
| Average Previous Purchases | **25.35** |
| Top Revenue Category | Clothing (**$104K**) |
| Non-Subscriber Share | **73%** of customer base |
| Top Revenue Age Group | Young Adults |

---

## 📈 Results & Key Insights

| Insight | Finding |
|---|---|
| **Revenue by Gender** | Male customers generated ~2.1x more revenue than female customers ($157,890 vs. $75,191) |
| **Discount-Driven High Spenders** | 839 customers used a discount but still spent above the average purchase amount |
| **Top-Rated Products** | Gloves, Sandals, Boots, Hat, and Skirt lead in average review ratings |
| **Shipping Impact** | Express shipping customers spend slightly more on average ($60.48) vs. Standard ($58.46) |
| **Subscription Behavior** | Non-subscribers drive ~73% of total revenue purely through volume; average spend per customer is nearly identical across both groups |
| **Discount Dependency** | Hat, Sneakers, Coat, Sweater, and Pants rely on discounts for 47–50% of their purchases |
| **Customer Segments** | 80% of customers fall into the "Loyal" segment, showing strong repeat-purchase behavior |
| **Revenue by Age** | Young Adults contribute the highest revenue ($62,143), followed by Middle-aged, Adult, and Senior groups |

---

## 💡 Business Recommendations

- 🎯 **Boost Subscriptions** — Promote exclusive subscriber-only benefits to grow this segment
- 🏆 **Loyalty Programs** — Reward repeat buyers to convert Returning customers into Loyal customers
- 💰 **Review Discount Policy** — Balance promotional sales boosts with margin protection on high-discount-dependency items
- 📢 **Product Positioning** — Feature top-rated and best-selling products prominently in marketing campaigns
- 🎯 **Targeted Marketing** — Focus campaigns on high-revenue age groups and Express-shipping customers

---

## 👤 Author

**Dheeraj Gupta**

<p align="center">⭐ If you found this project useful, consider giving it a star!</p>
