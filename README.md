# Sales-Insights-Data-Analysis-Project
## Data Analysis Using SQL
1. Show all customer records

   SELECT * FROM customers;

2. Show total number of customers

   SELECT count(*) FROM customers;

3. Show transactions for Chennai market (market code for chennai is Mark001

   SELECT * FROM transactions where market_code='Mark001';

4. Show distrinct product codes that were sold in chennai

   SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars

   SELECT * from transactions where currency="USD"

6. Show transactions in 2020 join by date table

   SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020,

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON
   transactions.order_date=date.date where date.year=2020 and
   transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020, January Month,

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON 
   transactions.order_date=date.date where date.year=2020 and and 
   date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON 
   transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Data Analysis Using Power BI
1. Formula to create norm_amount column
   = Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)"
     then [sales_amount]*75 else [sales_amount], type any)

## Project Insights
1. Computer hardware business facing challenges in scaling within a dynamically changing market and lacking actionable insights.
2. Performed data analysis using SQL and Power BI to track revenue growth, year-over-year(YOY) trends, and region-wise sales performace.
3. The dashboard enabled quick, data-informed decisions effectively displaying sales trends and potentially raising revenue by atleast 7% in the next quater.
