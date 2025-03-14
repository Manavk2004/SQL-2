# MIST4610-Project1-Group7

# Group Members:
1. Kamdar, Manav @Manavk2004
2. Allmond, Chandler @chandlerallmond
3. Barton, Nick @nicholasbarton1
4. Sengaphone, Vincent @sengaphone
5. Wilson, Landon @landonnn0


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




# Data Dictionary:

<img width="900" alt="Screenshot 2025-03-14 at 4 27 11 PM" src="https://github.com/user-attachments/assets/54d3ea60-55ce-468c-bd8f-d4a1587c3c25" />

<img width="900" alt="Screenshot 2025-03-14 at 4 27 30 PM" src="https://github.com/user-attachments/assets/e850d17e-dc89-4bd5-a0e9-cad09f64fc00" />

<img width="900" alt="Screenshot 2025-03-14 at 4 27 49 PM" src="https://github.com/user-attachments/assets/a7ead587-a36c-48bc-926b-4c2119db7438" />

<img width="900" alt="Screenshot 2025-03-14 at 4 28 02 PM" src="https://github.com/user-attachments/assets/0e1111be-edbb-4a08-ba0c-39e4ca2c166f" />

<img width="900" alt="Screenshot 2025-03-14 at 4 28 31 PM" src="https://github.com/user-attachments/assets/15f1edd4-d043-40f9-96b1-e32c4044bc88" />

<img width="900" alt="Screenshot 2025-03-14 at 4 28 44 PM" src="https://github.com/user-attachments/assets/cda61e04-600d-4524-8fbc-cceca1d123e4" />

<img width="900" alt="Screenshot 2025-03-14 at 4 29 00 PM" src="https://github.com/user-attachments/assets/fae6dc27-e253-4a7d-93a1-b269e4158d8f" />






# Queries:

1. Low Stock / High Stock Alert
This query identifies products with low stock levels and high stock levels to help businesses manage inventory efficiently. The low stock alert retrieves products with a stock quantity of 30 or less, ensuring that managers restock them before they run out. The high stock alert retrieves products with a stock quantity greater than 50, helping managers avoid excessive inventory that could lead to high storage costs or markdowns. Both queries order the results in ascending order of stock quantity for better visibility.


<img width="900" alt="Screenshot 2025-03-14 at 4 29 14 PM" src="https://github.com/user-attachments/assets/b47ae4be-73c0-48ff-817b-e4cdfa092356" />



Managers can use this query to maintain balanced stock levels by ensuring that fast-selling products are restocked in time while preventing overstocking of slow-moving items. This helps businesses reduce waste, improve cash flow, and optimize inventory space, leading to better profitability and operational efficiency.



2. Best Selling Products
This query retrieves the top 5 best-selling products based on the total quantity sold. The results are sorted in descending order by sales volume.

<img width="900" alt="Screenshot 2025-03-14 at 4 29 30 PM" src="https://github.com/user-attachments/assets/c3562191-3540-4e07-89bd-58cdc50538ad" />

Managers can identify high-demand products, allowing them to prioritize restocking and promotional efforts.



3. Total Revenue by Product Category
This query calculates the total sales revenue for each product category while filtering out categories that generate less than the average revenue of all categories. It first groups transactions by product category to compute total revenue and then applies a HAVING clause to retain only those categories that exceed the average revenue. A subquery is used to determine the overall average category revenue, ensuring that the analysis focuses on high-performing product categories.


<img width="900" alt="Screenshot 2025-03-14 at 4 30 00 PM" src="https://github.com/user-attachments/assets/fdc630c6-f088-4831-a9cd-6b732536e44e" />


Managers can use this query to identify high-performing product categories that generate above-average revenue. By filtering out lower-performing categories, businesses can allocate more resources to profitable categories, optimize inventory planning, and adjust marketing strategies for better financial outcomes.


4. Top 3 most profitable brands

<img width="900" alt="Screenshot 2025-03-14 at 4 30 19 PM" src="https://github.com/user-attachments/assets/d7d05d94-949e-4c43-8620-62a3196a46bf" />

If a store wanted to maximize revenue by stocking the brands from which consumers were purchasing most from, this code would be beneficial to visualize which brands sat at the top of the revenue chart.
This query joins the sales transaction, sales transaction for products, electronic product, and brand name tables then groups it by brand name then order by total revenue. Then we set the limit to 3 in order to show only the top 3 brands by revenue.



5. Query 5 shows show each of the employee’s sales performance and gives basic information including their name and employee id

<img width="900" alt="Screenshot 2025-03-14 at 4 30 34 PM" src="https://github.com/user-attachments/assets/7bbc6dab-0d61-44eb-b0cb-c63c50d18a1f" />


Managers can use this to gauge whether employees are meeting the standards that the company has set for itself. Having a clear and concise table showing the level of performance each employee brings into the company can allow managers to pinpoint those who may need extra assistance, and give the proper guidance for success. Comparing the performance of each employee overtime can allow the managers to make logical decisions to keep employees, fire employees, give bonuses, etc.




6. Monthly Sales TRends
This query displays the year, month, and total sales revenue for each month. The results are grouped by month and sorted in descending order to show the most recent months first.


<img width="900" alt="Screenshot 2025-03-14 at 4 30 49 PM" src="https://github.com/user-attachments/assets/5e0a5d52-1e40-4d7b-8896-9e7039a62e65" />

Managers can use this query to analyze sales trends over time, identifying seasonal patterns and peak sales months. This insight helps businesses make data-driven decisions about inventory management, pricing strategies, and marketing campaigns to maximize revenue.


7. Total Sales Transactions
This query retrieves the total number of transactions in the system.

<img width="900" alt="Screenshot 2025-03-14 at 4 31 08 PM" src="https://github.com/user-attachments/assets/77eb39ba-696f-422d-a247-bd8d5631a1f4" />


Gives managers a quick snapshot of overall sales activity.



8. List of All Employees
Retrieves basic employee details, sorted alphabetically by last name.

<img width="900" alt="Screenshot 2025-03-14 at 4 31 22 PM" src="https://github.com/user-attachments/assets/0212bfb7-2794-4d34-a1c3-6606d864553c" />



Provides a quick reference for employee records.


9. 
Most Used Payment Method
Finds the most frequently used payment methods.

<img width="900" alt="Screenshot 2025-03-14 at 4 31 35 PM" src="https://github.com/user-attachments/assets/0399710c-bf59-4182-92c4-ff09c3077e27" />


Helps managers analyze customer payment preferences.



10. 
The 10th query shows the average transaction value of each customer, meaning the average amount that a customer will spend.

<img width="900" alt="Screenshot 2025-03-14 at 4 31 47 PM" src="https://github.com/user-attachments/assets/dc1fa8ec-4a7e-47a2-99e6-998290076049" />


While this code is quite simple, managers can use this in a variety of ways. Taking a sample set of a few months and using it as a barometer for the following months can allow managers to see if there are fluctuations in the amount that customers usually spend. If significant fluctuations occur during certain parts of the year, managers can conclude that their product/service may have a seasonality component to it. If suddenly consumers start spending less, there may be new competition that has entered the market that the manager may be unaware of. If consumers are buying a lot of product, but there’s a disconnect with the transaction value, the product simply may not be priced high enough



# Database Information:


<img width="900" alt="Screenshot 2025-03-14 at 4 32 01 PM" src="https://github.com/user-attachments/assets/21fb6d59-b646-4ade-8d13-9108645515df" />

