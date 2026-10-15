# Customer Shopping Behavior Analysis

An end-to-end data analytics portfolio project exploring customer purchasing patterns, product performance, discounts, shipping preferences, and subscription behavior. The workflow uses **Python for data preparation**, **SQL for business analysis**, and **Power BI for interactive visualization**.


## Business Problem

Retail teams need to understand what drives customer purchases and how customer segments behave. This project turns customer shopping records into analysis that can help answer questions such as:

- Which product categories and items are purchased most often?
- How do purchase amounts differ by gender, age group, shipping type, and subscription status?
- How frequently are discounts used, and which products have the highest discount rates?
- How do new, returning, and loyal customers compare?
- Which products receive the highest average review ratings?

## Project Objectives

- Inspect and prepare customer shopping data for analysis.
- Use SQL aggregations, filtering, subqueries, `CASE` expressions, CTEs, and window functions to answer business questions.
- Present key metrics and patterns in a Power BI dashboard.
- Summarize findings in a report and presentation for non-technical stakeholders.

## Tools and Technologies

- **Python:** pandas, Jupyter Notebook, SQLAlchemy
- **SQL:** PostgreSQL / MySQL / SQL Server (choose the database you actually used)
- **Power BI:** dashboard and interactive visual analysis
- **Other files:** CSV dataset, SQL query file, PDF report, PowerPoint presentation

## Repository Contents

| File | Purpose |
|---|---|
| `customer_shopping_behavior.csv` | Source customer shopping dataset |
| `Customer_Shopping_Behavior_Analysis.ipynb` | Data inspection, cleaning/preparation, and database-loading workflow |
| `customer_behavior_sql_queries.sql` | SQL queries for the business questions |
| `customer_behavior_dashboard.pbix` | Power BI dashboard file |
| `Business Problem Document.pdf` | Business context and problem statement |
| `Customer Shopping Behavior Analysis.pdf` | Project report |
| `Customer-Shopping-Behavior-Analysis.pptx` | Project presentation |

## Workflow

1. **Data preparation — Python**
   - Load the CSV into pandas.
   - Inspect column types, summary statistics, and missing values.
   - Prepare the data for analysis and database loading.
2. **Database analysis — SQL**
   - Load the prepared data into a table named `customer`.
   - Run the queries in `customer_behavior_sql_queries.sql`.
   - Explore revenue, average purchase amount, ratings, discount rates, customer segments, and product rankings.
3. **Visualization — Power BI**
   - Open `customer_behavior_dashboard.pbix` in Power BI Desktop.
   - If prompted, update the data source to your local dataset/database and refresh the model.
   - Explore the dashboard and use its filters/slicers where available.
4. **Communication**
   - Use the report and presentation to explain the business questions, findings, and recommendations.

## Business Questions Covered

1. What is the revenue by gender?
2. Which customers used a discount but spent at least the average purchase amount?
3. Which five products have the highest average review rating?
4. How do average purchase amounts compare for Standard and Express shipping?
5. How do subscriber and non-subscriber purchase patterns compare by customer count, average spend, and total revenue?
6. Which products have the highest percentage of purchases with discounts?
7. How many customers fall into New, Returning, and Loyal segments based on previous purchases?
8. What are the top three purchased products within each category?
9. Among customers with more than five previous purchases, how many are subscribers versus non-subscribers?
10. How much revenue does each age group contribute?

## Getting Started

### 1. Download or clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Set up Python

```bash
python -m venv .venv
```

Windows Command Prompt:

```bat
.venv\Scripts\activate.bat
```

Install the packages needed for the notebook (the exact database driver depends on your database):

```bash
pip install pandas jupyter sqlalchemy psycopg2-binary
```

For MySQL, use `pymysql` instead of `psycopg2-binary`; for SQL Server, configure `pyodbc` and install the appropriate Microsoft ODBC driver.

### 3. Configure your database

Create a database (for example, `customer_behavior`) and update the connection settings in the notebook to match your local setup. **Never commit real passwords, API keys, or other credentials to GitHub.** Prefer environment variables for credentials.

Run the notebook cells to load the data into your database, then execute the SQL queries using your database client. SQL syntax may need small changes depending on the database engine.

### 4. Open the dashboard

Open `customer_behavior_dashboard.pbix` in Power BI Desktop. If the original data-source path is unavailable, reconnect it to your own data source and refresh.

## Skills Demonstrated

- Data inspection and preparation with pandas
- SQL querying, aggregation, joins/CTEs, subqueries, conditional logic, and window functions
- Customer segmentation and business KPI analysis
- Power BI dashboard exploration and data storytelling
- Translating business questions into analytical queries and recommendations

## Key Deliverables

- Python analysis notebook
- SQL business-question query collection
- Interactive Power BI dashboard
- Written report and presentation

