# Exploratory Data Analysis (EDA)

## Objective
- Calculate basic statistics (mean, median, count, etc.)
- Identify trends in sales and orders
- Check for missing values, duplicates, and outliers
- Summarize findings with simple charts

## Dataset Information
The dataset `Dataset for Data Analytics.xlsx` contains 1,200 rows and 14 columns:
- `OrderID`, `Date`, `CustomerID`
- `Product`, `Quantity`, `UnitPrice`, `TotalPrice`
- `ShippingAddress`, `PaymentMethod`, `OrderStatus`
- `TrackingNumber`, `ItemsInCart`, `CouponCode`, `ReferralSource`

## Technologies Used
- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure
```text
├── data_analysis.ipynb
├── Dataset for Data Analytics.xlsx
├── README.md
├── requirements.txt
└── .gitignore
```

## Main Findings
- **Top Product:** Chair generated the highest revenue, while Printer had the highest order count.
- **Average Spend:** The average order total is $1,053.97 and the median is $823.62.
- **Order Status:** Cancelled and Returned orders make up around 41.4% of total orders.
- **Outliers:** Found 8 high-value outliers in Total Price due to bulk orders of expensive items.

## How to Run
1. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Open Jupyter Notebook:
   ```bash
   jupyter notebook data_analysis.ipynb
   ```
