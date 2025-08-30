# 📊 **E-Commerce Analytics on Databricks**

This project showcases how to model and analyze an **E-Commerce Platform** using **Databricks Delta Tables**.  
The workflow is inspired by real-world online shopping systems where:  
- **Customers** place **Orders**  
- **Orders** contain multiple **Products**  
- **Products** belong to specific **Categories**  
- Orders progress through statuses like **Placed → Shipped → Delivered**

---

## 🏗️ **Data Model**

The database is structured into multiple tables under the **Datax schema**:

- **Customers** → Stores customer details (profile, contact, city).  
- **Products** → Contains product information with assigned categories.  
- **Categories** → Groups products into categories for easy classification.  
- **Orders** → Tracks purchase history and order statuses.  
- **Order_Items** → Records line-level details of products purchased per order.  

**Relationships:**  
- A **Customer** can place many **Orders**  
- Each **Order** can have multiple **Order_Items**  
- An **Order_Item** always refers to a **Product**  
- A **Product** belongs to one **Category**

---

## 📌 **Key Business Insights**

The notebooks contain reusable SQL queries that generate insights such as:  

1. **Top 5 Customers by Spending** → Identify your most valuable buyers.  
2. **Most Sold Product** → Find which product has the highest demand.  
3. **Pending Deliveries** → Track orders still awaiting shipment or delivery.  
4. **Revenue by Month** → Analyze sales trends and seasonal growth.  

---

## 🚀 **Why This Project?**

- **Hands-On Learning**: Builds a real-world e-commerce workflow.  
- **Reusability**: Queries are modular and can be extended easily.  
- **Scalability**: Structured to fit into a **Bronze → Silver → Gold** pipeline.  
- **Business Value**: Delivers insights that aid **marketing, sales, and operations** decisions.  

---

## 🖼️ **Visual ERD (Entity-Relationship Diagram)**

```mermaid
erDiagram
    CUSTOMERS ||--o{ ORDERS : places
    ORDERS ||--o{ ORDER_ITEMS : contains
    PRODUCTS ||--o{ ORDER_ITEMS : listed_in
    PRODUCTS }o--|| CATEGORIES : classified_into
