---
title: "S&P 500 Rating"
image: "/images/projects/sp500rating.png"
gif: "/images/projects/sp500rating.gif"
link: "https://public.tableau.com/views/Book3_16649292527140/screener?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

 The S&P 500 is one of the most widely followed indices in the U.S. Within that index each stock is given buy or sell recommendations based on how much that stock is folowed by analysts. For this reason some stocks, though included in the S&P 500 may not get a frequent update on its recommendation rating. I wan to know _what benefits can be gained by having a regression driven stock analysis tool that provided buy or sell recommendations on demand and is updated with every earnings release no matter the popularity of the stock?_

### Problem

Buy or sell recommendations are issued by investment firms on an irregluar schedule. Depending on how popular the stock, a recommendation may be more or less fequent, leaving some investors with little guidence when deciding to update an invetment position.

### Solution 

A regression driven stock analysis tool can be more available to the average investor on a regular schedule when issuing buy or sell recommendations. The benefit is having some way to update a investment position no matter the level of activity coming from the investment firm analysis.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a stock screener and analysis dashboard</p>
<p><b>Timeline:</b> Approximately 120 hours</p>
<p><b>Tools:</b> Python, R, Jupyter Lab, SQL, Azure Data Studio, Affinity Design</p>

Define -> Plan -> Data -> Analysis -> Visualize
<div class="mb-3"></div>

### Define

A multi-paged dashboard that can suppliment investment analysis using both exploratory analysis and regression modeling will be of great benefit to individual investors. Such a dashboard will feature financial reporting with common metrics, filtering, historical graphs, and up-to-date recommendatons.
<div class="mb-3"></div>

### Plan
1. Extract, Transform, and Load
    - Pull list of companies in S&P 500
    - Pull financial data from Yahoo Finance
    - Sort and transform data in Pandas
    - import dataframes into SQL Postgres Database
2. Analyze buy/sell ecommendation data in Python
    - Select features best suited
    - Transform data to limit outliers
    - Import into SQL Postgres Database 
3. Build Linear Regression with Fixed Effects in R
    - Explore data
    - Perform linear regression on test data
    - Use fixed effects to seperate sector bias
4. Design Tableau dashboard
    - Screener to filter companies based on specific measures
    - Overview with buy/sell readout from linear model
    - Income statement KPIs
    - Balance sheet KPIs
    - Cashflow statement KPIs

### Data

- Data source: [Yahoo Finance](https://finance.yahoo.com/)
- Four different datasets were collected: general info, income statement, balance sheet, cashflow statement
- Info dataset common features: symbol, date, total revenue, debt/equity 
- Income Statement dataset common features: ticker, date, net income, cost of revenue 
- Balance Sheet dataset common features: ticker, date, total assets, total liabilities  
- Cashflow Statement dataset common features: ticker, date, cash from operations, cash from financing
![screenshot](/images/projects/yahoofinance.png)
<div class="mb-3"></div>

### Analysis

- Pandas ETL - Yahoo Finance
- Azure Data Studio
- Statistical Analysis - Feature selection
- Linear Regression with Fixed Effects
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/sp500ranking.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/sp500.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/sp500_lm_features.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/sp500_lm.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Visualize

- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Affinity Designer
![screenshot](/images/projects/sp500_dash_design.png)
#### Tableau
![screenshot](/images/projects/book3.png)
<div class="mb-3"></div>

### Conclusion
<div class="row justify-content-start">
<div class="col-6">

<p>This dashboard is a combination of key performance measures, financial statement analysis, and recommendation system. Beginning on the first page, we see the entire list of companies include in the S&P 500. After filtering and selecting a target stock, the analysis continues through to the following pages. This is where we see financial statement analysis and common to each part, key performance measures with historical graphs.</p>
<p>Future plans include adding more stocks beyond those listed in the S&P 500, a recommendation scale with the source of other institutions, and building out the competition section to show more measures relative to the target stock.</p>

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

</div>
<div class="col-6">
<div class="whitebox" ><a href="{{page.link}}" target="_blank">
<img src="{{page.gif}}" alt="{{page.title}}" style="width:100%; height:auto; object-fit: cover;">
</a>
</div>
</div>
</div>

