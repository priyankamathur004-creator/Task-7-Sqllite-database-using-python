# Task-7-Sqllite-database-using-python
SQLite database file
# Task 7: Basic Sales Summary using Python & SQLite
1. Objective
The primary objective of this task was to demonstrate proficiency in connecting Python to an internal database, executing a basic SQL aggregation query, and presenting the summarized data both textually and visually.

The goal was specifically to pull simple sales information (like total quantity sold and total revenue) and display the results using basic print statements and a Matplotlib bar chart.

2. Tools and Technologies
Tool	Purpose
Python 3	Core programming environment
sqlite3	Built-in Python library for database connectivity
pandas	Used to run the SQL query and load the results into a DataFrame for analysis and plotting
matplotlib	Used for creating the required bar chart
Jupyter Notebook	Environment used for development and execution of the script

Export to Sheets
3. Methodology
The analysis was performed in a single script following these key steps:

Database Creation: Created the SQLite database file, sales_data.db, and defined a single table named sales.

Data Population: Inserted sample sales records (including columns for order_id, product, quantity, and price) into the sales table.

SQL Aggregation: Executed a single SQL query to calculate the total quantity sold (SUM(quantity)) and total revenue (SUM(quantity * price)) for each unique product.

Data Loading: Used the pandas.read_sql_query() function to pull the aggregated results directly into a pandas DataFrame.

Output Display: Printed the resulting DataFrame to the console.

Visualization: Generated a simple bar chart using the DataFrame's built-in plotting functionality (powered by Matplotlib), visualizing the revenue grouped by product.

4. Key SQL Query
SQL

SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM 
    sales 
GROUP BY 
    product;
