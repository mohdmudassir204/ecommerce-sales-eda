# E-Commerce Sales — Exploratory Data Analysis

## 📌 Project Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) on a synthetic e-commerce sales dataset.

The goal is to understand sales and profitability patterns, identify relationships between business variables, detect data-quality issues, and extract meaningful business insights from raw transactional data.

This project was completed as part of my hands-on journey in learning Exploratory Data Analysis and data analytics with Python.

---

## 🎯 Objectives

The main objectives of this analysis were to:

- Understand the structure and characteristics of the dataset
- Identify missing values and duplicate records
- Analyze numerical and categorical variables
- Investigate sales and profit across product categories
- Analyze the effect of discounts on profitability
- Compare sales and profit across regions
- Analyze monthly sales trends
- Study the relationship between sales and profit
- Identify loss-making orders
- Clean the dataset appropriately
- Extract actionable business insights

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- GitHub

---

## 📊 Dataset

The dataset contains **1,208 records and 14 columns** before cleaning.

### Main Features

| Column | Description |
|---|---|
| Order_ID | Unique order identifier |
| Order_Date | Date when the order was placed |
| Ship_Date | Date when the order was shipped |
| Customer | Customer name |
| Region | Sales region |
| Category | Product category |
| Product | Product name |
| Quantity | Number of units ordered |
| Unit_Price | Price per unit |
| Discount | Discount applied to the order |
| Sales | Final sales value |
| Cost | Cost associated with the order |
| Profit | Profit generated from the order |
| Shipping_Mode | Shipping method |

The dataset is synthetic and was created specifically for practicing EDA.

---

## 🔍 Exploratory Data Analysis

The analysis covered:

### 1. Data Understanding

- Dataset dimensions
- Data types
- Statistical summary
- Numerical and categorical variables
- Date columns

### 2. Data Quality

The raw dataset contained:

- **8 duplicate rows**
- **35 missing values**

Missing values were found in:

- Customer
- Region
- Discount
- Shipping_Mode

The duplicate records were removed, and missing categorical values were handled using the mode while missing discount values were handled using the median.

---

## 📈 Key Findings

### Category Analysis

Electronics generated the highest average profit:

| Category | Average Profit |
|---|---:|
| Electronics | $177.11 |
| Furniture | $136.46 |
| Accessories | $42.07 |
| Office Supplies | $19.54 |

However, Electronics also showed the highest variability in profit.

Furniture had the highest median profit, showing that average and median can tell different stories about a dataset.

---

### Profit Margin

The overall profit margins were:

| Category | Profit Margin |
|---|---:|
| Office Supplies | 36.54% |
| Accessories | 31.54% |
| Furniture | 20.63% |
| Electronics | 13.14% |

This shows that the category generating the highest average profit does not necessarily have the highest profit margin.

---

### Discount & Profit

A strong relationship was observed between discount level and average profit:

| Discount | Average Profit |
|---|---:|
| 0% | $163.65 |
| 5% | $111.77 |
| 10% | $99.45 |
| 15% | $62.73 |
| 20% | $28.87 |
| 30% | -$51.82 |

All observed loss-making orders occurred at the **30% discount level**.

This suggests that higher discounts are associated with substantially lower profitability in this dataset.

---

### Regional Analysis

North recorded the highest total sales and the highest average sales per order.

North also had the highest average profit among the regions.

---

### Sales & Profit Relationship

The correlation between Sales and Profit was:

**0.81**

This indicates a strong positive relationship between sales and profit in the dataset.

A scatter plot was also used to visually examine this relationship.

---

### Time Analysis

Monthly sales were analyzed across 2024 and 2025.

The highest monthly sales occurred in **June 2024**.

Although sales fluctuated considerably from month to month, there was no consistent overall upward or downward trend across the two-year period.

---

## 🧹 Data Cleaning

The following cleaning steps were performed:

1. Identified duplicate records
2. Removed 8 exact duplicate rows
3. Identified missing values
4. Filled categorical missing values using the mode
5. Filled missing discount values using the median
6. Verified that no missing values remained
7. Verified that no duplicate records remained

Importantly, negative-profit orders were **not removed**, because they represent valid business outcomes rather than automatically being treated as data errors.

---

## 📌 Business Insights

The analysis produced several important observations:

1. Electronics generates the highest average profit but has the lowest profit margin among the categories.
2. Furniture has the highest median profit.
3. Electronics has the greatest variability in profit.
4. Office Supplies has the highest profit margin despite having the lowest average profit.
5. North has the highest total sales and average sales per order.
6. Sales and profit have a strong positive correlation.
7. Higher discount levels are associated with lower average profit.
8. The 30% discount level is associated with negative average profit and contains all observed loss-making orders.
9. Monthly sales fluctuate considerably without a consistent long-term trend.

---

## 📚 What I Learned

Through this project, I practiced:

- Data inspection with Pandas
- Descriptive statistics
- Missing-value analysis
- Duplicate detection
- Categorical analysis
- GroupBy operations
- Mean vs. median interpretation
- Standard deviation and variability
- Correlation analysis
- Box plots
- Scatter plots
- Time-series exploration
- Data cleaning
- Business-oriented interpretation of EDA results

The main focus was not just writing Python code, but learning how to turn analytical results into meaningful business insights.

---

## 🚀 Future Improvements

Potential extensions to this project include:

- Building an interactive dashboard using Power BI or Tableau
- Performing deeper customer-level analysis
- Performing product-level profitability analysis
- Investigating shipping performance
- Creating sales and profit forecasting models
- Performing statistical hypothesis testing
- Building a predictive model for profit

---

## 📁 Project Structure

```text
ecommerce-sales-eda/
│
├── data/
│   └── project_2_ecommerce_sales.csv
│
├── notebook/
│   └── ecommerce_sales_eda.ipynb
│
├── README.md
└── requirements.txt
