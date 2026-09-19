# Netflix Dataset Cleaning

A data cleaning project using **Python and Pandas** to inspect, clean, transform, and prepare the Netflix Movies and TV Shows dataset for further analysis.

## 📌 Project Overview

Real-world datasets are rarely clean. They often contain missing values, inconsistent data types, duplicate records, and columns that require transformation before they can be analyzed.

In this project, the **Netflix Movies and TV Shows dataset** from Kaggle is cleaned using Pandas. The main focus is on understanding the data first and making deliberate decisions about how different types of messy data should be handled.

The project covers the complete workflow:

**Raw Dataset → Data Inspection → Missing Value Handling → Data Transformation → Validation → Clean Dataset**

## 🎯 Objectives

- Load the Netflix dataset using Pandas
- Inspect the dataset using `.head()`, `.info()`, and `.describe()`
- Identify missing values
- Handle missing values appropriately
- Remove duplicate records
- Clean mixed-type columns such as `duration`
- Convert date columns into proper `datetime` format
- Validate the cleaned dataset
- Export the final cleaned dataset as a CSV file

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **Jupyter Notebook**
- **Regular Expressions (Regex)**

## 📂 Project Structure

```text
Netflix-Dataset-Cleaning/
│
├── netflix_data_cleaning.ipynb
├── netflix_titles.csv
├── netflix_titles_cleaned.csv
└── README.md