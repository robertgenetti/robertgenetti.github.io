---
title: "Covid-19 Vaccines"
image: "/images/projects/covid19vacc.png"
gif: "/images/projects/covid19vacc.gif"
link: "https://public.tableau.com/views/Book1_16627808205440/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link"
---

In the early days of the Covid-19 Pandemic, policy makers and health organizations had little to compare to what the world was going through. Now, most of the policy decisions that were made in the two plus years that followed have come to an end. And with it the chance to look back at the data collected and ask _what impact did policy have on the general health of different nations?_ 

### Problem

Policy decisions made during the pandemic were less effective and ill received as there was nothing to compare to. Now that we have established common methods of data collection - the task of analysis is easy. What remains difficult is the care and consideration that although the pandemic has receded the threat has not.

### Solution 

This project takes publicly available data from Our World In Data and presents a set of key measures that when taken together give a holistic view of the impact of policy decisions on public health and presents it in an up-to-date easy to interpret dashboard for anyone to use.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a pandemic policy response dashboard</p>
<p><b>Timeline:</b> Approximately 80 hours</p>
<p><b>Tools:</b> Python, Jupyter Lab, SQL, Azure Data Studio, Affinity Design</p>

Define -> Plan -> Data -> Analysis -> Visualize

<div class="mb-3"></div>

### Define

A well defined pandemic time political and health care response measuring system, against known benchmarks will provide the necessary information to make more informed decisions and greatly increase the likelihood of lives saved moving forward.
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

### Data
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
<div class="row justify-content-start">
<div class="col-6">

<p>The dashboard illustrates the differences in policy restrictions and their effect on public health. The data suggests that nations that acted more quickly to stem the infection rate with restrictive policy were more equiped to combate the virus and limit the tole on fatality rates. Also included in the data is the vaccination status of income groups. This suggests that lower income groups were less protected or less willing to get vaccinated than that of the middle and high income groups.</p>

<p>Future plans include expanding the map and list features to respond to changes in the time parameter.</p>

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

