---
title: "Public Pensions"
order: 4
image: "/images/projects/pp_hero.png"
gif: "/images/projects/ppd.gif"
link: "https://public.tableau.com/views/PublicPensionFinancialReport/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---


Looking at recent data on public pensions I was surprised at how common unfunded liabilities were and why managers of these funds were at a loss to correct the imbalance. I postulated that all stakeholders in these under funded public pensions share the assumption that investment performance will reduce liabilities and improve funding levels in time. I question the basis of this reasoning and propose a more objective approach to identify potential areas for financial improvement.

### Goal

In this project we explore the attributes of public pensions that identify as having high unfunded liabilities and compare it to those with low unfunded liabilities. We will examine financial data to define these differences and collect evidence of any correlations that may explain why unfunded liabilities are so prevalent.

### Outcome 

The data indicates a pattern of unbalanced cash flow that contributes to higher rates of unfunded liabilities. Even in times of extraordinary investment performance, such as seen in 2021, only those pensions with minimal total deductions relative to cash inflows had the greatest positive impact on net position.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Dashboard</a>
    <!-- <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Report</a> -->
</div>


### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a public pensions dashboard</p>
<p><b>Timeline:</b> Approximately 40 hours</p>
<p><b>Tools:</b> Apache Airflow, Python, SQL, Azure Data Studio, Affinity Design, Tableau</p>

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

### Plan (3 Steps)
1. Extract and Load
    - Pull public pension data from Public Pensions Database
    - Import dataframes into SQL Postgres Database
2. Analyze data in SQL
    - Feature selection
    - Omitt pension plans that have been closed
    - Export datasets into Excel files
3. Design Tableau dashboard
    - Display each section of financial report


### Extract, Transform, and Load
- Data source: [Public Pensions Database](https://publicplansdata.org/public-plans-database/)
- All fields were collected: Financials, Asset allocation, etc.

#### Apache Airflow
- Build three DAG functions to auto extract and load data into Postgresql database  
- Set Airflow to run every week to update database 
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: Apache Airflow (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#airflow" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/ppd_py.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>


### Analyze Data
- Feature selection - Azure Data Studio
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: Azure Data Studio Code (SQL)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#sql" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/PPD-Notebook.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>


### Evaluate Results
- Design dashboard elements - Affinity Design
- Build sheets and dashboards - Tabeau
- Details sections with net position, membership, investment performance
- Additional section with asset allocation information

<div class="mb-3"></div>

#### Tableau Dashboard Shapshot 📸
![screenshot](/images/projects/pp_hero.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>Every year that goes by the value of public pensions is drawn down. As members collect on pension benefits the fund value is diminished. That is why it is essential that the actuarial planning of cash outflows is in balance with expected inflows. But when planning and cashflow balancing is not performed in accordance with what is prudent, the pension is threatened and members are at a loss.</p>
            <p>Not only are the members at a loss but so is the state or local government. Using 2021 as the base year, the data shows that pensions less than half funded have the greatest share of employer contributions as a percentage of total deductions at an average of 88%. That is compared to pensions more than 90% funded with employer contributions as a percentage of total deduction of 70%. That's a difference in employer contributions to deductions of 18%, far more financially burdensome to the state or local government. What is more surprising are the impacts of investment gains on annual net positions. Pensions that are below 50% funded have an investment inflow to total deductions rate of 102%, compared to the more lofty figure of 444% for pensions that are above 90% funded. A difference in the impact of investment inflows of 342%. Highly funded pensions are more effective at translating investment gains into actuarial assets because of lower total deductions on average. Once a pension becomes unbalanced in how it manages cashflow, recovery to accrue positive actuarial assets relative to unfunded liabilities becomes more difficult.</p>
            <p>In this project we explored public pension fund data in an effort to gain a better understanding of how specific factors contribute to higher levels of unfunded liabilities. The results, high total deductions relative to cash inflows significantly contributed to diminishing impacts of investment gains and increase the burden on state and local government to make up the difference for low asset levels. Investment gains, even in extraordinaty times such as experienced in 2021, are not enough to correct for years of cashflow imbalances. Policy recommendation moving forward is to focus on improving monitoring and evaluation of cashflow balances, and making adjustment as needed.</p>
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

