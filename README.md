# 🛒 Retail Supply Chain Management Analysis

## 📌 Problem Statement

Retail businesses often struggle to balance **sales growth, profitability, and inventory efficiency**.
This project analyzes retail supply chain data to uncover actionable insights that improve decision-making across sales, operations, and inventory management.

---

## 🎯 Objectives

* Analyze sales and profit performance
* Understand the impact of discounts on profitability
* Identify time-based trends (monthly, weekly, quarterly)
* Evaluate inventory efficiency
* Provide data-driven business recommendations

---

## 📊 Dashboard Overview

![Dashboard](images/dashboard.png)

---

## 📈 Key Metrics

| Metric              | Value   |
| ------------------- | ------- |
| Total Sales         | $32.03K |
| Total Profit        | $3.43K  |
| Profit Margin       | 11%     |
| Total Quantity Sold | 0.59K   |

---

# 🔍 Exploratory Data Analysis (EDA)

### 📊 Sales Distribution

* Sales are unevenly distributed across months
* High concentration in **Aug–Sep**

👉 **Insight:** Demand is seasonal and influenced by external factors (promotions, holidays)

---

### 💰 Profit vs Discount Analysis

* Discounts increased by **+48.6%**
* Profit showed **+54.3% variation**

👉 **Insight:**
Discounts strongly influence profit, but not always positively
→ Suggests **diminishing returns on high discounts**

---

### 📅 Time Series Analysis

#### Monthly Trend

* Peak: **Aug & Sep (~$10K)**
* Low: **July (~$1K)**

#### Weekly Trend

* Best day: **Monday ($17K)**
* Worst day: **Wednesday ($3K)**

👉 **Insight:**

* Early-week demand spike
* Mid-week performance drop

---

### 📦 Inventory Analysis

* Very low remaining inventory

👉 **Insight:**

* Efficient inventory turnover
* Risk of **stockouts during high demand periods**

---

### 📊 Quarterly Trends

| Quarter | Profit  | Contribution |
| ------- | ------- | ------------ |
| Q1      | $12.57K | 20%          |
| Q2      | $13.70K | 22%          |
| Q3      | $20.71K | 34%          |
| Q4      | $14.63K | 24%          |

👉 **Insight:**
Q3 dominates → peak season for business operations

---

### 🌍 Geographic Analysis

* Sales distributed across multiple states

👉 **Insight:**

* No over-dependence on a single region
* Indicates diversified market presence

---

# 🔍 Key Insights Summary

* Profit margin is relatively low (**11%**)
* Discounts heavily impact profitability
* Strong seasonal trends (Q3 peak)
* Weekly demand imbalance (Mon vs Wed)
* Inventory is efficient but may be too lean

---

# 💡 Business Recommendations

### 1. Discount Optimization

* Avoid excessive discounting
* Identify optimal discount threshold to maximize profit

---

### 2. Inventory Planning

* Increase stock before **Q3 and peak months (Aug–Sep)**
* Implement demand forecasting

---

### 3. Sales Strategy

* Launch **mid-week promotions (Wednesday)**
* Balance weekly demand

---

### 4. Seasonal Strategy

* Analyze Q3 success drivers
* Replicate strategies in other quarters

---

### 5. Data Strategy

* Implement predictive analytics
* Improve data collection for deeper insights

---

# ⚠️ Limitations

* Dataset size is relatively small (~$32K sales)
* No customer-level data for segmentation
* Limited cost breakdown (no operational cost visibility)
* No real-time data integration
* External factors (market trends, competition) not included

---

# 🧠 Business Case

### Objective

Improve retail supply chain efficiency and profitability through analytics.

### Key Questions

* How do discounts affect profitability?
* When should inventory be increased?
* Which periods drive the most revenue?
* Are we operating efficiently?

### Stakeholders

* Supply Chain Managers
* Sales Teams
* Finance Teams

### Expected Outcomes

* Improved margins
* Better stock planning
* Optimized promotions

---

# 🛠 Tools & Technologies

* **Power BI** – Dashboard development
* **DAX** – Measures and calculations
* **Excel / CSV** – Data source

---

# 🧱 Data Modeling

* Star schema used

**Fact Table:**

* Sales

**Dimension Tables:**

* Date
* Product
* Location

---

# 📊 Key DAX Measures

```DAX id="q2mzj1"
Total Sales = SUM(Sales[Sales])

Total Profit = SUM(Sales[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Total Quantity = SUM(Sales[Quantity])
```

---

# 📘 Data Dictionary

| Column Name | Description       |
| ----------- | ----------------- |
| Order ID    | Unique identifier |
| Product     | Product name      |
| Sales       | Revenue           |
| Profit      | Profit            |
| Discount    | Discount applied  |
| Quantity    | Units sold        |
| Date        | Order date        |
| State       | Customer location |

---

# 📂 Project Structure

```id="7z2w9k"
retail-supply-chain-analysis/
│
├── data/
│   ├── raw_data.csv
│   └── cleaned_data.csv
│
├── dashboard/
│   └── Retail_Supply_Chain.pbix
│
├── images/
│   └── dashboard.png
│
├── docs/
│   ├── business_case.md
│   ├── data_dictionary.md
│   └── dax_measures.md
│
├── notebooks/
│   └── exploratory_analysis.ipynb
│
├── README.md
└── requirements.txt
```

---

# 🚀 How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Interact with filters (Year, Month, State)

---

# 🔮 Future Improvements

* Add forecasting models (time series)
* Customer segmentation (RFM analysis)
* SQL-based data pipeline
* Real-time dashboard deployment

---

# 👤 Author

**Your Name**

* LinkedIn: (Add link)
* Portfolio: (Add link)

---
