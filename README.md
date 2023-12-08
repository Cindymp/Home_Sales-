Module-22-challenge: Home Sales Analysis

 In this challenge, you'll use your knowledge of PySpark for a comprehensive analysis of home sales data. The script seamlessly fetches data from an AWS S3 bucket, transforms it into a Spark DataFrame, generates temporary views, caches them for efficiency, and executes diverse SQL queries on the cached data.

Prerequisites:

Spark and Java installations are mandatory.
The script facilitates the download and installation of the latest Spark 3.x version, Java installation, and configuration of environment variables.
Essential packages, such as pandas and findspark, are imported to support the script's functionality.
Key Operations:

Data Loading and Transformation:

Fetches data from an AWS S3 bucket and transforms it into a Spark DataFrame.
Temporary Views:

Creates temporary views of the DataFrame for subsequent analysis.
SQL Queries:

Conducts a series of SQL queries on the home sales data:
Average price for a four-bedroom house sold each year (rounded to two decimal places).
Average price of a home for each year built with 3 bedrooms and 3 bathrooms (rounded to two decimal places).
Average price of a home for each year built with 3 bedrooms, 3 bathrooms, two floors, and a size greater than or equal to 2,000 square feet (rounded to two decimal places).
"View" rating for the average price of a home (rounded to two decimal places) where home prices are greater than or equal to $350,000.
Runtime Analysis:

Evaluates the runtime for the specified queries, considering the dataset's small size.
Caching:

Temporarily caches the home_sales table to enhance query performance.
Query on Cached Data:

Verifies if the table is cached and executes a query filtering out view ratings with an average price greater than or equal to $350,000.
Runtime Comparison:

Compares the runtime of the query on cached data with the uncached runtime.
Parquet Data Processing:

Partitions the data by the "date_built" field in the formatted parquet home sales data.
Reads the parquet formatted data and creates a temporary table for further analysis.