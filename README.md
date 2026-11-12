# Super Store Retail Sales Analytics Dashboard

## Overview
An interactive Power BI dashboard that analyzes the sales performance of a retail company across six pages: executive KPIs, products, discounts and pricing, regions, customers, and shipping operations. The goal is to show where the company makes and loses money and which actions would improve profitability.



## Business Questions
1. How are total sales, profit, and profit margin performing, and how do they change month to month?
2. Which product categories, sub-categories, and containers drive profit, and which ones lose money?
3. How do discounts and unit price bands affect profit margin?
4. Which regions, states, and managers contribute the most to sales?
5. Who are the most valuable customers, and how many customers are unprofitable?
6. Which customer segments generate the most sales?
7. How fast do orders ship across ship modes and order priorities, and what do they cost?

## Data
- Source: "Superstore" sample retail dataset (fictional company)
- Period: January – June 2015
- Scale: 5,632 orders, 1,130 customers, and 5.77M in total sales
- Data model: star schema with a fact table (Final Sales Data) connected to the dimension tables Calendar, Customers Data, Products Data, Managers Data, and Returns Data
- Measures Table: Total Sales, Total Profit, Profit Margin, AOV, Total Orders, Total Customers, Active Customers, Loss-Making Customers (and %), High Discount Lines (and %), High Discount Profit, Mid-Priced Profit (and contribution %), and Profit Contribution % by Band

## Dashboard Pages

### 1. Executive Overview
KPI cards for Total Sales, AOV, Profit Margin, Total Orders, Total Customers, and Total Profit, plus a monthly sales trend.



### 2. Product Performance
Total profit by sub-category, and sales by product category and product container.



### 3. Discounts and Pricing
Very high discount orders and profit, sales, profit, and margin by unit price band, and profit margin by discount level.



### 4. Regional Performance
Sales by state or province, region, and manager.



### 5. Customer Analysis
Total customers, orders, AOV, loss-making customers, sales by customer segment, and the top 10 customers by sales.



### 6. Shipping and Operations
Average shipment duration by ship mode and order priority, sales by ship mode, and shipping cost by product category.



## Key Findings

### Overall performance
- The company generated 5.77M in sales and 543.27K in profit, a 9.42% profit margin, from 5,632 orders and 1,130 customers (AOV 1.02K).
- Sales are volatile from month to month: April peaked at 1.28M, about 78% above January (0.72M), while March (0.81M) and May (0.87M) both dropped sharply after strong months.

### Products
- Binders and Binder Accessories (162.09K) and Chairs and Chairmats (157.04K) are the profit engines. Together they deliver 319.13K, about 59% of total profit.
- Seven sub-categories lose money, led by Tables (-40.48K), Office Machines (-20.04K) and Computer Peripherals (-15.01K). Together these seven lose about 87K.
- Furniture leads sales (2.1M), followed by Technology (2.0M) and Office Supplies (1.6M).
- Small Box (2.1M) and Jumbo Drum (1.7M) containers generate about two-thirds of all sales.

### Discounts and pricing
- Profit margin falls steadily as discounts rise: 18.03% (low), 11.89% (medium), 7.32% (high), and -9.35% (very high).
- 987 orders (17.52%) carry very high discounts and together lose 83.07K.
- Cheap items lose money (-41.71K, -25.49% margin) despite 2,100 orders.
- Mid-to-high priced items drive all the profit: 609.72K at a 13.14% margin from 3,451 orders, which is more than the company's total profit because the other two bands lose money.
- Very expensive items (81 orders, 963.96K in sales) also run at a loss (-24.74K, -2.57% margin).

### Regions and managers
- East (1.78M) and West (1.73M) produce about 61% of sales, while Central (1.27M) and South (0.99M) lag behind.
- California (1.04M) and New York (672.3K) together make up about 30% of total sales, so sales are heavily concentrated.
- Manager shares mirror the regions: Erin 30.92%, William 29.99%, Chris 22%, and Sam 17.08%.

### Customers
- 530 of 1,130 customers (46.90%) are loss-making. Nearly half the customer base destroys value.
- Corporate (1.71M) and Home Office (1.68M) segments generate about 59% of sales, ahead of Consumer (1.21M) and Small Business (1.16M).
- The top 10 customers contribute about 1.12M (around 19% of sales). Kristine Connolly leads with 279.76K, followed by Nina Horne Kelly with 192.3K.

### Shipping and operations
- Average shipment duration is 1.92 days. Express Air (1.81) is barely faster than Regular Air (1.94) and Delivery Truck (1.91), yet it generates only 0.4M in sales against 2.8M and 2.6M for the other two.
- Low-priority orders take 3.97 days, almost three times longer than the other priorities (1.32 to 1.49 days). Critical orders (1.39) ship slightly slower than High-priority ones (1.32).
- Furniture accounts for about half of shipping cost (39K of 75K), ahead of Office Supplies (23K) and Technology (13K).

## Recommendations
1. Introduce a discount governance policy. Cap discounts and require approval above a set threshold. Very high discounts lose 83.07K, about 15% of total profit, so eliminating them would be the single biggest profit lever.
2. Set price floors and bundles for cheap items. A -25.49% margin means every sale loses money. Raise minimum prices, bundle them with high-margin products, or drop the worst performers.
3. Fix or exit the loss-making sub-categories. Tables, Office Machines, Computer Peripherals, and Bookcases lose about 81K together. Review supplier costs, repricing, and discount levels for each, and shift marketing toward Binders and Chairs, which generate about 59% of profit.
4. Build a customer profitability program. With 46.90% of customers unprofitable, score customers by profit rather than sales, tie discount eligibility to customer profitability, and assign account managers to the top 10 customers who generate about 19% of sales.
5. Reduce geographic concentration. California and New York make up about 30% of sales. Grow the South (0.99M) and Central (1.27M) regions by applying the East and West managers' practices, and set manager-level targets for the weaker regions.
6. Plan for seasonality. Study what drove the April peak (1.28M) and the March and May dips. Align inventory, staffing, and promotions with that pattern, and run promotions in weak months with capped discounts rather than deep ones.
7. Rethink the Express Air service. It saves only about 0.13 days versus Regular Air but accounts for just 0.4M in sales. Review its pricing and cost, or promote it as a premium option.
8. Investigate delivery times for low-priority orders and shipping cost for furniture. Set a service-level target for low-priority orders (now 3.97 days), and renegotiate freight rates or introduce minimum order values for furniture, which drives about half of shipping costs.

## Tools Used
- Power BI (data modeling, DAX measures, interactive dashboard design)
- Power Query (data cleaning and transformation)
- Excel (source data)
