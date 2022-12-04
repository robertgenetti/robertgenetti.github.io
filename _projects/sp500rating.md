---
title: "S&P 500 Rating"
image: "/images/projects/sp500rating.png"
gif: "/images/projects/sp500rating.gif"
link: "https://public.tableau.com/views/Book3_16649292527140/screener?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

 The S&P 500 is one of the most widely followed index in the U.S. And every stock in that index gets a buy or sell recomendation. Depending on how much a stock is followed determines how much attention is given in the form of analysis and recommendations. _What benefits can be gained by having a self-hosted stock analysis tool that can give buy or sell recommendations with every earnings release?_

### Problem

Buy or sell recommendations are issued with every quarterly earnings and by different investment institutions. However that schedule is not always the same with every stock. Stocks can get very little analysis and suffer by having few buy or sell recommendations issued.

### Solution 

A self-hosted stock analysis tool can, with the use of statistical modeling, issue buy or sell recommendations to all stocks at every new earning release.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a stock screener and analysis dashboard</p>
<p><b>Timeline:</b> Approximately 120 hours</p>
<p><b>Tools:</b> Python, R, Jupyter Lab, SQL, Azure Data Studio, Affinity Design, Tableau</p>

<div class="container text-center my-4">
    <div class="row justify-content-center">
        <div class="col p-2">
            <h3>Plan</h3>
            <img src="/images/projects/Plan.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
        <div class="col p-2">
            <h3>Extract</h3>
            <img src="/images/projects/Extract.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
        <div class="col p-2">
            <h3>Analyze</h3>
            <img src="/images/projects/Analyze.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
        <div class="col p-2">
            <h3>Visualize</h3>
            <img src="/images/projects/Visual.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
    </div>
</div>

<div class="mb-3"></div>

### Plan
1. Extract, Transform, and Load
    - Pull list of companies in S&P 500
    - Pull financial data from Yahoo Finance
    - Sort and transform data in Pandas
    - Import dataframes into SQL Postgres Database
2. Analyze buy/sell recommendation data in Python
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

### Extract

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
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>A dashboard is no substitute for meaningful stock analysis done by professionals. However, there is value in having a self-hosted analysis dashboard. This stock anlaysis tool is both flexibility easy to use. The regression model included allows for responsive recommendation updates and customizable key performance measures. </p>
            <p>Future plans include adding more stocks beyond those listed in the S&P 500, a recommendation scale with the source of other institutions, and building out the competition section to show more measures relative to the target stock.</p>
            <div class="text-center">
                <a href="{{page.link}}" class="button button-primary mt-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
            </div>
        </div>
        <div class="col-12 col-md-5">
            <div class="whitebox" ><a href="{{page.link}}" target="_blank">
            <img src="{{page.gif}}" alt="{{page.title}}" style="width:100%; height:auto; object-fit: cover;"></a>
            </div>
        </div>
    </div>
</div>
