#📊 E-Commerce Analytics on Databricks

This project demonstrates how to model and analyze an E-Commerce Platform using Databricks Delta Tables.
The system is designed to capture real-world workflows, where:

Customers place orders.

Each order can contain multiple products.

Products belong to categories.

Orders go through statuses such as Placed → Shipped → Delivered.

#🏗️ Data Model

The data is organized into relational tables under the Datax schema:

Customers → Stores customer information (profile, contact, location).

Products → Catalog of products with details and assigned categories.

Categories → Classification of products into meaningful groups.

Orders → Tracks customer purchases and their statuses.

Order_Items → Line-level details of products purchased in each order.

Relationships:

A Customer can place many Orders.

Each Order can have multiple Order_Items.

An Order_Item always points to a Product.

A Product belongs to one Category.

#📌 Key Insights

The SQL queries provided inside the notebooks generate valuable business insights, including:

Top 5 Customers by Total Spending

Identifies the most valuable customers based on purchase amounts.

Most Sold Product by Quantity

Finds the product with the highest sales volume.

Pending Deliveries

Lists orders that are still in “Placed” or “Shipped” status.

Revenue Trend by Month

Tracks revenue growth and seasonality across months.

#🚀 Why This Project?

Hands-On Practice: Simulates real-world e-commerce scenarios.

Reusability: Queries are written to be modular and extensible.

Scalability: Designed to grow into a Bronze → Silver → Gold pipeline.

Business Value: Provides insights useful for decision making in marketing, sales, and operations.