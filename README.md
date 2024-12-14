# Deli-Meds: Use Case Study Report

## Overview
Deli-Meds is an e-commerce platform designed to sell medicines, products, and services sourced from various pharmacies or through self-channels. The primary goal of the project is to design and implement a robust relational database to store data related to orders, customers, pharmacy operations, and staff interactions. The database serves as a foundation for data-driven decisions, pattern recognition, and recommendation generation for sales and marketing strategies.

## Project Goals
1. **Database Design and Implementation**: Create an Entity-Relationship (EER) and UML model to structure and map the data into a relational database.
2. **Data Storage and Integration**: Implement the database using MySQL and test the feasibility of a NoSQL model using MongoDB.
3. **Python Integration**: Connect the database to Python via Jupyter Notebook for querying, analysis, and visualization.
4. **Insights and Visualization**: Generate insights from stored data to provide recommendations and decision-making support.

## Business Requirements
- Customers must have a prescription to add items to the cart.
- A pharmacy can:
  - Provide medicines.
  - List their services.
  - Sell products.
- Customers can pay in single or multiple settlements.
- Staff can interact with customers to address queries and escalate issues.
- Key relationships include:
  - Customer to Orders.
  - Pharmacy to Inventory (Medicines, Products, Services).
  - Interactions between Customers, Staff, and Queries.

## Data Model
### UML Diagram
- Unified Modeling Language diagram provides an overview of entities and their relationships.

### EER Diagram
- Represents relationships, including ternary and aggregation relationships for better understanding.

### Relational Model Mapping
Primary and foreign keys were defined for tables such as:
- **Customer**
- **Pharmacy**
- **Medicine**
- **Service**
- **Product**
- **Order**
- **Staff**
- **Interaction**
- **Delivery**

### Highlights
- **Ternary Relationships**: Prescription (Customer, Doctor, Cart) and Delivery (Staff, Pharmacy, Order).
- **Specialization**: Staff categorized into Customer Care and Delivery Personnel.

## Implementation
### MySQL
The database schema was implemented in MySQL with queries to:
1. Find the average payment by customers.
2. Retrieve staff names and departments.
3. Display order details with customer names.
4. Perform joins between tables like Medicine and Pharmacy.
5. Calculate total interaction durations.

### MongoDB (NoSQL)
A MongoDB test database named `deli_meds` was created by importing JSON data from MySQL tables. Key queries include:
- Fetching medicines based on price and name patterns.
- Aggregating counts of employees by job titles and office codes.

## Python Integration
The database is accessed via Python using the `mysql.connector` library, and data is visualized using `matplotlib` and `pandas`. Sample visualizations include:
- **Top 10 Customers** based on average spending.
- **Cart Conversion** rates to orders.
- **Customers with the Highest Interaction Duration**.

## Recommendations
1. Enhance data integrity by adding views and triggers.
2. Enable prescription scanning for a seamless ordering experience.
3. Transition to a NoSQL-based system for improved scalability and flexibility in data retrieval.

## Future Scope
- Integration of advanced analytics and machine learning for personalized recommendations.
- Support for pharmacy specialization (e.g., telehealth services, orthopedic care).
- Scalability improvements for large datasets using NoSQL models.

---
**Authors**:
- Yaswanth Reddy Nalamalapu
- Venkata Mani Sivasai Shanmukha Goparaju

**Tools Used**: MySQL, MongoDB, Python (Jupyter Notebook), Matplotlib, Pandas
