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


### Understanding the Dataset

A thorough understanding of the available data is crucial before beginning any analysis. This project involved both dimension and fact tables:

Dimension Tables: Contain static data like customer and product details.
Fact Tables: Contain transactional data.

- Customers

	1. Customer_id column contains whole numbers.
	2. Both customer_acct_num and customer_postal_code columns are formatted as text.
	3. A new column named full_name was created by merging the first_name and last_name columns, separated by a space.
	4. The birth_year column was added by extracting the year from the birthdate column and formatting it as text.
	5. A conditional column named has_children was created, where it equals 'N' if total_children is 0, otherwise 'Y'.

- Products

	1. product_id column contains whole numbers.
	2. product_sku is formatted as text.
	3. product_retail_price and product_cost columns are formatted as decimal numbers.
	4. The statistics tools returned the number of distinct product brands and product names.
	5. It has 111 brands and 1,560 product names.
	6. A calculated column named discount_price was added, equal to 90% of the original retail price (10% discount).The column was formatted as a fixed decimal number and rounded to 2 digits.
	7. product_brand was grouped by, and the average retail price by brand was calculated. The new column was named Avg Retail Price. It shows an average retail price of $2.18 for Washington products and $2.21 for Green Ribbon.
	8. null values in the recyclable and low-fat columns were replaced with zeros.

- Stores

	1. store_id and region_id columns contain whole numbers.
	2. A calculated column named full_address was added by merging store_city, store_state, and store_country, separated by a comma and space (using a custom separator).
	3. A calculated column named area_code was added by extracting the characters before the dash ("-") in the store_phone field.

- Regions

	1. Contains sales_district and sales_region columns and region_id contains whole numbers.

- Calendar

	1. Used the date tools in the query editor to add the following columns:
	2. Start of Week (starting on Sunday), Name of Day, Start of Month, Name of Month, Quarter of Year, Year.

- Return_Data

	1. Fact Table
	2. Contains Returns infomation

- Transaction_Data

	1. Added a new folder named "MavenMarket Transactions", containing both MavenMarket_Transactions_1997 and MavenMarket_Transactions_1998 CSV files. The data is combined and is the 2nd transaction table in the project.
	2. Verified that data types are accurate (all ID columns and quantity are whole numbers).
	3. Confirmed data ranges from 1/1/1997 through 12/30/1998 in the "transaction_date" column.


## Importing Data into Power BI

- All the required data for this dashboard are loaded with the help of CSV files.


## Data Modeling
Data modeling is the foundation of any report, directly impacting its performance. In this project, we used the below snowflake schema for data modeling
<img>

- In the Customers table, categorized "customer_city" as City, "customer_postal_code" as Postal Code, and "customer_country" as Country/Region.
- In the Stores table, categorized "store_city" as City, "store_state" as State, "store_country" as Country/Region, and "full_address" as Address.

## Calculated Columns and Important DAX Measures.

### Highlighted important Calculates Columns and DAX Measures created. 
<img> all dax

- In the Products table, added a column named "Price_Tier" Equals "High" if the retail price is >$3, "Mid" if the retail price is >$1, and "Low" otherwise.

<img>

- In the Stores table, added a column named "Years_Since_Remodel". It Calculates the number of years between the current date (TODAY()) and the last remodel date

<img>

- Created new measures named "All Transactions" and "All Returns" to calculate grand total transactions and returns (regardless of filter context). We observe 269,720 transactions and 7,087 returns across all rows (test with product_brand on rows)

<img>

- Created new measures to calculate "Total Revenue" based on transaction quantity and product retail price, and format as $. We have an iterator function.

<img>

- Created a new measure named "YTD Revenue" to calculate year-to-date total revenue, and format as $

<img>

- Created a new measure named "60-Day Revenue" to calculate a running revenue total over a 60-day period, and format as $

<img>

- Create new measures named  "Last Month Transactions" to compare the total transations month by month.

<img>

### matrix
<img>

- Created a new measure named "Revenue Target" based on a 5% lift over the previous month revenue, and format as $

<img>


## Dashboard Design:

### 1. Topline Performance

<img src="https://github.com/SandeepanBhattacharyya/Adventure_Works_Project/blob/main/Exec_Dashboard_View.png" class="center">

### 2. Key Insights

<img src="https://github.com/SandeepanBhattacharyya/Adventure_Works_Project/blob/main/Map_View.png" class="center">


Access the Full Report: [Report](https://github.com/SandeepanBhattacharyya/Adventure_Works_Project/blob/main/Adventure_Works_Project_report.pdf)

### Project Outcome
