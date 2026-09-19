# Analysing Pharmaceutical Sales Data

A beginner-level data analysis project that explores pharmaceutical sales data using Python, Pandas, and Matplotlib.

## Project Description

In this project, pharmaceutical sales data is analysed to identify sales patterns across different ATC (Anatomical Therapeutic Chemical) drug categories.

The analysis focuses on total sales, sales during specific months, yearly sales, average daily sales, and monthly patterns in respiratory drug sales.

## Questions Analysed

- What are the total sales quantities for each drug category (ATC code)?
- Which three drug categories have the highest sales in January 2015?
- Which three drug categories have the highest sales in July 2016?
- Which three drug categories have the highest sales in September 2017?
- Which drug category had the highest total sales in 2017?
- Which drug category has the highest average daily sales?
- Are respiratory drugs (R03) sold more during specific months?

## Technologies Used

- Python 3
- Pandas
- Matplotlib
- Jupyter Notebook

## Concepts Learned

Through this project, I learned how to:

- Load CSV datasets using Pandas
- Inspect and understand datasets
- Select specific columns
- Filter data using conditions
- Work with date and time data
- Calculate total sales using `sum()`
- Calculate average sales using `mean()`
- Find the top values using `nlargest()`
- Find maximum values using `idxmax()`
- Sort data using `sort_values()`
- Group data using `groupby()`
- Create bar charts using Matplotlib
- Analyse patterns in time-based data

## Dataset

The project uses the Pharma Sales Dataset from Kaggle:

https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data

The dataset contains daily pharmaceutical sales data categorized using ATC codes.

## Project Structure

```text
Project 4/
│
├── analysis.ipynb
├── salesdaily.csv
└── README.md