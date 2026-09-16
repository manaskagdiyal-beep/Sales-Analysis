#  Sales Analysis Using Python

## Project Overview

This project focuses on analyzing sales data using Python to understand sales performance, profitability, product performance, and category-wise trends.

The analysis uses **Pandas** for data manipulation and analysis and **Matplotlib** for data visualization. The project demonstrates the complete basic workflow of a data analytics project, including data loading, data cleaning, exploratory data analysis (EDA), and visualization.

---

## Objectives

The main objectives of this project are:

* Analyze overall sales performance
* Analyze overall profit performance
* Compare sales and profit
* Identify the highest and lowest sales
* Identify the highest and lowest profit
* Analyze sales by category
* Analyze profit by category
* Identify high-performing products
* Analyze order dates and sales trends
* Generate meaningful business insights from the data

---

## Tools & Technologies

* **Python**
* **Pandas**
* **Matplotlib**
* **Jupyter Notebook**
* **GitHub**

---

## Dataset

The project uses a sales dataset containing information related to orders, products, categories, sales, profit, and order dates.

### Important Columns

| Column       | Description                        |
| ------------ | ---------------------------------- |
| `Order Date` | Date on which the order was placed |
| `Product`    | Name of the product                |
| `Category`   | Category of the product            |
| `Sales`      | Sales amount                       |
| `Profit`     | Profit generated from the order    |

---

## Data Analysis Process

### 1. Data Loading

The dataset was loaded into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("Sales_Analysis_Dataset.csv")
```

### 2. Data Understanding

The dataset was explored using:

```python
df.head()
df.tail()
df.shape
df.columns
df.info()
df.describe()
```

This helped understand the structure, columns, data types, and statistical summary of the dataset.

### 3. Data Cleaning

The dataset was checked for missing values and unnecessary empty columns.

```python
df.isnull().sum()
```

Completely empty columns can be removed using:

```python
df = df.dropna(axis=1, how="all")
```

Other cleaning operations were performed where required.

---

## Exploratory Data Analysis

The following analysis was performed:

### Sales Analysis

* Total Sales
* Average Sales
* Minimum Sales
* Maximum Sales
* Product with the highest/lowest sales

Example:

```python
df["Sales"].sum()
df["Sales"].mean()
df["Sales"].max()
df["Sales"].min()
```

### Profit Analysis

* Total Profit
* Average Profit
* Minimum Profit
* Maximum Profit
* Product with the highest/lowest profit

Example:

```python
df["Profit"].sum()
df["Profit"].mean()
df["Profit"].max()
df["Profit"].min()
```

### Category Analysis

Sales and profit were analyzed category-wise.

```python
category_analysis = df.groupby("Category")[["Sales", "Profit"]].sum()

category_analysis
```

This helps compare the performance of different product categories.

### Sales vs Profit

Sales and profit were compared to understand the relationship between revenue generated and profitability.

```python
df.groupby("Category")[["Sales", "Profit"]].sum()
```

### Date Analysis

The `Order Date` column was also analyzed to understand sales trends over time.

Examples include:

```python
df["Order Date"].dt.year
df["Order Date"].dt.month
df["Order Date"].dt.month_name()
```

---

## Visualizations

Matplotlib was used to create visualizations such as:

* Sales by Category
* Profit by Category
* Sales vs Profit
* Product performance
* Time-based sales trends

Example:

```python
category_sales = df.groupby("Category")["Sales"].sum()

category_sales.plot(kind="bar")

plt.title("Sales by Category")
plt.xlabel("Category")
plt.ylabel("Sales")
plt.show()
```

---

## Key Insights

The analysis helps identify:

* Which category generates the highest sales?
* Which category generates the highest profit?
* Which products perform best?
* Which products have lower sales or profit?
* The overall sales and profit generated
* Differences between sales and profitability
* Trends in sales over time

> **Note:** The exact numerical findings are available in the `Sales_Analysis.ipynb` notebook and are based on the dataset used in this project.

---

## Project Structure

```text
Sales-Analysis/
│
├── Sales_Analysis.ipynb
├── Sales_Analysis_Dataset.csv
├── README.md
│
└── images/
    ├── sales_by_category.png
    ├── profit_by_category.png
    └── sales_vs_profit.png
```

---

## Skills Demonstrated

This project demonstrates the following data analytics skills:

* Python Programming
* Pandas
* Data Cleaning
* Data Manipulation
* Exploratory Data Analysis (EDA)
* Descriptive Statistics
* GroupBy Analysis
* Sales & Profit Analysis
* Date/Time Analysis
* Data Visualization
* Business Insight Generation

---

## Future Improvements

The project can be further improved by:

* Adding more advanced visualizations
* Performing correlation analysis
* Creating an interactive dashboard using Power BI or Tableau
* Performing customer-level analysis
* Adding predictive analysis
* Automating the data-cleaning process

---

##  Author

**Manas Kagdiyal**

Aspiring Data Analyst | Python | Pandas | Data Analytics

---

## Conclusion

This project demonstrates the use of Python for analyzing real-world sales data. Through data cleaning, exploratory data analysis, statistical analysis, and visualization, useful patterns and business insights can be identified from the dataset.

The project is part of my journey toward developing practical **Data Analytics and Python skills**.
