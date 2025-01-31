# DATA-ANALYSIS-WITH-COMPLEX-QUERIES

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: Pujitha Polumolu

**INTERN ID**: CT12WMWI

**DOMAIN**: SQL

**BATCH DURATION**:  January 15th, 2025 to April 15th, 2025

**MENTOR NAME**: NEELA SANTHOSH

#DESCRIPTION OF THE TASK PERFORMED

he task required me to analyze a dataset containing sales information for a retail company. The dataset included two tables: sale and customer. The sale table contained columns for sale_id, customer_id, sale_date, sales_rep_id, region, and amount. The customer table contained columns for customer_id and signup_date. The goal was to calculate the customer retention rate over time, which involved determining the number of customers who made repeat purchases in each month.
**Approach**:
To solve this task, I employed a combination of window functions, subqueries, and CTEs. Here's an overview of my approach:
1. FirstPurchase CTE: I created a CTE named FirstPurchase to calculate the first purchase date for each customer. This CTE used the MIN aggregation function to determine the earliest sale_date for each customer_id.
2. Retention CTE: I created another CTE named Retention to calculate the number of purchases made by each customer after their first purchase. This CTE joined the sale table with the FirstPurchase CTE on the customer_id column and applied a filter to exclude the first purchase. The CTE then used the DATE_TRUNC function to truncate the sale_date to the month level and counted the number of purchases made by each customer in each month.
3. Final Query: The final query selected the purchase_month and the count of distinct customer_id values from the Retention CTE. The results were grouped by purchase_month and ordered in ascending order.
**Window Functions**:
Although I didn't explicitly use window functions in this task, the DATE_TRUNC function used in the Retention CTE can be considered a type of window function. Window functions allow you to perform calculations across a set of rows that are related to the current row. In this case, the DATE_TRUNC function truncated the sale_date to the month level, allowing me to group the results by month.
**Subqueries**:
I used subqueries in the form of CTEs to break down the problem into smaller, more manageable pieces. The FirstPurchase CTE calculated the first purchase date for each customer, while the Retention CTE calculated the number of purchases made by each customer after their first purchase.
**CTEs**:
CTEs are temporary result sets that you can reference within a query. I used CTEs to simplify the query and make it more readable. The FirstPurchase and Retention CTEs were used to calculate intermediate results, which were then used in the final query to produce the desired output.
**Key Takeaways**:
Through this task, I gained hands-on experience with using window functions, subqueries, and CTEs to solve complex data analysis problems. I learned how to:
Apply window functions to perform calculations across a set of rows related to the current row.Use subqueries in the form of CTEs to break down complex problems into smaller, more manageable pieces.Create CTEs to simplify queries and make them more readable.Apply filters and aggregations to refine the results and extract meaningful insights.
**Conclusion**:
In conclusion, this task allowed me to apply advanced SQL concepts to a real-world scenario, demonstrating my ability to calculate the customer retention rate over time using window functions, subqueries, and CTEs. I gained valuable experience in breaking down complex problems into smaller pieces, applying filters and aggregations, and using CTEs to simplify queries.
**OUTPUT**:
![Image](https://github.com/user-attachments/assets/0cfe40fc-effb-4037-9b6b-1920e3997c9e)

![Image](https://github.com/user-attachments/assets/b65f814f-9e02-4927-8826-9849710bcf9b)

![Image](https://github.com/user-attachments/assets/d8ae2452-3347-4d19-a0b6-922d2f420b89)
