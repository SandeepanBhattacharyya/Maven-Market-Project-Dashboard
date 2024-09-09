# Maven Market Project Dashboard

## Project Overview

In the current business environment, where data plays a crucial role, the skill to harness data for informed decision-making sets professionals apart. 

To highlight my expertise in Power BI and data analytics, I utilized the Maven Market dataset — a multi-national grocery chain with locations in Canada, Mexico and the United States.

This project underscores my abilities in data storytelling, applying DAX formulas, and creating dynamic reports.

[View Project Report]()

## Technologies Used

- PowerBi Desktop
- DAX (Data Analysis Expressions) language
- Excel

## Power BI Skills Acquired

- Identifying key questions before initiating a project
- Creating calculated columns
- Crafting measures using DAX
- Data modeling techniques
- Utilizing Bookmarks for toggling between visuals
- Implementing page navigation with buttons
- Avoiding division by zero errors using the DIVIDE function
- Creating date tables with M language
- Dynamic title generation based on filters
- Integrating KPI indicators
- Applying conditional formatting with icons or colors
- Data validation strategies
- Power BI services
- Publishing reports on Power BI services
- And much more 😅

## Key Business Concepts




### Understanding the Dataset

A thorough understanding of the available data is crucial before beginning any analysis. This project involved both dimension and fact tables:

Dimension Tables: Contain static data like customer and product details.
Fact Tables: Contain transactional data.

- Customers

customer_id column contains whole numbers.
Both customer_acct_num and customer_postal_code columns are formatted as text.
A new column named full_name was created by merging the first_name and last_name columns, separated by a space.
The birth_year column was added by extracting the year from the birthdate column and formatting it as text.
A conditional column named has_children was created, where it equals 'N' if total_children is 0, otherwise 'Y'.

- Products

product_id column contains whole numbers.
product_sku is formatted as text.
product_retail_price and product_cost columns are formatted as decimal numbers.
The statistics tools returned the number of distinct product brands and product names.
It has 111 brands and 1,560 product names.
A calculated column named discount_price was added, equal to 90% of the original retail price (10% discount).The column was formatted as a fixed decimal number and rounded to 2 digits.
product_brand was grouped by, and the average retail price by brand was calculated. The new column was named Avg Retail Price. It shows an average retail price of $2.18 for Washington products and $2.21 for Green Ribbon.
null values in the recyclable and low-fat columns were replaced with zeros.

- Stores

store_id and region_id columns contain whole numbers.
A calculated column named full_address was added by merging store_city, store_state, and store_country, separated by a comma and space (using a custom separator).
A calculated column named area_code was added by extracting the characters before the dash ("-") in the store_phone field.

- Regions

Contains sales_district and sales_region columns and region_id contains whole numbers.

- Calendar

Used the date tools in the query editor to add the following columns:
Start of Week (starting on Sunday), Name of Day, Start of Month, Name of Month, Quarter of Year, Year.

- Return_Data

Fact Table
Contains Returns infomation

- Transaction_Data

Added a new folder named "MavenMarket Transactions", containing both MavenMarket_Transactions_1997 and MavenMarket_Transactions_1998 CSV files. The data is combined and is the 2nd transaction table in the project.
Verified that data types are accurate (all ID columns and quantity are whole numbers).
Confirmed data ranges from 1/1/1997 through 12/30/1998 in the "transaction_date" column.


## Importing Data into Power BI

- All the required data for this dashboard are loaded with the help of CSV files.


## Data Modeling
Data modeling is the foundation of any report, directly impacting its performance. In this project, we used the below snowflake schema for data modeling
<img>

1. In the Customers table, categorized "customer_city" as City, "customer_postal_code" as Postal Code, and "customer_country" as Country/Region.
2. In the Stores table, categorized "store_city" as City, "store_state" as State, "store_country" as Country/Region, and "full_address" as Address.

## Calculated Columns and Important DAX Measures.

Highlighted importand Calculates Columns and DAX Measures created. 


