# Walmart Sales Data Analysis

## Project Overview
This project involves analyzing Walmart sales data to understand top-performing branches and products, sales trends of different products, and customer behavior. The analysis aims to provide insights that can help increase sales and improve customer satisfaction.

## Database Schema
The analysis is based on a MySQL database with the following structure:

```sql
CREATE TABLE sales(
    invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
    branch VARCHAR(5) NOT NULL,
    city VARCHAR(30) NOT NULL,
    customer_type VARCHAR(30) NOT NULL,
    gender VARCHAR(30) NOT NULL,
    product_line VARCHAR(100) NOT NULL,
    unit_price DECIMAL(10,2) NOT NULL,
    quantity INT NOT NULL,
    tax_pct FLOAT(6,4) NOT NULL,
    total DECIMAL(12, 4) NOT NULL,
    date DATETIME NOT NULL,
    time TIME NOT NULL,
    payment VARCHAR(15) NOT NULL,
    cogs DECIMAL(10,2) NOT NULL,
    gross_margin_pct FLOAT(11,9),
    gross_income DECIMAL(12, 4),
    rating FLOAT(2, 1)
)
```

## Features
The analysis includes several key aspects:

### Product Analysis
- Unique product lines
- Most selling product lines
- Revenue by product line
- Average VAT (Tax) by product line
- Product performance analysis (Good/Bad)
- Product ratings analysis

### Sales Analysis
- Sales by time of day
- Sales by day of week
- Revenue by month
- Revenue by customer type
- Revenue by city
- Cost of goods sold (COGS) by month

### Customer Analysis
- Customer types distribution
- Payment method analysis
- Gender distribution by branch
- Customer ratings by time of day
- Customer ratings by day of week
- Branch performance analysis

## Key Findings
1. Product Performance:
   - Most selling product lines
   - Highest revenue generating product lines
   - Products with best average ratings

2. Sales Patterns:
   - Peak sales periods
   - Highest revenue generating cities
   - Most profitable customer segments

3. Customer Behavior:
   - Preferred payment methods
   - Shopping patterns by gender
   - Rating patterns

## Setup and Usage

### Prerequisites
- MySQL Server
- MySQL Workbench (recommended for running queries)

### Installation Steps
1. Clone this repository
2. Open MySQL Workbench
3. Create a new database:
   ```sql
   CREATE DATABASE IF NOT EXISTS walmartSales;
   ```
4. Select the database:
   ```sql
   USE walmartSales;
   ```
5. Import and run the SQL scripts in the following order:
   - `create_tables.sql`
   - `data_cleaning.sql`
   - `analysis_queries.sql`

## Contributing
Feel free to fork this repository and submit pull requests. You can also open issues for any bugs found or improvements suggested.
