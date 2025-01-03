# <span style="color:#2C3E50;">**Data Analysis using SQL for an E-commerce Website**</span>

---

## <span style="color:#34495E;">**Objective**</span>
As a Database Analyst for Maven Fuzzy Factory, an eCommerce start-up, I apply advanced SQL tools and techniques to analyze business performance and uncover insights that drive growth. This project focuses on using data analysis to optimize key business areas, providing actionable insights that support strategic decision-making.

---

## <span style="color:#34495E;">**Project Overview**</span>

### <span style="color:#16A085;">1. [**Traffic-Analysis-and-Optimization**](#traffic-analysis-and-optimization)</span>
In this section, I use MySQL to analyze website traffic sources, evaluating their performance in terms of traffic volume and conversion rates. The goal is to identify patterns and optimize advertising spend by adjusting bids, ensuring better budget allocation for maximum impact.
- [**Analyzing top traffic sources**](#analysing-top-traffic-sources)
- [**Analyzing traffic trend weekly from Google Search**](#analysing-traffic-trend-weekly-from-gsearch)

### <span style="color:#16A085;">2. [**Website Measurement & Testing**](#website-measurement-testing)</span>
In this section, I focus on page-level website data, comparing traffic and conversion rates across different pages. Using MySQL, I build and analyze conversion funnels to gain insights into the customer purchase journey, helping to optimize the user experience and improve conversion rates.
- [**Objective: Analyze Page Views for Different URLs**](#objective-analyze-page-views-for-different-URLs)
- [**Objective: Analyzing Landing Page Performance**](#objective-analyzing-landing-page-performance)
- [**Objective: Conversion Funnel Analysis**](#objective-conversion-funnel-analysis)

### <span style="color:#16A085;">3. [**Channel Analysis & Optimization**](#channel-analysis-optimization)</span>
In this section, I delve into the traffic channel mix, analyzing both paid and free traffic sources. I break down performance by device type and write advanced SQL queries to perform time-series analysis, helping to identify trending patterns and seasonality, ultimately optimizing channel strategy for better ROI.
- [**Objective: Channel Portfolio Analysis**](#objective-channel-portfolio-analysis)
- [**Objective: Cross Channel Bid Optimization**](#cross-channel-bid-optimization)
- [**Objective: Channel Portfolio Trends**](#channel-portfolio-trends)

### <span style="color:#16A085;">4. [**Product-Level Analysis**](#product-level-analysis)</span>
In this section, I use MySQL to analyze product-level sales and conversion rates, identifying cross-selling opportunities and evaluating refund rates to maintain product quality. This analysis provides valuable insights for product optimization and improving overall sales performance.
- [**Objective: Analyzing Order and Revenue Performance by Product**](#analyzing-order-and-revenue-performance)
- [**Objective: Trend Analysis of Products**](#trend-analysis-of-products)
- [**Objective: Product Level Website Analysis**](#product-level-website-analysis)
- [**Objective: Product-Specific Conversion Funnels**](#product-specific-conversion-funnels)
- [**Objective: Understanding Cross-Selling Product Performance**](#understanding-cross-selling-product-performance)
- [**Objective: Analyzing Product Refund Rates**](#analyzing-product-refund-rates)

### <span style="color:#16A085;">5. [**User-Level Analysis**](#user-level-analysis)</span>
In this section, I focus on user behavior and repeat sessions, using MySQL data analysis techniques to identify the most valuable customers. I explore which traffic channels are driving these high-value users, enabling more targeted marketing strategies and improving customer retention.
- [**Objective: Understanding Repeat Visitor Behavior**](#understanding-repeat-visitor-behavior)
- [**Objective: Analyzing Time to Repeat**](#analysing-time-to-repeat)
- [**Objective: Analyzing Repeat Channel Behavior**](#repeat-channel-behavior)
- [**Objective: Analyzing New and Repeat Conversion Rates**](#analyzing-new-and-repeat-conversion-rates)

---

## <span style="color:#34495E;">**Database Schema**</span>
Below is the database schema used for this project. It also has information related to all the tables and columns associated with this project.

![Database Schema](Assets/DBSchema.png)

---

## <span style="color:#34495E;">**Data Dictionary**</span>

### <span style="color:#2980B9;">Table `website_session`</span>
