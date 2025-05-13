🛍️ E-Commerce Database Project
This project is a simple e-commerce system designed using MySQL, which includes the management of customers, products, and orders. It demonstrates essential relational database concepts including foreign keys, joins, normalization, and aggregate queries.

📁 Database: ecommerce
📦 Tables:
customers – Stores customer information

products – Stores product catalog

orders – Stores customer orders

order_items – (Normalized) Stores line items for each order

🏗️ Schema
customers
Column	Type	Description
id	INT (PK)	Auto-incremented ID
name	VARCHAR	Customer's full name
email	VARCHAR	Customer's email address
address	VARCHAR	Customer's address
products
Column	Type	Description
id	INT (PK)	Auto-incremented ID
name	VARCHAR	Product name
price	DECIMAL	Product price
description	TEXT	Product description
discount	DECIMAL	Product discount (optional)
orders
Column	Type	Description
id	INT (PK)	Auto-incremented ID
customer_id	INT (FK)	Links to customers.id
order_date	DATE	Date order was placed
total_amount	DECIMAL	Total amount of the order
order_items
Column	Type	Description
id	INT (PK)	Auto-incremented ID
order_id	INT (FK)	Links to orders.id
product_id	INT (FK)	Links to products.id
quantity	INT	Number of units ordered
