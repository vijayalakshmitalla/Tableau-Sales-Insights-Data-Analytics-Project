<h1 align="center">Sales Insights - Data Analysis using Tableau & SQL </h1>

### About Project 👨‍💻

- Performed India based hardware company sales insights - A Data Analysis project.

- Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design star schema data model on Tableau.

- Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.

## Technologies used ⚙️

* <a href="https://coursera.org/share/064db4645159df788ad0b31abebf1556">Advance Excel</a>

* <a href="https://www.mysql.com/">MySQL</a>
* <a href="https://www.tableau.com/">Tableau</a>
* <a href="https://powerbi.microsoft.com/en-us/">Power BI</a>
* <a href="https://www.britannica.com/science/statistics">Statistics</a>


### Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 Products by revenue.
  
- Q5. Net Profit & Profit Margin by Market

### Approach - Project Planning & [Aims Grid](https://www.youtube.com/watch?v=6118I9HViuQ)
  
#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.

#### 2. Stake Holders: Who will be involved?
- Sales Director, 
- I.T. Team, 
- Customer Service Team, 
- Data & Analytics Team.

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick & latest sales insights in order to support data driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with latest data available.
- Sales team able to take better decision & prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.

  
## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`

  
## Project References: 🔗

|**Sr.No. 🔢**|**References 👨‍💻**| **Links :link:**|
|------|--------------------|---------------------|
|1| **Tableau Project Dashboard :** Sales Insights - Data Analysis using Tableau | [Dashboard](https://public.tableau.com/views/SalesInsights-DataAnalysisProject/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)|
|2| **Tableau Public Profile** | [Tableau Public Dashboard](https://public.tableau.com/app/profile/mrankitgupta) |
|3| Tutorial | [YouTube 1](https://www.youtube.com/playlist?list=PLeo1K3hjS3utcb9nKtanhcn8jd2E0Hp9b) | 
|4| MySQL installation | [YouTube 2](https://www.youtube.com/watch?v=WuBcTJnIuzo) |
|5| OLTP & OLAP | [Geeks for Geeks](https://www.geeksforgeeks.org/difference-between-olap-and-oltp-in-dbms/) | 
|6| Star Schema: Fact Table & Dimension Table | [Microsoft docs.](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema) | 
