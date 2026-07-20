# German-Credit-Risk-Analysis

A credit risk analysis project on the **German Credit Dataset**, using SQL and Excel to identify patterns in customer credit behavior, loan characteristics, and default risk. The project applies business-rule-based risk segmentation and Excel Pivot Table analysis to answer real-world lending questions and support better credit decisions.

# 📊 German Credit Risk Analysis

## 📌 Project Overview

This project analyzes the German Credit dataset containing **1,000 loan applicants** to understand factors influencing credit risk. 

The analysis focuses on customer segmentation, loan characteristics, and risk patterns using SQL queries and Excel Pivot Tables. Additional features were created, such as age groups, loan categories, loan duration categories, and risk categories, to generate meaningful business insights.

## 🎯 Business Problem

Financial institutions need to identify which customer segments are more likely to default so that lending policies, approval criteria, and risk management strategies can be improved.

This project analyzes:

- Which customer segments have higher default risk?
- How does credit risk vary by age group, employment status, and housing type?
- Which loan purposes contribute to higher risk?
- What differences exist between Good and Bad credit customers?

## 🗂️ Repository Structure

```
├── README.md
├── data/
│   └── german_credit_data.xlsx        # Dataset with feature engineering and Excel analysis
├── sql/
│   └── queries.sql                    # SQL queries for credit risk analysis
└── dashboard/
    └── PowerBI_Dashboard.pbix         # Interactive dashboard (if available)
```

## 🛠️ Tools Used

- **SQL (PostgreSQL/MySQL)**  
  - Data aggregation
  - CASE WHEN logic
  - Subqueries
  - Window functions
  - Risk segmentation

- **Microsoft Excel**
  - Data cleaning
  - Feature engineering
  - Pivot Tables
  - Summary reporting

- **Power BI (Optional)**
  - Interactive dashboard creation
  - Data visualization
  - KPI reporting

## 🔍 Data Preparation & Feature Engineering

The original German Credit dataset was enhanced by creating additional columns:

### 1. Age Group
- Derived from the existing Age column.
- Customers were segmented into different age categories to analyze risk patterns.

### 2. Loan Category
- Derived from the Credit Amount column.
- Loan amounts were categorized into:
  - Small Loan Amount
  - Medium Loan Amount
  - Large Loan Amount

### 3. Loan Duration Category
- Derived from the Loan Duration field.
- Customers were grouped into:
  - Short Duration
  - Medium Duration
  - Long Duration

### 4. Risk Category
- Derived from the Target variable.
- Converted credit status into business-friendly risk labels:
  - Good Credit → Low Risk
  - Bad Credit → High Risk

## 📊 Key Insights

| Analysis | Finding |
|---|---|
| Overall Credit Portfolio | 700 customers have Good credit and 300 customers have Bad credit |
| Loan Amount Analysis | Bad credit customers have a higher average loan amount compared to Good credit customers |
| Age Risk Analysis | Younger customers show higher default risk compared to older age groups |
| Loan Purpose Analysis | Certain loan purposes show higher default rates and require additional evaluation |
| Housing Analysis | Housing type influences customer repayment behavior |

## 📊 Excel Analysis (`data/german_credit_data.xlsx`)

The workbook contains:

- Good vs Bad Credit Analysis
- Credit Risk by Age Group
- Loan Purpose vs Credit Status
- Loan Amount Analysis by Risk Category
- Employment Status vs Credit Risk
- Housing Type vs Credit Risk
- Loan Duration Risk Analysis

## 🧮 SQL Analysis (`sql/queries.sql`)

SQL queries answer business questions such as:

- Identify high-risk loan purposes based on default percentage
- Analyze credit risk by age group and employment status
- Compare average loan amounts between Good and Bad credit customers
- Find high-risk customers with above-average loan amounts
- Create customer risk segmentation using CASE WHEN logic

## ▶️ How to Use

1. Download the German Credit dataset.
2. Load the dataset into a SQL database table named `credit_data`.
3. Run SQL queries from the `/sql` folder.
4. Open the Excel file to explore Pivot Table analysis and insights.

## 👤 Author

**Atharv Bhosale**

LinkedIn: https://www.linkedin.com/in/atharv-bhosale-8b83b8379/
