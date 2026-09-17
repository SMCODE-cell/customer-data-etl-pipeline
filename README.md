# Customer Data ETL & Analytics Pipeline

## Overview

This project demonstrates an end-to-end ETL pipeline for customer and transaction data using Python, Pandas, SQLite and SQL.

The pipeline extracts data from CSV and JSON sources, performs data cleaning and validation, transforms the data, loads it into a relational SQLite database, and performs SQL-based analytics.

## Problem Statement

Businesses receive customer and transaction data from multiple sources. Raw data may contain duplicate records, missing values and invalid transaction values.

This project demonstrates a data pipeline for cleaning, validating, transforming and analyzing customer and transaction data.

## Tech Stack

- Python
- Pandas
- NumPy
- SQLite
- SQL
- JSON
- Matplotlib
- Google Colab
- GitHub

## ETL Architecture

CSV / JSON
↓
Python + Pandas
↓
Data Cleaning
↓
Data Validation
↓
Data Transformation
↓
SQLite Database
↓
SQL Analytics
↓
Business Insights
↓
Visualization

## ETL Pipeline

### Extract

- Read customer data from CSV.
- Read order data from JSON.

### Transform

- Remove duplicate records.
- Handle missing values.
- Validate dates.
- Validate quantities and prices.
- Calculate total transaction amount.
- Standardize data types.

### Load

Load the cleaned customer and order datasets into relational SQLite tables.

### Analyze

Use SQL queries to generate:

- Total revenue
- Revenue by category
- Revenue by city
- Top customers
- Product performance
- Monthly revenue
- Customer segmentation
- Order value classification

## Data Model

### Customers

| Column | Description |
|---|---|
| customer_id | Unique customer identifier |
| name | Customer name |
| email | Customer email |
| city | Customer city |
| signup_date | Customer registration date |

### Orders

| Column | Description |
|---|---|
| order_id | Unique order identifier |
| customer_id | Customer reference |
| order_date | Order date |
| product | Product name |
| category | Product category |
| quantity | Quantity purchased |
| unit_price | Price per unit |
| total_amount | Total transaction value |

### Relationships

- `customers.customer_id` — Primary Key
- `orders.order_id` — Primary Key
- `orders.customer_id` — Foreign Key

One customer can have multiple orders.

## Data Quality Checks

The pipeline performs checks for:

- Duplicate customer records
- Missing email values
- Missing city values
- Invalid order quantities
- Invalid product prices
- Invalid dates
- Missing values

Invalid and inconsistent records are handled during the transformation stage.

## SQL Concepts Demonstrated

- SELECT
- WHERE
- JOIN
- LEFT JOIN
- GROUP BY
- ORDER BY
- LIMIT
- Aggregate functions
- CTEs
- CASE statements
- Window functions

## Analytics

### Customer Analysis

- Top customers by spending
- Customer spending
- Customer segmentation

### Product Analysis

- Units sold
- Product revenue
- Category performance

### Revenue Analysis

- Total revenue
- Revenue by category
- Revenue by city
- Monthly revenue

## Results

The pipeline successfully performs:

1. Data extraction
2. Data profiling
3. Data cleaning
4. Data validation
5. Data transformation
6. Relational database loading
7. SQL analytics
8. Data visualization

## Project Structure

```text
customer-data-etl-pipeline/
│
├── Customer_Data_ETL_Analytics_Pipeline.ipynb
├── customers_raw.csv
├── orders_raw.json
├── customers_clean.csv
├── orders_clean.csv
└── README.md
