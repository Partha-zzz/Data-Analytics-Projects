# Data Cleaning & Preparation using Python (Pandas)

## Project Overview
This project focuses on the cleaning and preprocessing of a raw retail-like transactional Excel dataset. It was completed as part of the **Week 1 task for the DecodeLabs Data Analytics Internship**. The primary objective was to transform raw, messy data into a clean, structured, and reliable format suitable for downstream analysis or visualization, using Python and the Pandas library.

---

## Problem Statement
In real-world scenarios, raw datasets are rarely clean. They often contain missing values, duplicate records, inconsistent date formats, and other anomalies. Conducting analytics or building models on dirty data leads to inaccurate insights and faulty decision-making. 

This project addresses this fundamental challenge by identifying and resolving data quality issues in a transactional dataset of 1,200 records, ensuring data integrity and consistency before any analytics tasks are performed.

---

## Solution Approach
The data preparation workflow was implemented step-by-step in a Jupyter Notebook:

1. **Data Inspection**: Loaded the Excel dataset using Pandas (`read_excel`) and performed an initial assessment of the data structure. Using `.head()`, `.info()`, and `.shape`, I checked the dimensions of the dataset, identified the column data types, and observed how the data was laid out.
2. **Missing Value Analysis**: Used `.isnull().sum()` to quantify missing data across all columns. The analysis revealed that only the `CouponCode` column had missing values (309 missing entries).
3. **Handling Missing Coupon Codes**: Instead of dropping the rows with missing coupon codes (which would result in losing valuable transaction data), I used `.fillna('No Coupon')` to replace the null entries with a default string. This maintains the record integrity while explicitly indicating that no coupon was used for those transactions.
4. **Duplicate Verification**: Checked for duplicate rows across all fields using `.duplicated().sum()`. While no identical duplicate rows were found in this dataset, a safety step using `.drop_duplicates()` was included to ensure robustness.
5. **OrderID Validation**: Validated the uniqueness of the primary key (`OrderID`) by checking for duplicates within that specific column. No duplicate transaction IDs were detected, confirming that each row represents a unique order.
6. **Date Standardization**: To prevent issues with inconsistent date representations, the `Date` column was parsed into standard datetime format using `pd.to_datetime()`. It was then consistently formatted as `YYYY-MM-DD` using `.dt.strftime("%Y-%m-%d")`.
7. **Exporting Cleaned Data**: Finally, the preprocessed DataFrame was exported to a new file named `Cleaned_Data.xlsx` with `index=False` to avoid saving row numbers as a separate column.

---

## Technologies Used
- **Language**: Python
- **Libraries**: Pandas, OpenPyXL (for Excel reading/writing)
- **Environment**: Jupyter Notebook

---

## Project Structure
```text
Week 1/
│
├── Cleaned_Data.xlsx               # Preprocessed and cleaned dataset
├── Dataset for Data Analytics.xlsx  # Raw input dataset
├── data_cleaning.ipynb             # Jupyter Notebook containing the cleaning logic
├── README.md                       # Project documentation
└── .gitignore                      # Git configuration to exclude temporary/unwanted files
```

### Version Control & Excluded Files
To keep the repository lightweight and professional, some files are excluded from version control via `.gitignore`. 

Below is the `.gitignore` configuration used to exclude large document files and temporary notebook checkpoints:
```text
# Jupyter Notebook checkpoints
.ipynb_checkpoints/

# Project documentation / large files not intended for version control
DATA ANALYTICS p1.pdf
```

---

## How to Run

### 1. Prerequisites
Ensure you have Python installed on your system. You will also need to install `pandas` and `openpyxl`.

### 2. Installation
Install the required dependencies using pip:
```bash
pip install pandas openpyxl notebook
```

### 3. Running the Jupyter Notebook
Clone this repository, navigate to the project directory, and start Jupyter Notebook:
```bash
jupyter notebook
```
Open `data_cleaning.ipynb` and run all cells sequentially to execute the data cleaning pipeline and generate the `Cleaned_Data.xlsx` file.

---

## Results
- **Missing Values Handled**: 309 missing values in `CouponCode` successfully filled with `"No Coupon"`.
- **Data Integrity Verified**: Verified that there are 0 duplicate rows and 0 duplicate `OrderID` values.
- **Dates Standardized**: The `Date` column was successfully formatted uniformly to `YYYY-MM-DD`.
- **Ready for Analysis**: The output dataset `Cleaned_Data.xlsx` is clean, consistent, and ready for exploratory data analysis (EDA) or dashboard creation.

---

## Learning Outcomes
Through this project, I strengthened my understanding of:
- **Data Inspection**: How to quickly assess a dataset's size, column types, and general structure using Pandas.
- **Missing Value Handling**: Understanding when to fill missing values versus when to drop them to preserve dataset volume.
- **Data Validation**: Techniques to verify uniqueness of identifiers (`OrderID`) and detect duplicate rows.
- **Data Preprocessing**: Converting column types (e.g., strings to datetime objects) and formatting dates consistently.
- **Pandas Fundamentals**: Practical application of Pandas methods like `.fillna()`, `.duplicated()`, and `.to_excel()`.

---

## Future Improvements
As I progress in my data science journey, I plan to expand this project by:
- **Automating Data Validation**: Implementing assertions or validation libraries (like Great Expectations) to check data schemas automatically.
- **Creating Reusable Cleaning Pipelines**: Wrapping the cleaning steps into modular Python functions (`.py` scripts) for cleaner code execution.
- **Generating Quality Reports**: Automatically generating data profile reports (using `ydata-profiling` or similar libraries) before and after cleaning.
- **Interactive Dashboard**: Building a simple visualization dashboard (using Streamlit or Power BI) to display sales trends from the cleaned data.
