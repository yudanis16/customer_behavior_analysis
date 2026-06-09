# Data Analytics Project: Customer Shopping Behavior Analysis

## Overview
This repository contains an end-to-end data analytics project focused on extracting actionable business insights from retail transaction data. The project demonstrates a complete workflow: starting with data cleaning and feature engineering in Python, executing Exploratory Data Analysis (EDA) using PostgreSQL, building an interactive Power BI dashboard, and delivering strategic business recommendations via a Gamma AI presentation.

---

## Dataset
* **File:** `customer_shopping_behavior.csv`
* **Size:** 3,900 rows and 18 columns.
* **Description:** Contains historical customer transaction records, including demographics, purchase amounts, product categories, shipping types, review ratings, and subscription status.

---

## Tools
* **Data Processing & Cleaning:** Python (Pandas, SQLAlchemy)
* **Database & Querying:** PostgreSQL
* **Data Visualization:** Power BI
* **Presentation & Reporting:** Gamma AI

---

## Steps
1. **Data Loading and Cleaning (Python):** 
   * Imported the raw CSV dataset using Pandas.
   * Handled missing data by imputing the median for 37 missing values in the `Review Rating` column.
   * Standardized column names to `snake_case`.
   * Engineered new features, such as creating an `age_group` category using the `qcut` function.
2. **Database Integration (SQLAlchemy & PostgreSQL):** 
   * Established a connection using SQLAlchemy and seamlessly loaded the cleaned dataframe into a local PostgreSQL database for structured querying.
3. **Exploratory Data Analysis (SQL):** 
   * Formulated advanced SQL queries to evaluate customer retention (New vs. Returning vs. Loyal), analyze discount dependencies, and calculate revenue distribution by age demographic.
4. **Dashboard Creation (Power BI):** 
   * Connected the processed data to Power BI to build an interactive dashboard highlighting core KPIs ($59.76 Average Purchase Amount, 3.9K Customers) with dynamic slicers.
5. **Reporting (Gamma AI):** 
   * Translated SQL and Power BI findings into a professional, actionable business presentation.

---

## Dashboard
The Power BI dashboard (`Customers Behavior Dashboard.pbix`) provides a comprehensive view of business performance. It visualizes critical metrics such as total revenue by category (Clothing leading the sales) and revenue by age group. Interactive filters (Subscription Status, Gender, Category, Shipping Type) allow stakeholders to dynamically slice the data for real-time insights.

---

## Results & Key Insights
* **Retention vs. Acquisition Gap:** The business has an exceptionally strong retention rate with 3,116 "Loyal" customers, but suffers from critically low acquisition, securing only 83 "New" customers.
* **Missed Subscription Opportunities:** Out of the highly active customer base, 2,518 repeat buyers (>5 purchases) are not subscribed, indicating that current subscription perks fail to incentivize top buyers.
* **Margin-Draining Discounts:** Specific products are heavily dependent on extreme discounts to drive sales, notably Hats (50%) and Sneakers (49.66%). 
* **Primary Revenue Drivers:** The "Young Adult" demographic contributes the highest total revenue ($62,143), establishing them as the primary target for future marketing budgets.

---

## How to Run
1. Clone this repository to your local machine.
2. Run the Python data preparation script/notebook to clean the raw `customer_shopping_behavior.csv` data and export it to your PostgreSQL database.
3. Execute the queries found in `Customer_Behavior.sql` within your PostgreSQL client (e.g., pgAdmin or DBeaver) to reproduce the analytical findings.
4. Open `Customers Behavior Dashboard.pbix` in Power BI Desktop to interact with the visual dashboard.
5. Review the executive summary in the presentation slide deck.
