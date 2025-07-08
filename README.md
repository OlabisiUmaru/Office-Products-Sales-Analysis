# Office Products Order Sales Analysis
This project presents a comprehensive analysis of sales performance from 2013 to 2017 across regions, customer types, product categories, and account managers for a fictitious Office Products Sales Company. Using Excel functions, the analysis uncovers key business insights and provides actionable recommendations to optimize sales, profitability, and operational efficiency. Dashboards have been included to visualize findings.

## **Table of Contents**

Executive Summary

Project Objectives

Document Purpose

Use Case

The Dataset

Data Cleaning and Processing

Analysis and Insights

 - Sales Performance by State

 - Sales by Customer Type

 - Sales Trends Over Time

 - Account Manager Performance

 - Product Category and Profitability

 - High Quantity Orders (40 and above)

Data Visualization

Recommendation

Conclusion

## **Executive Summary**
The dataset comprises 1,039 orders, providing details on order date, customer type, product category, account manager, and financial metrics (cost price, retail price, profit margin, and total sales). The analysis focuses on seven key areas: sales by state, customer type, sales trends over time, account manager performance, product category profitability, order priority, and high-quantity orders (>=40 units). Key findings include:
- NSW dominates sales, contributing most of the revenue and order volume.
- Corporate customers drive high-value orders, but Home Office customers show high order frequency.
- Technology products yield higher profit margins, though Office Supplies dominate order volume.
- Sales trend shows fluctuations throughout the year, with notable peaks and dips showcasing seasonal demand driven by holidays and business cycles.
- Top-performing account managers like Yvette Biti and Connor Betts drive significant sales in VIC.

Actionable recommendations include targeted marketing, product focus on high-margin Technology items, and training for underperforming account managers. Dashboards are proposed to visualize these insights, and a GitHub project structure is outlined for transparency and collaboration.

## **Project Objectives**
The analysis focuses on seven key areas and aims to provide actionable insights, including:

**Sales Performance by State**
  
- Understand the distribution of sales across different states (VIC, NSW, WA) to identify high-performing regions and opportunities for growth.

**Sales by Customer Type**
  
- Identify which customer types (Home Office, Consumer, Small Business, Corporate) drive the most revenue and order volume to optimize customer segmentation strategies

**Sales Trends Over Time (Daily, Monthly, Quarterly and Yearly)**

- Analyze sales trends over years (2013–2017) and months to identify seasonality or growth patterns.

**Account Manager Performance**

- Evaluate the performance of account managers to identify top performers and those needing support.

**Product Category and Profitability Analysis**

- Identify which product categories (Office Supplies, Technology, Furniture) and specific products yield the highest profit margins and sales.

**High Quantity Orders (40 and above)**

- Analyze orders with quantities over 50 to understand high-volume purchasing behaviour.


## **Document Purpose**

This documentation serves as a guide for project stakeholders, providing insights into the project's objectives, data sources, data analysis, visualizations, and other relevant information.

## **Use Case**

- **Primary Stakeholders**: Senior Management, Sales Managers, and Marketing Team. Based on the analysis, these stakeholders would gain a high-level understanding of sales trends, profitability, and regional performance to inform strategic decisions, design targeted campaigns, budget allocations, and growth targets, as they directly influence strategic and operational decisions.

- **Secondary Stakeholders**: Account Managers, Supply Chain Managers, and Finance Team, who implement tactical changes and ensure resource alignment, would benefit from the analysis in optimizing stock levels, budgeting, cost management and evaluating the financial impact of discontinuing low-margin products.

- **Tertiary Stakeholders**: Customer Service Team, IT/Data Analysts, and External Stakeholders, who support execution, scalability, and external validation, would benefit from this analysis by understanding customer segment behaviour to improve support and address seasonal spikes. 


## The Dataset

The provided dataset is a synthetic dataset which represents sales information for a company, containing 2,092 entries with 17 columns. The data encompasses various aspects of sales transactions, including order details, customer information, product details, pricing, and account manager information. The dataset is diverse, containing both categorical and numerical data. It includes temporal information like "Order Date" in datetime format. Below is a detailed breakdown of each column:

- **Order No**: Unique identifier for each order.
- **Order Date**: Date when the order was placed.
- **Customer Name**: Name of the customer placing the order.
- **Address**: Customer's address (one entry appears to be missing).
- **City**: City where the customer is located.
- **State**: State where the customer is located.
- **Customer Type**: Type of customer (e.g., retail, wholesale).
- **Account Manager**: Name of the account manager handling the order.
- **Order Priority**: Priority level of the order.
- **Product Name**: Name of the product being sold.
- **Product Category**: Category to which the product belongs.
- **Product Container**: Container type for the product.
- **Cost Price**: Cost price of the product.
- **Retail Price**: Retail price at which the product is sold.
- **Profit Margin**: Margin between retail and cost prices.
- **Order Quantity**: Quantity of products ordered.
- **Total**: Overall total cost

The dataset lacks data for June, August, September, November, and December of 2017. This gap may affect the analysis of sales and trends. Caution will be noted in the relevant sections of the analysis.


## **Data Cleaning and Processing**

Having a clean dataset is the backbone of a sound numerical analysis. A clean dataset ensures accurate, reliable analysis by eliminating errors, duplicates, and inconsistencies, leading to better decision-making. Some columns like "Cost Price," "Retail Price," and others related to monetary values were initially stored as currently stored as objects, which were converted for accurate numerical analysis. analytical and exploratory tasks. Duplicate records for the same sales were removed from the dataset, with wrong calculations on the “Total” column corrected based on sales price and quantities sold for each order ID. All the necessary fields are present and filled out correctly. The data values are accurate, and each column has been updated to the correct data type.

However, to ensure a robust analysis, especially as it relates to analyzing sales trends over days, months and years, some new columns were added. These new columns included:

- **Month**: This column represents the month in which each order was placed, allowing for the analysis of monthly sales trends.
- **Day**: This column indicates the day of the week for each order, helping to identify the busiest days.
- **Quarter**: This column denotes the fiscal quarter in which each order occurred, providing insights into quarterly performance.

These additional columns are crucial for examining sales trends over time, identifying seasonal patterns, and determining peak sales periods.

## **Data Analysis and Insight**


**Analysis 1: Sales Performance by State**

**Objective**: Understand the distribution of sales across different states (VIC, NSW, WA) to identify high-performing regions and opportunities for growth.
To achieve this, a pivot table was created using the underlisted methodologies:

**Aggregated Total sales and Order No count by State (NSW, VIC, WA), yielding**:
- NSW: $1,538,527 (67.21% of total sales), 1,410 orders (67.21% of total)
- VIC: $607,542 (27.74%), 578 orders (27.74%)
- WA: $91,023 184,567 (8%), 104 orders (5.05%)

**Calculated average order value**:
- NSW: $1,091.15
- VIC: $1,051.11
- WA: $875.22

**TDESV.P: Measured sales variability**:
- NSW: $3,132.22
- VIC: $3,250.14
- WA: $2,710.27
This indicates higher fluctuations due to large orders (e.g., Order 5867-1, $29,999.50 (NSW) and Order 5681-1, $24,5999.59 (WA)).

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Total%20Orders%20in%20Revenue%20by%20State.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/%25%20Contribution%20by%20State.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Sales%20Trend%20by%20State.jpg)

**Insights**:

- NSW Dominance: Accounts for 67% of sales with a 3.7% higher average order value than VIC, driven by corporate customers and high-value office supplies purchases.
- VIC Stability: VIC contributes 27.74% of sales ($607,542), also with a strong performance in office supplies products.
- WA Underperformance: WA lags with 5.05% of sales ($91,023), indicating low sales and order volume. This suggests market saturation or weak account manager focus but also an opportunity for market expansion.
- High-Value Outliers: 44 orders >= $10,000 (44 out of 55 orders are concentrated in NSW) skew the regional average, indicating potential for targeted upselling. Also, a one-off sale to one customer in WA for $24,599.59 skews its regional average.
- Sales Trend across the States:
   - Uniform 2017 Decline Across States: All states experienced a drastic sales drop in 2017 (NSW: $19,992.51, VIC: $19,992.51, WA: $481.43), a significant departure from prior years.
   - This synchronized decline could indicate a company-wide issue, such as a product recall, loss of a major client, economic downturn, or the result of the data anomaly (incomplete 2017 data)
   - The 2017 drop represents a 94.8% (NSW), 85.1% (VIC), and 98.5% (WA) reduction from 2016, based on their CAGR from 2013 -2016, confirming statistical significance and a strong correlation between sales and order count.


**Analysis 2: Sales by Customer Type**

**Objective**: Identify customer segment contributions to tailor marketing and sales strategies.

**Methodology**:

To achieve this, a pivot table was created using the underlisted methodologies:

**Pivot Table**: Grouped by customer type with total as sum and order no as count.
- Corporate: $809,061.62 (36.17%), 756 orders (36.14%)
- Small Business: $568,144.29 (25.40%), 467 orders (22.32%)
- Home Office: $472,008.61 (21.10%), 522 orders (24.95%)
- Consumer: $387,877.19 (17.34%), 347 orders (16.59%)

**COUNTIFS**: Calculated count of high-value order totals (> $10,000), substituted for the different customer types:

 - =COUNTIFS(Total,">10000", Customer_Name, "Home Office") to count high-value orders 
 - (Corporate: 20, Small Business: 16, Home Office: 9, Consumer: 9)
  
**COUNTIFS**: Calculated count of high-value order totals (> 50), substituted for the different customer types
- =COUNTIFS (Order_Quantity, ">=50", Customer_Name, "Home Office")
- (Corporate: 20, Small Business: 5, Home Office: 19, Consumer: 10)
  
**SUMIFS**: Calculated the sum of high-value order totals (> $10,000), substituted for the different customer types:
- =SUMIFS (Total, Customer_Name, "Home Office", Total,">10000")
- (Corporate: $331,501.84, Small Business: $305,935.04, Home Office: $158,011.84, Consumer: $163,304.61)
  
**CORREL**: Assessed the relationship between order quantity and sales:
- Corporate: 0.40, Small Business: 0.19, Home Office: 0.18 and Consumer: 0.18
- Indicating no strong positive correlation between both variables. However, there is a stronger relationship between sales in the corporate category and quantities sold.

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/%25%20Contribution%20by%20Customer%20Type.png)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Total%20Sales%20by%20Customer%20Type.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/%25%20Contribution%20of%20High%20VAlue%20Orders%20per%20Customer%20Type.jpg)

**Insights**:

- Corporate customers contribute 36.17% of sales with 36.14% of orders.
- Average Order Values:
    - Corporate sales have the third-lowest average order values, amounting to $1,070/order. 
    - Home office at $904.23/order. 
    - Consumer is $1,117.80/order
    - Small Business has the highest average value at $1,216.58/order, indicating repeat higher transactions.
- Corporate High-Value Focus: 54% of sales from orders > $10,000, driven by Technology and bulk purchases.
- Corporate Frequency: Highest order count (36.14%) but lowest average value ($1,070), suggesting frequent but smaller transactions.
- Small Business Potential: Balanced volume and value, with 54% of high-quantity orders (>$10,000), indicating bulk buying opportunities.
- Consumer Lag: Minimal impact, with 17.34% of sales and 16.59% of orders. Despite limited retail focus or competition, it has potential for upselling high-value orders, contributing 42%, the second highest.


**Analysis 3: Sales Trends Over Time**

Objective: Analyze yearly and monthly sales to identify seasonality and growth patterns.

**Methodology**:
- TEXT: Extracted year (= TEXT (B:B, "YYYY")), month (=TEXT (B:B, "MMMM")), quarter (="Q" & ROUNDUP(MONTH(A1)/3,0) and Day (TEXT (B:B, "DDDD"), from Order Date.
- Pivot Table: 
   - Grouped by year, quarter, month and day with Total as sum.
   - Aggregated Total by year (2013–2017), month (Jan–Dec), quarter (Q1 – Q4) and Day (Sunday – Saturday)
- Yearly: $432,987 (2013) to $598,321 (2017), CAGR = 8.4% (= (598321/432987) ^ (1/4)-1).
- Seasonality Index: Calculated as monthly sales/annual average ($186,424.31), showing Jan (1.70), Apr (1.12), Aug (1.47) and Oct (1.14) as extremes.

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Sales%20Trend%20by%20Years%20(2013%20-%202017).jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Sales%20Trend%20by%20Quarter%20Per%20Year.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Monthly%20Sales%20Trend%20.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Total%20Sales%20by%20Days%20of%20the%20Week.jpg)


**Insights**:

- Yearly Growth: Sales grew from $424,079.83 in 2013 to $542,028.65 in 2016, with a significant dip in 2017 ($37,208.80).
- 8.4% CAGR reflects steady growth until a 2017 dip possibly due to market saturation.
- Seasonal Peaks: February ($316,104) and August ($273,600) suggest holiday/post-holiday and mid-year restocking, while June-August dips indicate summer slowdowns.
- December Dip: $135,214 drop likely holiday driven reducing demand across board and years.
- Sales remain steady throughout the week with a notable peak on Fridays ($365,433), likely due to stock reconciliations, and high sales on Sundays ($359,290). Saturdays see a significant dip, indicating reduced activity over the weekend.


**Analysis 4: Account Manager Performance**

**Objective**: Evaluate the performance of account managers to identify top performers and those needing support.

**Methodology**

- Pivot Table: Summarized sales and orders by Account Manager:
  - Connor Betts: $339,227.25, 342 orders.
  - Tina Carlton: $304,650.61, 297 orders.
  - Yvette Biti: $268,314.40, 236 orders.
- RANK: Ranked by sales: Connor (1), Tina (2), Yvette (3).
- AVERAGEIF: Profit margin averages = $12.87. The underlisted account managers outperformed this average by:
  - Leighton : 147% 
  - Radhya: 125%.
  - Charlie Bui: 120%.

Despite indicating high profit margins, the sales from these account managers exhibited low order volumes.

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Total%20Sales%20Analysis%20by%20Account%20Manager.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Top%205%20Avg.%20Profit%20Margin%20by%20Account%20Managers.jpg)

**Insights**:

**Top Performers**: Connor Betts ($339,227.25 sales, 342 orders) and Yvette Biti ($268,314.40 sales, 236 orders) lead, with strong performance in VIC. While Tina Carlton leads in NSW/WA with a total of $304,650.61, 297 orders.

**Underperformers**: Stevie Bacata ($8,019.22 sales, 15 orders) and Preston Senome ($33,067.30 sales, 67 orders) lag, primarily in NSW.

**Profit Margins**: Leighton Forrest, Radhya Staples and Charlie Bui achieve higher margins (28–32%) due to focus on Office Supplies (primary) and Technology products (secondary).


**Analysis 5: Product Category and Profitability**

**Objective**: Identify high-performing product categories and products to optimize inventory and marketing.

**Methodology**:

- Pivot Table: 
  - Grouped by Product Category and Profit Margin as values:
    - Technology: $18,634.01 (45.07% margin)
    - Office Supplies: $21,523.30 (52.06% margin)
    - Furniture: $1,188.75 (2.88% margin)
  - Grouped by Product Category with Total and Order Quantity for category sales:
    - Technology: $1,038,912 (46.44%), 9,676 orders
    - Office Supplies: $1,154,999 (51.63%), 43,934 orders
    - Furniture: $43,181 (1.93%), 1,067 orders
  - Grouped by Product Name with Total and Order Quantity for top 5 category sales by revenue:
    - Cando PC940 Copier: $408,590.92 (33.20%), 35 orders
    - HFX LaserJet 3310 Copier: $368,393.86 (29.94%), 20 orders
    - UGen Ultra Professional Cordless Optical Suite: $192,921.77 (15.68%), 25 orders
    - Adesso Programmable 142-Key Keyboard: $133,877.44 (10.88%), 33 orders
    - Deluxe Rollaway Locking File with Drawer: $126,843.40 (10.31%), 14 orders
  - Grouped by Product Name with Order Quantity for top 5 category sales by volume:
    - Alto Memo Cubes: 1,081 orders (20.47%)
    - Apex Straight Scissors: 980 orders (18.55%)
    - Artisan 474 Labels: 1,068 orders (20.22%)
    - Artisan 481 Labels: 1,185 orders (22.43%)
    - Artisan Hanging File Binders: 968 orders (18.33%)
  - Listed top 5 products by sales and margins

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Total%20Sales%20by%20Product%20Category%20(Revenue%20%26%20Qty).jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Top%205%20Products%20by%20Revenue%20and%20Qty.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Bottom%205%20Products.jpg)

**Insights**:
- Office Supplies Leader: 51.63% of sales driven by bulk orders (e.g., envelopes, clips).
- Technology Volume: 33.20% margin and $1,038,912 from high-value items (e.g., Cando PC940 Copier, $408,590.92) offer growth potential.
- Furniture Weakness: Minimal contribution (1.93%), with inconsistent demand.
- Low Performers: Products like Ecolon Metal Binder Clips ($2.62) have minimal profitability.


**Analysis 6: High Quantity Orders (40 and above)**

**Objective**: Analyze orders with quantities over or equals 40 to understand high-volume purchasing behavior.

**Methodology**

- **COUNTIF**: =COUNTIF(Order_Quantity,">=40") to count high-quantity orders. Identified 493 orders where Order Quantity >=40.
- **COUNTIF**: =COUNTIFS(Total,">10000", Customer_Name, "Home Office") to count high value orders over $10,000 per order. Identified 54 orders where Total sales per order >10000. Substituted across the different product categories.
- **SUMIF**: =SUMIFS (Total, Customer_Name,"Home Office", Total,">10000") to identity revenue realised for orders over $10,000. for total sales ($958,753.33). Substituted across the different product categories.
- **SUMIF**: =SUMIFS (Total, Customer_Name,"Home Office", Order_Quantity,">=40") to identity revenue realised for order quantities 40 and above ($1,007,726.66). Substituted across the different product categories.
- **Pivot Table**: Analyzed high-quantity orders by Customer Type and Product Category.

  ![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/High%20Qty%20Orders%20Table%20(Revenue%20%26%20Qty).jpg)

  ![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/High%20Value%20Orders%20(Revenue%20%26%20Qty).jpg)

  ![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/High%20VAlue%20Orders%20by%20Product%20Category.jpg)

  ![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Monthly%20Sales%20Trend%20for%20High%20Value%20Orders.jpg)

  ![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/High%20Value%20Orders%20by%20States.jpg)

**Insights**:

- Corporate Leadership: Corporate category makes the most contribution to high value orders both in quantities ordered and revenue (33% and 37% respectively).
- Home Office Category: While Home Office products are ranked second by quantity ordered (over 40), they generate the lowest revenue among categories, indicating a lower cost per transaction.
- Technology products such as keyboards and copiers account for 61.11% of high-quantity order value, with an average order value of $18,082.33.
- Office Supplies accounts for 80% of high-quantity orders, often for Office Supplies.
- Seasonal Spike: 60% of orders in February and August, aligning with peaks.
- NSW has the most high-quantity orders (323 out of 493), reinforcing regional strength.

## **Data Visualization**

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Dashboard%201.jpg)

![](https://github.com/OlabisiUmaru/Office-Products-Sales-Analysis/blob/main/Dashboard%202.jpg)


## **Recommendations**

- **Increase marketing in WA**: Due to lower sales in this region, implementing targeted campaigns or forming partnerships with marketing agencies may help improve performance.
- **Reinforce NSW strategy**: NSW accounted for 67% of sales with a 3.7% higher average order value than other regions, therefore more account managers could be allocated to capitalize on the high order values.
- **Analyse VIC office supplies sales**: Investigate why office supplies products perform well in VIC and replicate strategies elsewhere.
- **Corporate Customers**: Over 50% of sales came from corporate customers placing $10,000+ orders, primarily for Technology products. Maintain premium technology offerings and bulk discounts and implement loyalty programs to increase sales and order value.
- **Loyalty programs for Small Business**: Small businesses accounted for 54% of high-volume orders (over $10,000), suggesting instances of bulk purchasing. Implementing reward or loyalty programs may support maintaining consistent order frequency.
- **Target Consumer Business**: Despite limited retail focus or competition with17.34% of sales and 16.59% of orders, it has potential for upselling high-value orders. Develop tailored contracts or bundles to encourage larger orders.
- **Seasonal Promotions**: Provide discounts during March and September to address slower sales periods.
- **Inventory Planning**: Maintain inventory of high-margin Technology products to meet anticipated demand in February, August, and before Friday peak order times.
- **Training Programs**: Share Connor Betts, Tina Carlton and Yvette Biti’s strategies with underperformers like Stevie Bacata and Preston Senome.
- **Incentives**: Reward top performers with bonuses to maintain motivation.
- **Reassign Accounts**: Allocate WA accounts to managers with a record of higher regional performance, or pair account managers with these individuals for mentorship and sales development.
- **Promote Technology Products**: Increase marketing for high-margin items like copiers and keyboards.
- **Bundle Offers**: Pair Office Supplies with Technology products to boost overall margins especially for products in the furniture category.
- **Discontinue Low-Margin Products**: Evaluate items like Ecolon Metal Binder Clips and Alliance Rubber Bands for discontinuation or repricing.
- **Bulk Discounts**: Offer discounts for orders over 40 units to encourage larger purchases especially in regions like NSW which has the most high-quantity orders (323 out of 493).
- **Target Small Businesses**: Develop contracts for bulk Office Supplies purchases.
- **Supply Chain Efficiency**: Ensure inventory and logistics can handle high-quantity orders especially during spike periods like February and August. 

## **Conclusion**
The analysis highlights strong sales and profit potential in NSW, corporate customers, and technology products. Optimizing for seasonal trends and account manager performance can further boost results.

I am seeking a Data Analyst position in an organization where I can showcase my skills, take on additional responsibilities, and continue to learn and grow alongside the company, ensuring my contributions are highly valuable to the organization.

You can reach me on olabisiumaru@gmail.com

Thank you!

  
