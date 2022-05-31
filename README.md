# Sales_Performance_Analysis
We examined a superstore's fiscal year sales data, which spans from 1st April, 2018 to 31st March, 2019. 
The store is an Indian online sales store, with sales cutting across 19 states and 25 cities.

Product analysis, customer analysis and trend analysis was done, so as to answer the following questions and in turn derive actionable business insights.


- Which state has the highest sales?
- Which product has the highest sales?
- How is our products fairing in various cities?
- What is the overall sales pattern trend?
- What is our profit margin? Helps us know if the business is profitable and if our products prices are good.
- Are we meeting our target?                                                                                         


# Developer Tools
Power Query Editor in Power Bi was used for cleaning.
Power Bi visualization tools were used for visualization.

# Procedure
We imported our tables; City, Order List, Order Details and Sales Target, from excel workbook. We then went ahead to clean our messy dataset in the Power Bi Power Query Editor.
After our data has been cleaned, we went ahead to create relationship between our tables.
Measures were then created using DAX expressions.
The following are the measures created:
- ProfitMargin = DIVIDE([Profit],[TotalSales])
- SalesLastMonth = IF(NOT(ISBLANK([TotalSales])),CALCULATE([TotalSales], PARALLELPERIOD('Calendar'[Date],-1,MONTH)))
- SalesTargetdiff% = DIVIDE([TotalSales]-SUM('Sales target'[Target]),SUM('Sales target'[Target]))
- SalesVariance = [TotalSales]-[SalesLastMonth]
- SalesVariance% = DIVIDE([SalesVariance],[SalesLastMonth], BLANK())

We then went ahead to visualize our metrics.

# Images
![Screenshot (45)](https://user-images.githubusercontent.com/84106015/169573837-72f03a4b-1a37-4d67-a33f-f47d35b2b461.png)![Screenshot (44)](https://user-images.githubusercontent.com/84106015/169574210-3b30906d-4aef-4a0e-af31-fa443a13ed99.png)
![Screenshot (46)](https://user-images.githubusercontent.com/84106015/169574133-e4a21b48-ff01-452c-a37d-af3c28db6b38.png)

![Scree![Screenshot (44)](https://user-images.githubusercontent.com/84106015/171219212-b59d68ab-d85b-4f7a-94c1-a7abc3a9fa38.png)
nshot (43)](https://user-images.githubusercontent.com/84106015/169574289-86fadd49-3d54-409b-bcfb-0dd2495f5559.png)

# Observations

From our analysis, we were able to derive answers to our questions.

- The city of Indore tops the chart with total sale of $79,069.00 which constitutes 18.32% of the total sales in the fiscal year. Mumbai followed with total sales of $61,867.00.
The total sales recorded in the remaining cities is between $33,481.00(7.76%) in city of Pune and 4,507.00(1.04%) in Amritsar. 

- We have three product categories, electronics, furniture and clothing. And we have 17 product sub-categories.
Electronics category has the highest sales with total sales of $165,267.00, which is 38.3% of the total sales. This was followed by cloth, then furniture.
It's worth noting that we are running at loss on electronic games, in the electronic category and on table, in the furniture category. 

- From the customer’s charts we can deduce we are selling below profit margin to some customers. An example is customer with order id B-25653, with profit margin of -9.2%.
We can further see how we are running loss on some of our customer's table.

- We ran at loss from April 2018 to September 2018. Profit was recorded for the remaining months of the fiscal year recording the highest profit in November 2018 with 24.2% profit margin.

- The month over month% chart helped us look indepth to our sales trend. We can see the percentage increase and decrease that makes the trend.

- There was an overall uptrend in sales trend.

- The overall profit margin percentage recorded was 5.6%.

- We went ahead to look deeply into why we are running at loss selling to some customers. From the tables page, we compared the unit price per product to the price at which we sold to customers.
We observed that we don't follow an organized plan for giving discount to customers. 
The discount given to customers is way too high. 

- We were able to meet sales target in 5 months, and we were behind target in 7 months. We recorded 41% sales above target  in January, 2019 which is farthest we exceeded target in the fiscal year and   62% sales  below target in July, 2018 which is the lowest point behind target.

# Conclusion and Recommendations
Although, we saw an overall uptrend in sales, we were 1% behind our sales target and also had a 5.6% profit margin in the fiscal year. This performance is poor a poor one. From our findings we deduced that the cost of goods and the unit price of products are good but we have a faulty discounting system. 
Goods are sold to different customers at different prices, which most times is way below the set price. We therefore recommend that a well planned discounting system should be put in place.

Our brand is only known to 25 Cities across India, with low patronage in most of the cities. The company should engage in brand awareness, through social media promotions and social ads, to mention but few.

# Background Template
The background templated were created in PowerPoint.

# Author
- GitHub: ITOPE
- LinkedIn: Itunu Fatokunbo

# Contribution
Contributions, issues and requests are welcome!
