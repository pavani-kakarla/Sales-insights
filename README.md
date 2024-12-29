# Sales-Insights-Data-Analysis-Project
## Data Analysis Using SQL
1. Show all customers records
2. ![Screenshot 2024-12-29 191546](https://github.com/user-attachments/assets/aad24f24-1582-4ec9-b378-68846865e5d6)
3. Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";


   

