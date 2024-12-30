# **Data Analysis using SQL for an E-commerce Website**

---

## **Objective**
As a Database Analyst for Maven Fuzzy Factory, an eCommerce start-up, I apply advanced SQL tools and techniques to analyze business performance and uncover insights that drive growth. This project focuses on using data analysis to optimize key business areas, providing actionable insights that support strategic decision-making.

## **Project Overview** 

### [**Traffic Analysis & Optimization**](#Traffic-Analysis-and-Optimization)
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

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">website_session_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the session</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Session creation date and time</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">user_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Identifier for the user</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">is_repeat_session</td>
      <td style="border: 1px solid black; padding: 5px;">BINARY</td>
      <td style="border: 1px solid black; padding: 5px;">Indicates if it's a repeat session</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">utm_source</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">Source of the traffic</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">utm_campaign</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">Marketing campaign details</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">utm_content</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">Content details</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">device_type</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">Type of device used</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">http_referer</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">HTTP referrer</td>
    </tr>
  </tbody>
</table>


### Table `website_pageviews`

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">website_pageview_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the pageview</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Pageview creation date and time</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">website_session_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Associated session identifier</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">pageview_url</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">URL of the page viewed</td>
    </tr>
  </tbody>
</table>


### Table `orders`

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_item_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the order item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Creation date and time of the order item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Identifier for the associated order</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">product_id</td>
      <td style="border: 1px solid black; padding: 5px;">INT</td>
      <td style="border: 1px solid black; padding: 5px;">Identifier for the associated product</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">is_primary_item</td>
      <td style="border: 1px solid black; padding: 5px;">BINARY</td>
      <td style="border: 1px solid black; padding: 5px;">Indicates if this is the primary item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">price_usd</td>
      <td style="border: 1px solid black; padding: 5px;">DECIMAL(6,2)</td>
      <td style="border: 1px solid black; padding: 5px;">Price in USD</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">cogs_usd</td>
      <td style="border: 1px solid black; padding: 5px;">DECIMAL(6,2)</td>
      <td style="border: 1px solid black; padding: 5px;">Cost of goods sold in USD</td>
    </tr>
  </tbody>
</table>

### Table `products`

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">product_id</td>
      <td style="border: 1px solid black; padding: 5px;">INT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the product</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Product creation date and time</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">product_name</td>
      <td style="border: 1px solid black; padding: 5px;">VARCHAR(45)</td>
      <td style="border: 1px solid black; padding: 5px;">Name of the product</td>
    </tr>
  </tbody>
</table>

### Table `order_items`

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_item_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the order item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Creation date and time of the order item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Identifier for the associated order</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">product_id</td>
      <td style="border: 1px solid black; padding: 5px;">INT</td>
      <td style="border: 1px solid black; padding: 5px;">Identifier for the associated product</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">is_primary_item</td>
      <td style="border: 1px solid black; padding: 5px;">BINARY</td>
      <td style="border: 1px solid black; padding: 5px;">Indicates if this is the primary item</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">price_usd</td>
      <td style="border: 1px solid black; padding: 5px;">DECIMAL(6,2)</td>
      <td style="border: 1px solid black; padding: 5px;">Price in USD</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">cogs_usd</td>
      <td style="border: 1px solid black; padding: 5px;">DECIMAL(6,2)</td>
      <td style="border: 1px solid black; padding: 5px;">Cost of goods sold in USD</td>
    </tr>
  </tbody>
</table>


### Table `order_item_refunds`

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">Column Name</th>
      <th style="border: 1px solid black; padding: 5px;">Data Type</th>
      <th style="border: 1px solid black; padding: 5px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_item_refund_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Unique identifier for the refund</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">created_at</td>
      <td style="border: 1px solid black; padding: 5px;">DATETIME</td>
      <td style="border: 1px solid black; padding: 5px;">Refund creation date and time</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">order_item_id</td>
      <td style="border: 1px solid black; padding: 5px;">BIGINT</td>
      <td style="border: 1px solid black; padding: 5px;">Associated order item identifier</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">refund_amount_usd</td>
      <td style="border: 1px solid black; padding: 5px;">DECIMAL(6,2)</td>
      <td style="border: 1px solid black; padding: 5px;">Refund amount in USD</td>
    </tr>
  </tbody>
</table>


---


## Traffic Analysis and Optimization

### Objective - Analysing top traffic sources
  To understand customer acquisition sources, analyze conversion rates, and optimize marketing efforts by identifying high-performing traffic patterns and opportunities to improve budget allocation.
  
  
### Key Questions Addressed
  1. **Where are customers coming from?**  
  2. **What are the conversion rates for specific traffic patterns?**  
  
  
### Why This Analysis is Important
  - **Budget Optimization**:  
    - Shift budgets towards traffic sources driving the strongest conversion rates.  
    - Scale high-performing campaigns to maximize ROI.  
  - **Eliminating Wasteful Spend**:  
    - Identify low-converting traffic sources and reallocate resources effectively.  
  
  
### Tools and Data Sources
  - **Tables Used**:  
    - `Website_sessions`  
    - `Website_pageviews`  
    - `Orders`  
  
  - **Key Insights**:  
    - Paid traffic is tagged with **UTM (Urchin Tracking Module) parameters**.  
    - UTM parameters are appended to URLs to track specific traffic sources and campaigns.  


### Steps in the Analysis

1. **Traffic Source Identification**  
   - Use **UTM parameters** to classify and segment traffic sources

2. **Count the number of orders and website session id's**

3. **Conversion Rate Analysis**  
   - Calculate conversion rates for each traffic source using:  
     ```
     Conversion Rate = (Number of Orders) / (Website Sessions)
     ```

### SQL code for the query
```sql
SELECT
    website_sessions.utm_content,
    COUNT(DISTINCT website_sessions.website_session_id) AS sessions,
    COUNT(DISTINCT orders.order_id) AS orders,
    COUNT(DISTINCT orders.order_id) / COUNT(DISTINCT website_sessions.website_session_id) AS session_to_order_conversion_rate
FROM
    website_sessions
    LEFT JOIN orders
        ON website_sessions.website_session_id = orders.website_session_id
WHERE
    website_sessions.website_session_id BETWEEN 1000 AND 2000
GROUP BY
    website_sessions.utm_content
ORDER BY
    COUNT(DISTINCT website_sessions.website_session_id) DESC;
```
### Sample Output

<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">utm_content</th>
      <th style="border: 1px solid black; padding: 5px;">sessions</th>
      <th style="border: 1px solid black; padding: 5px;">orders</th>
      <th style="border: 1px solid black; padding: 5px;">sessions_to_order_conversion_rate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">g_ad_1</td>
      <td style="border: 1px solid black; padding: 5px;">975</td>
      <td style="border: 1px solid black; padding: 5px;">35</td>
      <td style="border: 1px solid black; padding: 5px;">0.0359</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">NULL</td>
      <td style="border: 1px solid black; padding: 5px;">18</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">g_as_2</td>
      <td style="border: 1px solid black; padding: 5px;">6</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">b_ad_2</td>
      <td style="border: 1px solid black; padding: 5px;">2</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
      <td style="border: 1px solid black; padding: 5px;">0</td>
    </tr>
  </tbody>
</table>

### **Key Findings**
1. **High-Performing Campaign (`g_ad_1`)**:
   - Achieved a conversion rate of **3.59%**, generating **35 orders** from **975 sessions**.
   - Clearly the standout campaign, demonstrating strong ROI and scalability potential.

2. **Organic Traffic (`NULL`)**:
   - Represented **18 sessions** with **0% conversion rate**.
   - Highlights a need to optimize organic landing pages and improve SEO strategies.

3. **Low-Performing Campaigns (`g_as_2` and `b_ad_2`)**:
   - Both campaigns had negligible traffic and **0% conversion rates**.
   - Likely suffer from poor targeting, ineffective ad content, or insufficient reach.

### **Recommendations**
1. **Scale High-Performing Campaigns**:
   - Allocate more budget to campaign `g_ad_1` to maximize conversions and revenue growth.

2. **Optimize Organic Traffic**:
   - Evaluate landing pages and align content with user intent to improve conversion rates from organic traffic.
   - Enhance SEO strategies to attract more relevant traffic.

3. **Review Low-Performing Campaigns**:
   - Reassess the targeting, messaging, and reach of `g_as_2` and `b_ad_2`.
   - Pause these campaigns if improvements cannot be achieved, and redirect funds to higher-performing campaigns.

---


### **Objective: Analysing traffic trend weekly from gsearch**

*   Analyze website traffic trends over time, specifically for filtered UTM parameters (e.g., source and campaign).
*   Identify weekly fluctuations in website sessions.

### **Key Questions:**

*   How many website sessions are we getting each week for the specified UTM parameters?
*   Are there any significant increases or decreases in sessions week over week?

### **Data Sources and Tools:**

*   **Data Source:** Website session data (e.g., `website_sessions`).
*   **Key Data Points:** `created_at`, `website_session_id`, `utm_source`, `utm_campaign`.
*   **Tools:** SQL, Data visualization tools (for trend analysis).

### **Analysis Steps (Process):**

1.  **Data Filtering:** Filter the `website_sessions` table based on the desired UTM parameters (e.g., `utm_source = 'gsearch'` and `utm_campaign = 'nonbrand'`).

2.  **Weekly Aggregation:**
    *   Extract the year and week number from the `created_at` timestamp.
    *   Determine the start date of each week.
    *   Count the distinct website sessions for each week.

3.  **Trend Analysis:**
    *   Analyze the weekly session counts to identify trends (e.g., increasing, decreasing, seasonal patterns).
    *   Calculate week-over-week changes (percentage or absolute difference).

### **SQL code for this analysis**

```sql
SELECT
    YEAR(created_at) AS yr,
    WEEK(created_at) AS wk,
    MIN(DATE(created_at)) AS week_started_at,
    COUNT(DISTINCT website_session_id) AS sessions
FROM
    website_sessions
WHERE
    created_at < '2012-05-12' -- Your original date filter
    AND utm_source = 'gsearch' -- Your UTM filters
    AND utm_campaign = 'nonbrand'
GROUP BY
    YEAR(created_at),
    WEEK(created_at)
ORDER BY
    yr, wk; -- Order by year and week
```

### **Output**
<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">yr</th>
      <th style="border: 1px solid black; padding: 5px;">wk</th>
      <th style="border: 1px solid black; padding: 5px;">week_started_at</th>
      <th style="border: 1px solid black; padding: 5px;">sessions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">12</td>
      <td style="border: 1px solid black; padding: 5px;">3/19/2012</td>
      <td style="border: 1px solid black; padding: 5px;">896</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">13</td>
      <td style="border: 1px solid black; padding: 5px;">3/25/2012</td>
      <td style="border: 1px solid black; padding: 5px;">956</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">14</td>
      <td style="border: 1px solid black; padding: 5px;">4/1/2012</td>
      <td style="border: 1px solid black; padding: 5px;">1152</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">15</td>
      <td style="border: 1px solid black; padding: 5px;">4/8/2012</td>
      <td style="border: 1px solid black; padding: 5px;">983</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">16</td>
      <td style="border: 1px solid black; padding: 5px;">4/15/2012</td>
      <td style="border: 1px solid black; padding: 5px;">621</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">17</td>
      <td style="border: 1px solid black; padding: 5px;">4/22/2012</td>
      <td style="border: 1px solid black; padding: 5px;">594</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">18</td>
      <td style="border: 1px solid black; padding: 5px;">4/29/2012</td>
      <td style="border: 1px solid black; padding: 5px;">681</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">2012</td>
      <td style="border: 1px solid black; padding: 5px;">19</td>
      <td style="border: 1px solid black; padding: 5px;">5/6/2012</td>
      <td style="border: 1px solid black; padding: 5px;">651</td>
    </tr>
  </tbody>
</table>

### **Actionable Recommendations**

*   **Identifying Peaks and Dips:** If there are significant peaks or dips in sessions, investigate the possible causes (e.g., marketing campaigns, seasonality, external events).
*   **Forecast Future Traffic:** Use historical trends to forecast future traffic and plan accordingly.

---


### **Objective: Analyze Page Views for Different URLs**

*   Analyze page views across various website URLs.
*   Identify the most visited pages on the website.

### **Key Questions:**

*   What are the most visited pages on the website?
*   How can we optimize the website's structure based on user behavior?

### **Data Sources and Tools:**

*   **Data Source:** Website pageview data (e.g., `website_pageviews`).
*   **Key Data Points:** `pageview_url`, `website_pageview_id`, `created_at`.
*   **Tools:** SQL, Data visualization tools (for insights).

### **Analysis Steps (Process):**

1.  **Data Aggregation:** Group the data by `pageview_url` and count distinct `website_pageview_id`.
2.  **Filtering:** Apply a date filter to exclude data after `'2012-06-09'`.
3.  **Ranking:** Sort the URLs by the total number of page views in descending order.

### **SQL Code for this Analysis**

```sql
SELECT
    pageview_url,
    COUNT(DISTINCT website_pageview_id) AS page_views
FROM
    website_pageviews
WHERE
    created_at < '2012-06-09'
GROUP BY
    pageview_url
ORDER BY
    page_views DESC;
```
###**Output**
<table style="border: 1px solid black; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid black; padding: 5px;">pageview_url</th>
      <th style="border: 1px solid black; padding: 5px;">page_views</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/home</td>
      <td style="border: 1px solid black; padding: 5px;">10403</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/products</td>
      <td style="border: 1px solid black; padding: 5px;">4239</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/the-original-mr-fuzzy</td>
      <td style="border: 1px solid black; padding: 5px;">3037</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/cart</td>
      <td style="border: 1px solid black; padding: 5px;">1306</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/shipping</td>
      <td style="border: 1px solid black; padding: 5px;">869</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/billing</td>
      <td style="border: 1px solid black; padding: 5px;">716</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">/thank-you-for-your-order</td>
      <td style="border: 1px solid black; padding: 5px;">306</td>
    </tr>
  </tbody>
</table>

### **Actionable Recommendations**

*  **Optimize High-Traffic Pages: Ensure that pages like /home and /products provide a seamless user experience and prominently feature key information.
*  **Improve Low-Traffic Pages: Review pages like /thank-you-for-your-order for potential enhancements to encourage user engagement.
*  **Strategic Content Placement: Use high-performing pages as platforms for driving traffic to other parts of the website.




---

[Back to README](README.md)

