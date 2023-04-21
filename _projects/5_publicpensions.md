---
title: "Public Pensions"
image: "/images/projects/pp_hero.png"
gif: "/images/projects/ppd.gif"
link: "https://public.tableau.com/views/PublicPensionFinancialReport/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---


U.S. Public Pension plans are among the most transparent financial institutions, but can become opaque when comparing one pension plan to another or across states and local governments. Public pension plans stand to gain from more information comparison between pensions to improve policy and investment planning. _What benefits can be gained by having an aggegate level comparison tool for all public pension plans?_

### Problem

Public pension plans in the U.S. are great at reporting performance changes and policy transparency, but when it comes to aggregate level analysis online tools and metrics are not readily available.

### Solution 

Creating a data visualization tool using common public pension financial information metrics to allow ad hoc research and evaluation across multipe state and municiple public pensions.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
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

### Plan
1. Extract and Load
    - Pull public pension data from Public Pensions Database
    - Import dataframes into SQL Postgres Database
2. Analyze data in SQL
    - Feature selection
    - Omitt pension plans that have been closed
    - Export datasets into Excel files
3. Design Tableau dashboard
    - Display each section of financial report

### Extract

- Data source: [Public Pensions Database](https://publicplansdata.org/public-plans-database/)
- All fields were collected: Financials, Asset allocation, etc.

![screenshot](/images/projects/ppd_online.png)
<div class="mb-3"></div>

#### Apache Airflow
- Build three DAG functions to auto extract and load data into Postgresql database  
- Set Airflow to run every week to update database 

![screenshot](/images/projects/ppd_airflow.png)
<div class="mb-3"></div>

<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/ppd_py.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Analyze

- Feature selection - Azure Data Studio
- Data source: Public Pensions Database

<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/PPD-Notebook.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Visualize

- Design dashboard elements - Affinity Design

![screenshot](/images/projects/ppd_affinity.png)
<div class="mb-3"></div>

#### Tableau
- Build sheets and dashboards - Tabeau
- Details sections with net position, membership, investment performance
- Additional section with asset allocation information

![screenshot](/images/projects/pp_hero.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>Tracking and monitoring public pension plans across state and local governments is now easier and more accessable than before. In this project we built a simple dashboard that can be used to quickly view many U.S. Public Pension all in one place. The information that is gained through this data visualization benefits data professionals and researchers alike.</p>
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

