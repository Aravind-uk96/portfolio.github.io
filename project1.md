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

## **Data Dictionary**

### Table `website_session`

| Column Name          | Data Type       | Description                      |
|-----------------------|-----------------|----------------------------------|
| website_session_id    | BIGINT          | Unique identifier for the session |
| created_at            | DATETIME        | Session creation date and time   |
| user_id               | BIGINT          | Identifier for the user          |
| is_repeat_session     | BINARY          | Indicates if it's a repeat session |
| utm_source            | VARCHAR(45)     | Source of the traffic            |
| utm_campaign          | VARCHAR(45)     | Campaign name in marketing       |
| utm_content           | VARCHAR(45)     | Content identifier in marketing  |
| device_type           | VARCHAR(45)     | Type of device used              |
| http_referer          | VARCHAR(45)     | HTTP referrer link               |


### Table `website_pageviews Table`

| Column Name          | Data Type       | Description                          |
|-----------------------|-----------------|--------------------------------------|
| website_pageview_id  | BIGINT          | Unique identifier for the pageview   |
| created_at           | DATETIME        | Pageview creation date and time      |
| website_session_id   | BIGINT          | Identifier for the associated session|
| pageview_url         | VARCHAR(45)     | URL of the page viewed               |


### Table `orders Table`

| Column Name          | Data Type       | Description                          |
|-----------------------|-----------------|--------------------------------------|
| order_id             | BIGINT          | Unique identifier for the order      |
| created_at           | DATETIME        | Order creation date and time         |
| website_session_id   | BIGINT          | Identifier for the associated session|
| user_id              | BIGINT          | Identifier for the user placing order|
| primary_product_id   | INT             | Identifier for the primary product   |
| items_purchased      | INT             | Total items purchased in the order   |
| price_usd            | DECIMAL(6,2)    | Total price in USD                   |
| cogs_usd             | DECIMAL(6,2)    | Cost of goods sold in USD            |

### Table `products Table`

| Column Name          | Data Type       | Description                          |
|-----------------------|-----------------|--------------------------------------|
| product_id           | INT             | Unique identifier for the product    |
| created_at           | DATETIME        | Product creation date and time       |
| product_name         | VARCHAR(45)     | Name of the product                  |

### Table `order_items Table`

| Column Name          | Data Type       | Description                          |
|-----------------------|-----------------|--------------------------------------|
| order_item_id        | BIGINT          | Unique identifier for the order item |
| created_at           | DATETIME        | Order item creation date and time    |
| order_id             | BIGINT          | Identifier for the associated order  |
| product_id           | INT             | Identifier for the product in the order |
| is_primary_item      | BINARY          | Indicates if this is the primary item |
| price_usd            | DECIMAL(6,2)    | Price of the order item in USD       |
| cogs_usd             | DECIMAL(6,2)    | Cost of goods sold for this item in USD |

### Table `order_item_refunds Table`

| Column Name          | Data Type       | Description                          |
|-----------------------|-----------------|--------------------------------------|
| order_item_refund_id | BIGINT          | Unique identifier for the refund     |
| created_at           | DATETIME        | Refund creation date and time        |
| order_item_id        | BIGINT          | Identifier for the refunded order item |
| refund_amount_usd    | DECIMAL(6,2)    | Amount refunded in USD               |

---

## **Process**
- **SQL Queries**: I wrote complex SQL queries using joins, aggregates, subqueries, and window functions to gather insights from large datasets.
- **Traffic Analysis**: Analyzed sources of traffic and optimized marketing bids using conversion rates.
- **Segmentation**: I segmented users to identify high-value customers.

## **Tools Used**
- SQL (MySQL)

---

[Back to README](README.md)

