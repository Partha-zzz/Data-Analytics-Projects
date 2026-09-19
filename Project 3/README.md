# Project 3: SQL Data Analysis

## Problem Statement
Spreadsheets can become slow and hard to query as datasets grow. Organizations need structured relational databases to quickly search, filter, and summarize transaction records. This project demonstrates how to query transactional order data using SQL to uncover basic business insights.

## Objective
The primary objective of this project is to learn and apply fundamental SQL concepts:
- `SELECT` queries to view table data
- `WHERE` clause for data filtering
- `ORDER BY` clause for sorting query results
- `GROUP BY` clause for grouping records
- Aggregate functions: `COUNT()`, `SUM()`, and `AVG()`

## Technologies Used
- **Python**: Core programming language
- **Pandas**: Used only to load the Excel dataset and insert data into SQLite
- **SQLite (`sqlite3`)**: Lightweight relational database engine
- **Jupyter Notebook**: Interactive environment for executing code and queries

## Project Structure
```text
Project 3/
│
├── sql_data_analysis.ipynb      # Main Jupyter Notebook containing SQL queries and results
├── Dataset for Data Analytics.xlsx  # Original dataset
├── Data Analytics Project 3.pdf  # Project guidelines document
├── README.md                    # Project documentation
├── requirements.txt             # Python dependencies
└── .gitignore                   # Ignored files (database, checkpoints)
```

## SQL Concepts Used
1. **`SELECT`**: Displaying all columns and specific column subsets.
2. **`WHERE`**: Filtering rows based on categorical values (`OrderStatus = 'Delivered'`) and numerical limits (`TotalPrice > 2500`).
3. **`ORDER BY`**: Sorting query output in descending order to identify top-performing transactions.
4. **`GROUP BY`**: Grouping rows by categories like product name and payment method.
5. **Aggregate Functions**:
   - `COUNT()`: Counting the number of orders per product.
   - `SUM()`: Calculating total sales revenue by payment method.
   - `AVG()`: Computing average order total price per product.

## Analysis Performed
- Viewed overall table structure and verified data loading.
- Filtered orders based on delivery status and high order values.
- Sorted transactions to find the highest value individual order.
- Grouped data to find product order frequencies.
- Calculated revenue distributions across different payment channels.
- Computed average spend per product category.

## Key Findings
- **Most Ordered Product**: Printer recorded the highest order volume with **181 orders**, followed closely by Tablet (179 orders).
- **Top Payment Method**: **Credit Card** generated the highest total revenue ($263,847.63), followed by Online payment ($262,442.94).
- **Highest Average Order Price**: **Laptop** had the highest average order total price ($1,110.56 per order).
- **Highest Single Order**: The single highest order total was **$3,456.40** for a Tablet order.

## How to Run
1. Clone or download this project folder.
2. Ensure Python 3.x is installed.
3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook sql_data_analysis.ipynb
   ```
5. Run all cells sequentially to create the SQLite database (`ecommerce.db`) and view the query results.

## Learning Outcomes
- Understood how to load tabular Excel data into a SQLite database table using Pandas.
- Learned how to write clean, beginner-level SQL queries using standard SQL syntax.
- Understood the practical difference between row filtering (`WHERE`) and grouping (`GROUP BY`).
- Gained confidence in summarizing metrics using SQL aggregate functions.

## Future Improvements
- Add `HAVING` clause to filter grouped aggregate data.
- Explore table joins (`JOIN`) if additional relational tables (e.g., customer details or product details) are added.
- Add multi-column sorting and complex date filtering.
