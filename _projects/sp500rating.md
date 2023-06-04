---
title: "S&P 500 Rating"
order: 2
image: "/images/projects/sp500rating.png"
gif: "/images/projects/sp500rating.gif"
link: "https://public.tableau.com/views/SP500StockScreener/screener?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

 Learning to invest is difficult to say the least, but with the right analytical tools and with enough practice it can be done. Having fun while learning is always the goal when picking up new skills. And learning financial analysis is not different. Necessity is the mother of invention and this project is a necessary step on the road to a better understanding of the basics.

### Goal
This project aims to improve financial statement learning for beginner investors and provide a basic understanding of common financial ratio analysis.

### Outcome 
Solid financial analysis skills are the foundation to building more advanced skills and becoming a successful investor.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Dashboard</a>
    <!-- <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Report</a> -->
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

### Plan (4 Steps)
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
    - Buy/sell recommendation estimate -- OLS model
    - Income statement KPIs
    - Balance sheet KPIs
    - Cashflow statement KPIs

### Extract, Transform, and Load
- Data source: [Yahoo Finance](https://finance.yahoo.com/)
- Four different datasets were collected: general info, income statement, balance sheet, cashflow statement
- Info dataset common features: symbol, date, total revenue, debt/equity 
- Income Statement dataset common features: ticker, date, net income, cost of revenue 
- Balance Sheet dataset common features: ticker, date, total assets, total liabilities  
- Cashflow Statement dataset common features: ticker, date, cash from operations, cash from financing

#### Jupyter Notebook
- Build ETL functions to extract and load data into Postgresql database  
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: JupyterLab (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#python1" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/sp500ranking.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

### Analyze Data
- Feature selection - Azure Data Studio
- Statistical Analysis - OLS Model to estimate buy/sell recommendations

<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: Azure Data Studio Code (SQL)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#sql" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/sp500.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: JupyterLab (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#python2" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/sp500_lm_features.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: R-Studio (R)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#r" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/sp500_lm.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

### Evaluate Results
- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Tableau Dashboard Shapshot 📸
![screenshot](/images/projects/book3.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>When I began investing for the first time I had trouble identifying trends and value in the equities market. The novice investors are at risk of making investment decisions based on incomplete information. That is why having a dedicated stock screener and buy/sell recommendations model is important to improving financial analysis skills.</p>
            <p>Jan 2023, when this project’s data was last updated, the financial market was in a decidedly downward correction, shifting from the elevated levels of the year and a half before to a slightly lower valuations. Following this trend was lower projected earnings and less favorable buy/sell recommendations. Our own OLS model estimated a majority of stocks as a hold recommendation indicating a pull back in investments is underway.</p>
            <p>This project began as simple idea, to build a data visualization that would improve financial statement analysis and recommend buy/sell targets provided with the most recent data. For me the project gave me a better understanding of how different segments of the market are valued and what financial ratios to look for when analyzing specific stocks. If you are interested in financial markets and would like to learn more visit <a href="https://www.betterinvesting.org/" style="text-decoration:none;" target="_blank">betterinvesting.org</a> for tips on how to become an investor yourself.</p>
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
