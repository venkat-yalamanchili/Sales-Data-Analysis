
# Sales & Profit Performance Analytics (Star Schema Power BI Project)

## Project Overview

This project delivers an end-to-end Business Intelligence solution designed to analyze sales performance, profitability, and customer behavior across various dimensions. Built using **Power BI** and structured around a robust **Star Schema Data Model**, this project transforms raw transactional data into actionable insights, enabling stakeholders to make data-driven decisions.

The core focus of this project is demonstrating advanced data modeling techniques, dual-period temporal analysis, and highly interactive reporting layouts.

## Data Model Architecture (Star Schema)

To ensure optimal performance, scalability, and intuitive DAX calculations, the data model is strictly organized into a **Star Schema** with a central fact table surrounded by dimension tables.

-   **Fact Table:** `Facts table` (Contains transactional records like Net Sales, Quantity, Profit, Discount Values, and keys).
    
-   **Dimension Tables:** * `Dim Product` (Product hierarchies, Pricing per unit, Product lines).
    
    -   `Dim Customers` (Customer names, contact details, and geographic locations like City/State).
        
    -   `Dim Promotion` (Promotion campaigns, coupon codes, and discount categories).
        
    -   `Date Table 1` & `Date Table 2` (Disconnected date dimensions optimized for advanced period-over-period comparisons).
        

## Business Questions Answered

### 1. Product Performance Analysis

-   **Top/Bottom 5 Products:** Dynamically isolates the top 5 and bottom 5 performing products across three critical business metrics: **Sales**, **Profit**, and **Quantity Sold**.
    
-   _Insight:_ This identifies core revenue drivers (e.g., Apple iPhone 14, MacBook Air) versus low-performing stock-keeping units (SKUs) requiring strategic clearance.
    

### 2. Temporal Sales Trends

-   **Sales Trends Over Time:** Evaluates high-level and granular sales fluctuations across the entire operational timeline (daily, monthly, quarterly, and annually) to uncover seasonal spikes and structural dips.
    

### 3. Financial Correlation

-   **Sales vs. Profit Relationship:** Features a scatter plot detailing the direct linear correlation between Net Sales and Profit margins, assisting in pricing strategy evaluation.
    

### 4. Dual-Period Comparative Analysis

-   **Time-Period Comparison:** Implements an advanced comparison mechanism using disconnected date tables. Users can filter and compare **Total Sales**, **Total Profit**, and **Quantity Sold** between any two custom-selected date ranges simultaneously.
    

### 5. Promotion & Discount Optimization

-   **Average Discount by Category:** Evaluates the impact and average depth of discounts offered across various promotion segments (e.g., Weekend Flash Sale, Clearance Sale, Festive Diwali) to spot promotional efficiency.
    

### 6. Key Operational Metrics

-   **Total Orders Tracker:** Displays a high-level executive KPI card summarizing the total volume of orders processed ($3.51\text{K}$ total orders).
    

### 7. Granular Auditing & Reporting

-   **Dynamic Order Transaction Matrix:** Provides a comprehensive transactional ledger detailing Sales, Profit, Discounts, and Net Sales at the individual order level. Fully filterable by Product, Date, Customer ID, and Promotion Categories.
    

### 8. Geographic Performance

-   **Sales by City:** Uses geospatial mapping to plot revenue concentration across major regional hubs (including Delhi, Mumbai, Bangalore, Jaipur, etc.).
    

## Dashboard Layout & Features

### Page 1: Executive Performance Overview

Focuses on high-level operational health metrics, geographic sales distribution, macro time trends, and promotional discount breakdowns.

-   _Key Visuals:_ Geospatial Sales Map, Total Orders KPI, Promotion Horizontal Bar Chart, Profit vs. Net Sales Scatter Plot, and the Macro Line Chart for temporal trends.
    

### Page 2: Product Performance Deep Dive

A dedicated catalog assessment view displaying side-by-side performance hierarchies.

-   _Key Visuals:_ Comparative purple and red bar charts highlighting the structural dichotomy between top revenue generators and underperforming products.
    

### Page 3: Advanced Period-Over-Period Comparison

Empowers business analysts to run custom timeline scenarios.

-   _Key Visuals:_ Dual interactive date sliders (`Date Filter 1` and `Date Filter 2`) side-by-side with multi-series bar charts comparing dynamic sales variations.
    

### Page 4: Order Ledger & Granular Filter Matrix

A detailed raw-audit view built for operational drilling.

-   _Key Visuals:_ Filter slices for Customer, Product, Promotion, and State feeding into a comprehensive tabular transaction matrix.
    

## DAX & Modeling Techniques Used

-   **Star Schema Optimization:** Modeled clean $1:\infty$ (one-to-many) unidirectional relationships to prevent ambiguity and optimize engine performance.
    
-   **Disconnected Table Trick:** Implemented a secondary independent date table to handle dual-range comparison slicers without cross-filtering interference.
    
-   **Explicit Measures Table:** Grouped all core calculations (`Total Profit`, `Total Sales`, `Total quantity`, etc.) inside a dedicated `Measures Table` for clean repository maintenance.
    

## How to View and Run the Project

1.  Clone this repository to your local machine.
    
2.  Install the latest version of [Power BI Desktop](https://powerbi.microsoft.com/).
    
3.  Open the `.pbix` file contained within this repository.
    
4.  Interact with the slicers across the pages to explore live data cross-filtering
