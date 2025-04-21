## 🏡 Home Sales Analysis with PySpark
This repository contains a PySpark-based analysis of home sales data. The project explores real estate trends using SparkSQL to answer business-relevant questions and benchmark the performance of caching and partitioning strategies.

## 📁 File Structure
Home_Sales.ipynb: Final Jupyter notebook containing the full implementation and analysis.

home_sales_revised.csv: Revised home sales dataset (loaded from AWS S3).

README.md: Project overview and instructions.

## 🚀 Project Objective
Use Apache Spark and PySpark SQL to perform large-scale data analysis on a dataset of home sales. The goals are to:

Analyze average home prices based on various features.

Compare performance impacts of caching and partitioning.

Practice data transformation, SQL querying, and performance tuning using Spark.

## 📌 Instructions
1. Setup
Rename the provided starter notebook file to Home_Sales.ipynb.

Import required PySpark libraries and modules.

Load the dataset from AWS S3:

arduino
Copy
Edit
s3a://<bucket-path>/home_sales_revised.csv
2. Data Preparation
Read the CSV file into a PySpark DataFrame.

Register the DataFrame as a temporary SQL table called home_sales.

## 🧠 SparkSQL Tasks
Use SparkSQL to answer the following:

Average price of 4-bedroom homes by year sold

Group by year

Round to 2 decimal places

Average price of homes built per year with 3 beds and 3 baths

Filter on bedrooms == 3 and bathrooms == 3

Average price of 3-bed/3-bath homes with ≥2 floors and ≥2000 sqft, grouped by year built

Average price per "view" rating (only views where average price ≥ $350,000)

Record runtime

⚡ Performance Optimization
# 1. Caching
Cache the home_sales temp table.

Confirm it's cached.

Rerun Query 4 on cached data and record runtime.

# 2. Partitioning
Write the DataFrame as a Parquet file, partitioned by date_built.

Create a new temporary table from the Parquet data.

Rerun Query 4 on partitioned data and record runtime.

# 3. Uncaching
Uncache the home_sales table.

Confirm the table is no longer cached.

## 🗃️ Output
Final results include:

Query answers (rounded to two decimal places)

Runtime benchmarks for cached vs uncached and partitioned queries

Spark SQL performance insights

## 🛠️ Technologies Used
Python

Apache Spark / PySpark

SparkSQL

AWS S3 (for data loading)

Jupyter Notebook
