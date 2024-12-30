# **Data Analysis using SQL for an E-commerce Website**

---

## **Objective**
As a Database Analyst for Maven Fuzzy Factory, an eCommerce start-up, I apply advanced SQL tools and techniques to analyze business performance and uncover insights that drive growth. This project focuses on using data analysis to optimize key business areas, providing actionable insights that support strategic decision-making.

## **Project Overview** 

### **Traffic Analysis & Optimization**
In this section, I use MySQL to analyze website traffic sources, evaluating their performance in terms of traffic volume and conversion rates. The goal is to identify patterns and optimize advertising spend by adjusting bids, ensuring better budget allocation for maximum impact.

### **Website Measurement & Testing**  
In this section, I focus on page-level website data, comparing traffic and conversion rates across different pages. Using MySQL, I build and analyze conversion funnels to gain insights into the customer purchase journey, helping to optimize the user experience and improve conversion rates.

### **Channel Analysis & Optimization**  
In this section, I delve into the traffic channel mix, analyzing both paid and free traffic sources. I break down performance by device type and write advanced SQL queries to perform time-series analysis, helping to identify trending patterns and seasonality, ultimately optimizing channel strategy for better ROI.

### **Product-Level Analysis**  
In this section, I use MySQL to analyze product-level sales and conversion rates, identifying cross-selling opportunities and evaluating refund rates to maintain product quality. This analysis provides valuable insights for product optimization and improving overall sales performance.

### **User-Level Analysis**  
In this section, I focus on user behavior and repeat sessions, using MySQL data analysis techniques to identify the most valuable customers. I explore which traffic channels are driving these high-value users, enabling more targeted marketing strategies and improving customer retention.

---

## **Database Schema**
Below is the database schema used for this project. It also has information related to all the tables and columns associated with this project

![Database Schema](Assets/DBSchema.png)

---

### Data Dictionary

| Table Name     | Column Name   | Data Type | Description                      | Constraints       |
|----------------|---------------|-----------|----------------------------------|-------------------|
| `customers`    | `customer_id` | INT       | Unique identifier for customers  | Primary Key       |
| `customers`    | `name`        | VARCHAR   | Name of the customer             |                   |
| `orders`       | `order_id`    | INT       | Unique identifier for orders     | Primary Key       |
| `orders`       | `customer_id` | INT       | Foreign key linking to customers | Foreign Key       |

---

## **Process**
- **SQL Queries**: I wrote complex SQL queries using joins, aggregates, subqueries, and window functions to gather insights from large datasets.
- **Traffic Analysis**: Analyzed sources of traffic and optimized marketing bids using conversion rates.
- **Segmentation**: I segmented users to identify high-value customers.

## **Tools Used**
- SQL (MySQL)

---

[Back to README](README.md)

