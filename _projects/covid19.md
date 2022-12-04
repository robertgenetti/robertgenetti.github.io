---
title: "Covid-19 Vaccines"
image: "/images/projects/covid19vacc.png"
gif: "/images/projects/covid19vacc.gif"
link: "https://public.tableau.com/views/Book1_16627808205440/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link"
---

In the early days of the Covid-19 Pandemic, international policy makers and world health officials were put in the precarious position of crafting policy recommendations and enacting public restrictions, all without the benefit of having historical data to guide those decisions. Today however, the situation has changed, we know more than before and have the benefit of many nations working together to collect and analyzed the data available My question in this analysis is _how did restrictive policy measures impact the national health and wellbeing of those countries with high restrictions and those with low restrictions?_ 

### Problem

Policy decisions made during the Covid-19 pandemic were rendered less effective and ill received by the general public in part because no known metrics or data was available to support and garner confidence. Policy outcomes are best measured when more data is available to determine the net effects.

### Solution 

This project takes on two roles: to provide insight into the policy outcomes of national restrictions using the publicly available data from Our World In Data, and inform both the public and policy makers so that any further policy decisions can benefit from the data and experience gained thus far.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a pandemic policy response dashboard</p>
<p><b>Timeline:</b> Approximately 80 hours</p>
<p><b>Tools:</b> Python, Jupyter Lab, SQL, Azure Data Studio, Affinity Design, Tableau</p>

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
    - Pull dataset from Our World in Data
    - Sort and transform data in Pandas
    - import dataframes into PostgreSQL Database
2. Query SQL Database for subsets
    - Get aggregate dataset
    - Get vaccination status by nation
    - Get List of highest death count countries
    - Get vaccination status by income
3. Design Tableau dashboard
    - Top worst countries with highest death count
    - Time parameter
    - World metrics
    - Map with vaccination status
    - Bar graph of vaccination status by income

### Extract
- Data source: [Our World In Data - Coronavirus Pandemic](https://ourworldindata.org/coronavirus)
- Rows of data: 214706
- Common features: location, date, cases, deaths, vaccinations, population
![screenshot](/images/projects/ourworldindata.png)
<div class="mb-3"></div>

### Analysis

- Pandas ETL - Our World In Data
- Azure Data Studio
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/owid-covid.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/covid.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Visualize

- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Affinity Designer
![screenshot](/images/projects/covid_dash_design.png)
#### Tableau
![screenshot](/images/projects/book1.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>The dashboard illustrates the differences in policy restrictions and their effect on public health. The data suggests that nations that acted more quickly to stem the infection rate with restrictive policy were more equiped to combate the virus and limit the tole on fatality rates. Also included in the data is the vaccination status of income groups. This suggests that lower income groups were less protected or less willing to get vaccinated than that of the middle and high income groups.</p>
            <p>Future plans include expanding the map and list features to respond to changes in the time parameter.
            </p>
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



