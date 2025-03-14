# Problem Description:

Retail technology businesses, such as Best Buy, face challenges in efficiently managing inventory, sales transactions, and product categorization. Without an organized database system, these businesses may encounter difficulties such as:
Overstocking or understocking due to poor inventory tracking.
Inefficient sales tracking, leading to unclear insights on employee performance and product demand.
Difficulty in categorizing products, which slows down retrieval and impacts customer service.
Lack of visibility into sales trends, making it harder for management to optimize stock levels and pricing strategies.
To address these challenges, the Electronic Product Database is designed as a comprehensive inventory and sales tracking system. This database will:
Store detailed product information, including descriptions, pricing, warranty periods, and brand associations.
Track real-time inventory status, restock dates, and reorder quantities.
Facilitate sales transactions, recording employee sales contributions, transaction amounts, and payment methods.
Enable sales analysis, allowing management to identify top-selling products, evaluate employee performance, and forecast future demand.
By implementing this database, businesses can improve inventory accuracy, sales efficiency, and data-driven decision-making to enhance overall operations.






# Data Model:
The Electronic Product Database is designed to manage the inventory and sales of an electronics retail business. This data model provides a structured way to store and retrieve information about electronic products, their availability, and their categorization. The electronic_product table serves as the core of the model, linking products to their respective brands and categories through the brand_name and type_of_device tables. Additionally, the inventory table ensures that stock levels and restocking requirements are efficiently tracked, preventing shortages and optimizing supply chain operations.
The sales transaction process is handled through the sales_transaction and sales_transaction_product tables, which record transaction details, payment methods, and the number of products sold. Each sale is associated with an employee, stored in the employee table, allowing management to track individual employee contributions to sales. This structure ensures that every transaction is linked to both the products being sold and the employees processing the sales, making it easier to evaluate performance and analyze revenue trends.
By integrating inventory, sales, and employee management, this database provides businesses with real-time insights into product performance, stock availability, and financial transactions. The structured relationships between tables allow for streamlined data retrieval, enabling managers to make data-driven decisions regarding restocking, sales strategies, and employee performance evaluations. This system ultimately helps improve operational efficiency, profitability, and customer satisfaction by ensuring that products are always available and transactions are accurately recorded.


# Queries:

1. Low Stock / High Stock Alert
This query identifies products with low stock levels and high stock levels to help businesses manage inventory efficiently. The low stock alert retrieves products with a stock quantity of 30 or less, ensuring that managers restock them before they run out. The high stock alert retrieves products with a stock quantity greater than 50, helping managers avoid excessive inventory that could lead to high storage costs or markdowns. Both queries order the results in ascending order of stock quantity for better visibility.





Managers can use this query to maintain balanced stock levels by ensuring that fast-selling products are restocked in time while preventing overstocking of slow-moving items. This helps businesses reduce waste, improve cash flow, and optimize inventory space, leading to better profitability and operational efficiency.



2. Best Selling Products
This query retrieves the top 5 best-selling products based on the total quantity sold. The results are sorted in descending order by sales volume.


Managers can identify high-demand products, allowing them to prioritize restocking and promotional efforts.



3. Total Revenue by Product Category
This query calculates the total sales revenue for each product category while filtering out categories that generate less than the average revenue of all categories. It first groups transactions by product category to compute total revenue and then applies a HAVING clause to retain only those categories that exceed the average revenue. A subquery is used to determine the overall average category revenue, ensuring that the analysis focuses on high-performing product categories.


Managers can use this query to identify high-performing product categories that generate above-average revenue. By filtering out lower-performing categories, businesses can allocate more resources to profitable categories, optimize inventory planning, and adjust marketing strategies for better financial outcomes.


4. Top 3 most profitable brands


If a store wanted to maximize revenue by stocking the brands from which consumers were purchasing most from, this code would be beneficial to visualize which brands sat at the top of the revenue chart.
This query joins the sales transaction, sales transaction for products, electronic product, and brand name tables then groups it by brand name then order by total revenue. Then we set the limit to 3 in order to show only the top 3 brands by revenue.



5. Query 5 shows show each of the employee’s sales performance and gives basic information including their name and employee id



Managers can use this to gauge whether employees are meeting the standards that the company has set for itself. Having a clear and concise table showing the level of performance each employee brings into the company can allow managers to pinpoint those who may need extra assistance, and give the proper guidance for success. Comparing the performance of each employee overtime can allow the managers to make logical decisions to keep employees, fire employees, give bonuses, etc.




6. Monthly Sales TRends
This query displays the year, month, and total sales revenue for each month. The results are grouped by month and sorted in descending order to show the most recent months first.



Managers can use this query to analyze sales trends over time, identifying seasonal patterns and peak sales months. This insight helps businesses make data-driven decisions about inventory management, pricing strategies, and marketing campaigns to maximize revenue.


7. Total Sales Transactions
This query retrieves the total number of transactions in the system.



Gives managers a quick snapshot of overall sales activity.



8. List of All Employees
Retrieves basic employee details, sorted alphabetically by last name.




Provides a quick reference for employee records.


9. 
Most Used Payment Method
Finds the most frequently used payment methods.



Helps managers analyze customer payment preferences.



10. 
The 10th query shows the average transaction value of each customer, meaning the average amount that a customer will spend.



While this code is quite simple, managers can use this in a variety of ways. Taking a sample set of a few months and using it as a barometer for the following months can allow managers to see if there are fluctuations in the amount that customers usually spend. If significant fluctuations occur during certain parts of the year, managers can conclude that their product/service may have a seasonality component to it. If suddenly consumers start spending less, there may be new competition that has entered the market that the manager may be unaware of. If consumers are buying a lot of product, but there’s a disconnect with the transaction value, the product simply may not be priced high enough



# Database Information:

