# 🛍️ Customer Shopping Behavior Analysis

> An end-to-end data analytics project analyzing customer shopping behavior using transactional retail data — covering data cleaning, feature engineering, SQL-based business analysis, customer segmentation, and interactive Power BI dashboard development.

---

## 📋 Project Overview

This project performs a comprehensive analysis of **3,900 customer transactions** across multiple product categories to uncover actionable insights into:

- 💰 Spending patterns and revenue drivers
- 👥 Customer segmentation (New, Returning, Loyal)
- 🏷️ Discount & promotion behavior
- 📦 Product and category performance
- 🔄 Subscription vs. non-subscription trends

The goal is to help businesses make **data-driven decisions** around marketing, retention, and product strategy.

---

## 📊 Dataset Summary

| Attribute | Details |
|---|---|
| **Total Records** | 3,900 transactions |
| **Total Features** | 18 columns |
| **Missing Data** | 37 values in `Review Rating` column |
| **Source** | Publicly available retail dataset |

**Key Features:**

| Category | Features |
|---|---|
| Customer Demographics | Age, Gender, Location, Subscription Status |
| Purchase Details | Item Purchased, Category, Purchase Amount (USD), Season, Size, Color |
| Shopping Behavior | Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python (Pandas, NumPy)** | Data cleaning, feature engineering, EDA |
| **Matplotlib & Seaborn** | Exploratory visualizations |
| **PostgreSQL** | Relational database & SQL business analysis |
| **Power BI** | Interactive dashboard & KPI reporting |

---

## 🔄 Project Workflow

```
Raw Dataset
    │
    ▼
Python (Pandas) — Data Cleaning & Feature Engineering
    │
    ▼
PostgreSQL — Database Integration & SQL Analysis
    │
    ▼
Power BI — Interactive Dashboard & Business Insights
```

---

## 🐍 Exploratory Data Analysis (Python)

### Data Cleaning & Preprocessing

- **Data Loading** — Imported dataset using `pandas`; used `.info()` and `.describe()` for initial exploration
- **Missing Value Handling** — Imputed 37 missing values in `Review Rating` using **median rating per product category** (robust to outliers)
- **Column Standardization** — Renamed all columns to `snake_case` for consistency
- **Redundancy Check** — Verified `discount_applied` and `promo_code_used` were redundant; dropped `promo_code_used`

### Feature Engineering

| New Feature | Description |
|---|---|
| `age_group` | Binned customer ages into Young Adult, Adult, Middle-aged, Senior |
| `purchase_frequency_days` | Derived from purchase frequency field for numerical analysis |

### Customer Segmentation Logic

Customers classified into 3 segments based on purchase history:

| Segment | Criteria |
|---|---|
| **New** | 0–1 previous purchases |
| **Returning** | 2–5 previous purchases |
| **Loyal** | 6+ previous purchases |

---

## 🗄️ SQL Business Analysis (PostgreSQL)

Cleaned data was loaded into PostgreSQL and **10 business questions** were answered using SQL:

| # | Business Question | Key Finding |
|---|---|---|
| 1 | Revenue by Gender | Male: $157,890 \| Female: $75,191 |
| 2 | High-Spending Discount Users | 839 customers spent above average even with discounts |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 4 | Shipping Type Comparison | Express ($60.48) vs Standard ($58.46) avg spend |
| 5 | Subscribers vs Non-Subscribers | 1,053 subscribers \| 2,847 non-subscribers |
| 6 | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| 7 | Customer Segmentation | Loyal: 3,116 \| Returning: 701 \| New: 83 |
| 8 | Top 3 Products per Category | Jewelry, Blouse, Sandals, Jacket top their categories |
| 9 | Repeat Buyers & Subscriptions | 2,518 repeat buyers are non-subscribers (retention opportunity) |
| 10 | Revenue by Age Group | Young Adults lead at $62,143 |

---

## 📊 Power BI Dashboard

An interactive dashboard was built with the following components:

**KPI Cards:**
- 3.9K Total Customers
- $59.76 Average Purchase Amount
- 3.75 Average Review Rating

**Visualizations:**
- % of Customers by Subscription Status (Donut Chart)
- Revenue by Category (Bar Chart)
- Sales by Category (Bar Chart)
- Revenue by Age Group (Horizontal Bar)
- Sales by Age Group (Horizontal Bar)

**Slicers / Filters:**
- Subscription Status, Gender, Category, Shipping Type

### Dashboard Preview



---

## 💡 Key Insights

- 🏆 **80% of customers are Loyal** — strong retention base exists
- 👦 **Young Adults drive the most revenue** at $62,143+
- 🏷️ **73% customers are non-subscribers** — large untapped subscription opportunity
- 🎩 **Hat has highest discount dependency** at 50% — margin risk
- 💳 **839 high-value discount users** still spend above average — these are prime loyalty targets
- 🚚 **Express shipping users spend more** ($60.48 vs $58.46) — premium segment indicator

---

## 📢 Business Recommendations

| Recommendation | Rationale |
|---|---|
| **Boost Subscriptions** | 73% non-subscribers; promote exclusive benefits to convert them |
| **Customer Loyalty Programs** | Reward repeat buyers to move them from Returning → Loyal |
| **Review Discount Policy** | Hat, Sneakers, Coat have 48–50% discount rates — balance sales boost with margin |
| **Product Positioning** | Highlight top-rated products (Gloves, Sandals, Boots) in campaigns |
| **Targeted Marketing** | Focus on Young Adults and Express-shipping users — highest revenue segments |

---

## 📁 Project Structure

```
CUSTOMER-SHOPPING-BEHAVIOR-ANALYSIS/
│
├── data/
│   └── shopping_behavior_updated.csv     # Raw dataset
│
├── notebooks/
│   └── customer_shopping_eda.ipynb       # Python EDA & cleaning
│
├── sql/
│   └── business_analysis_queries.sql     # All 10 SQL queries
│
├── dashboard/
│   └── customer_behavior_dashboard.pbix  # Power BI file
│
├── dashboard_screenshot.png              # Dashboard preview
└── README.md
```

---

## 🙋‍♂️ Author

**Ravi Prakash Chaudhary**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/ravi-chaudhary-8ab3a1233/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/ravichaudhary-code)

---

⭐ **If you found this project helpful, please give it a star!**
