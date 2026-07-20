# Risk_Analysis_Project
This project focuses on analyzing credit risk using customer financial data to identify factors that influence loan repayment behaviour and classify customers into different risk categories.
German Credit Risk Analysis — SQL & Excel
A credit risk analysis project on the German Credit dataset, combining SQL for querying and business-rule-based risk segmentation with Excel Pivot Tables for summary reporting. Built to answer the kind of questions a bank or lending team would ask when evaluating loan default risk.
📌 Business Problem
Lenders need to understand which customer segments (loan purpose, age group, employment status, housing type) carry the highest risk of default, so that credit policy and approval thresholds can be adjusted accordingly.
This project analyzes 1,000 loan applicants to answer:
Which loan purposes and customer segments have the highest default rates?
How does risk vary by age, employment history, and housing status?
What distinguishes "Good" credit customers from "Bad" credit customers?
🗂️ Repository Structure
```
├── README.md
├── data/
│   └── german_credit_pivot.xlsx     # Raw data + Excel pivot table analysis
└── sql/
    ├── queries.sql                  # Plain SQL file (5 queries + bonus risk-score query)
    └── SQL_Queries.docx             # Formatted write-up with business context per query
```
🛠️ Tools Used
SQL (PostgreSQL/MySQL syntax) — aggregation, CASE WHEN logic, subqueries, window functions
Microsoft Excel — Pivot Tables for cross-tab summaries and quick reporting
🔍 Key Insights
Analysis	Finding
Overall portfolio	700 Good / 300 Bad credit customers (70% / 30%)
Average loan amount	Bad credit customers borrow more on average (₹3,938 vs ₹2,985 for Good)
Age risk	18–25 age group has the highest default rate (~42%), 60+ the lowest (~22%)
Loan purpose	Car (New) and Education loans show the highest default rates among high-volume categories
Housing	Renters default at a higher rate (~39%) than homeowners (~26%)
(Full breakdown available in the pivot tables and SQL query outputs.)
📊 Excel Pivot Analysis (`data/german_credit_pivot.xlsx`)
The workbook contains the raw dataset plus six pivot-table sheets:
Good vs Bad Credit — overall split
Credit Risk by Age Group
Loan Purpose by Credit Status
Average Loan Amount by Credit Status
Employment History vs Credit Status
Housing vs Credit Status
🧮 SQL Queries (`sql/queries.sql`)
Top 5 Highest-Risk Loan Purposes — default rate by purpose, filtered for statistical relevance (`HAVING COUNT(*) >= 10`)
Risk Profile by Age Group and Employment — multi-dimensional segmentation
Rank Customer Segments by Average Loan Amount — `DENSE_RANK()` window function
High-Risk Customers with Above-Average Loans — correlated subquery filtering
Credit Risk Summary Dashboard Query — KPI comparison between Good vs Bad customers
Bonus: Composite Risk Score — multi-condition `CASE WHEN` risk classification (Low / Medium / High / Very High)
▶️ How to Use
Load the dataset into a table named `credit_data` in PostgreSQL/MySQL (matching columns used in the queries).
Run `sql/queries.sql` to reproduce the analysis.
Open `data/german_credit_pivot.xlsx` to explore the same insights via pivot tables.
👤 Author
Atharv Bhosale
LinkedIn · GitHub
