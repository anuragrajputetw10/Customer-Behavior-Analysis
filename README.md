# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analysis project exploring shopping behavior across **3,900 customer transactions** — combining **Python** for data cleaning and EDA, **SQL (MySQL)** for structured business-question analysis, and **Power BI** for interactive visualization.

---

## 📌 Project Overview

This project analyzes customer shopping behavior using transactional data to uncover insights into:

- Spending patterns across gender, age, and category
- Customer segmentation (New, Returning, Loyal)
- Product preferences and ratings
- Discount dependency and pricing sensitivity
- Subscription behavior and its impact on revenue

The goal is to translate raw transactional data into **actionable business recommendations**.

---

## 🗂️ Dataset Summary

| Attribute | Details |
|---|---|
| Rows | 3,900 |
| Columns | 18 |
| Missing Data | 37 values in `Review Rating` (imputed using category median) |

**Key features:**
- **Customer demographics:** Age, Gender, Location, Subscription Status
- **Purchase details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

---

## 🛠️ Tools & Tech Stack

- **Python** (pandas) — data loading, cleaning, feature engineering
- **MySQL** — SQL-based business analysis
- **Power BI** — interactive dashboard for visual storytelling

---

## 🔍 Exploratory Data Analysis (Python)

- Loaded and profiled the dataset with `df.info()` and `.describe()`
- Imputed missing `Review Rating` values using the **median rating per product category**
- Standardized all column names to `snake_case`
- **Feature engineering:**
  - Created an `age_group` column by binning customer ages
  - Created a `purchase_frequency_days` column from purchase data
- Verified `discount_applied` and `promo_code_used` for redundancy and dropped the duplicate column
- Loaded the cleaned dataset into PostgreSQL for SQL-based analysis

---

## 🧮 SQL Analysis — Business Questions Answered

| # | Business Question |
|---|---|
| 1 | Revenue by gender |
| 2 | High-spending customers who still used discounts |
| 3 | Top 5 products by average review rating |
| 4 | Standard vs. Express shipping — average purchase amount |
| 5 | Subscribers vs. non-subscribers — spend and revenue |
| 6 | Products most dependent on discounts |
| 7 | Customer segmentation — New / Returning / Loyal |
| 8 | Top 3 products per category |
| 9 | Repeat buyers vs. subscription likelihood |
| 10 | Revenue contribution by age group |

### Key Findings
- 👕 **Male customers** generated **$157,890** in revenue vs. **$75,191** from female customers
- 💳 **Non-subscribers** contributed far more total revenue (**$170,436**) than subscribers (**$62,645**) — though average order value is nearly identical (~$59–60)
- 🏆 **Loyal customers** make up 80% of the customer base (3,116 of 3,900)
- ⭐ Top-rated products (Gloves, Sandals, Boots, Hat, Skirt) all cluster tightly between 3.78–3.86 average rating
- 🏷️ Hats, Sneakers, Coats, Sweaters, and Pants are the most **discount-dependent** products (~47–50% of purchases involve a discount)
- 🎂 Revenue is fairly even across age groups, with **Young Adults** slightly ahead ($62,143)

---

## 📊 Dashboard (Power BI)

An interactive Power BI dashboard was built to explore the data visually, with filters for:
- Subscription Status
- Gender
- Category
- Shipping Type

**Dashboard highlights:**
- 3.9K customers | $59.76 average purchase amount | 3.75 average review rating
- Revenue & sales breakdowns by category and age group
- Subscriber vs. non-subscriber distribution

---

## 💡 Business Recommendations

- **Boost Subscriptions** — Promote exclusive benefits to convert high-frequency shoppers into subscribers
- **Customer Loyalty Programs** — Reward repeat buyers to move them into the "Loyal" segment
- **Review Discount Policy** — Balance sales boosts with margin control on discount-heavy products
- **Product Positioning** — Highlight top-rated and best-selling products in campaigns
- **Targeted Marketing** — Focus efforts on high-revenue age groups and express-shipping users

---

## 📁 Repository Structure

```
├── data/                # Raw and cleaned dataset (if included)
├── notebooks/           # Python EDA & cleaning notebooks
├── sql/                 # SQL queries for business analysis
├── dashboard/           # Power BI dashboard file (.pbix)
├── Customer_Shopping_Behavior_Analysis.pdf   # Project summary report
└── README.md
```

---

## 🚀 How to Reproduce

1. Clone this repository
   ```bash
   git clone https://github.com/anuragrajputetw10/customer-shopping-behavior-analysis.git
   ```
2. Install dependencies
   ```bash
   pip install pandas psycopg2-binary
   ```
3. Run the Python notebook to clean the data and load it into PostgreSQL
4. Execute the SQL scripts in `sql/` against your PostgreSQL instance
5. Open the `.pbix` file in Power BI Desktop to explore the dashboard

---

## 👤 Author

**Anurag Rajput**
GitHub: [@anuragrajputetw10](https://github.com/anuragrajputetw10)

---

⭐ If you found this project useful, consider giving it a star on GitHub!
