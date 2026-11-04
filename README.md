# Superstore Sales Data Exploration (SQL)

## Project Overview

This project explores Superstore sales data using **SQL** to answer business-oriented questions about customer performance, sales trends, product performance, profitability, and target achievement.

The objective is to demonstrate practical SQL skills by transforming raw relational data into insights that can support business decision-making.

## Business Questions

The analysis addresses the following 10 questions:

1. **Top 10 Customers:** Identify the top 10 customers by total sales.
2. **Monthly Sales Trends:** Calculate total sales for each month in 2023.
3. **Unsold Products:** Find products that have never been sold.
4. **New Customer Acquisition:** Count customers whose first order was placed in 2022.
5. **Profit Margin by Category:** Calculate the profit margin percentage for each product category.
6. **Daily Sales and Running Totals:** Show date-wise sales and cumulative sales for each category.
7. **Most Recent Customer Orders:** Retrieve each customer's most recent order.
8. **Customer Segmentation:** Classify customers into Platinum, Gold, Silver, and Bronze segments based on total sales.
9. **Best-Selling Product by Category:** Identify the product with the highest total sales in each category, including ties.
10. **Actual vs. Target Sales:** Compare actual sales with target sales by category and year.

## Database Tables

The SQL script references the following tables:

| Table | Purpose |
|---|---|
| `Customer` | Customer details, including customer ID and name |
| `Products` | Product details and category information |
| `Shipping` | Shipping-related information |
| `Sales` | Order-level sales data, including customer, product, date, price, and profit |
| `TargetSales` | Annual sales targets by product category |

> Note: The project script assumes these tables and their columns already exist in the SQL Server database. The dataset or table-creation scripts are not included in this repository unless added separately.

## SQL Skills Demonstrated

- **Joins:** `INNER JOIN`, `LEFT JOIN`
- **Aggregations:** `SUM()`, `COUNT()`, `MIN()`, `MAX()`
- **Grouping and Sorting:** `GROUP BY`, `ORDER BY`
- **Common Table Expressions:** `WITH` (CTEs)
- **Window Functions:** `RANK()`, `SUM() OVER()`
- **Conditional Logic:** `CASE WHEN`
- **Date Functions:** `YEAR()`, `MONTH()`, `DATEFROMPARTS()`
- **Data Transformation:** `UNPIVOT`, `REPLACE()`
- **Subqueries:** Derived tables and nested queries
- **Data Type Conversion:** `CAST()`

## Project Structure

```text
Superstore-Sales-Data-Exploration/
│
├── SuperstoreSales_DataExploration.sql
└── README.md
```

## Tools Used

- SQL

## How to Run the Project

1. Set up a SQL environment.
2. Load the Superstore dataset into your SQL Server database.
3. Ensure the database contains the five tables referenced in the SQL script:
   `Customer`, `Products`, `Shipping`, `Sales`, and `TargetSales`.
4. Open `SuperstoreSales_DataExploration.sql` in your SQL editor.
5. Select the appropriate database context.
6. Execute the queries to explore the analysis.

## Notes and Assumptions

- The project uses SQL queries to explore and analyse the dataset.
- `Sales.Price` is treated as the sales amount in the calculations.
- Profit margin is calculated as total profit divided by total sales, multiplied by 100.
- New customers are identified using their earliest recorded order date in the available sales data.
- The most recent order query can return multiple orders if a customer has multiple orders on the same latest date.
- The actual-versus-target analysis uses the annual target columns for 2020–2023.

## Author

**Anant Singhal**

---

*This project is part of my hands-on SQL practice and portfolio development, focused on solving practical business problems through data analysis.*
