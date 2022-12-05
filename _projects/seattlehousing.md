---
title: "Seattle Housing"
image: "/images/projects/seattlehousing.png"
gif: "/images/projects/seattlehousing.gif"
link: "https://public.tableau.com/views/Book2_16641659196370/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

Pre-foreclosure properties are an underserved market that stands to benefit from increased open records search tools and data visualization. In U.S. states like Washington, public records are freely available online - further opening the door to timely analysis and quick visual real-time tools. The question is _how might this new open data feature in King county Washington benefit from lower barriers and increased access to market information?_

### Problem

The pre-foreclosure property market is an area of the real estate investment community that can benefit from having tools availble to view in real time active investment opportunities. Without tools to meet the growing demand for modernization of this market and open data standard it will remain an undeveloped , unrealized value in the real estate market. 

### Solution

This project focused on increasing the utilization of open data provided by King County Records online resource. By collecting and merging data relevant to our utilization purposes, we can build a dashboard using modern search methods that display real-time prospects to engage with investors and property owners alike.   

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a pre-foreclosure property dashboard</p>
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
            <h3>Visualization</h3>
            <img src="/images/projects/Visual.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
    </div>
</div>

<div class="mb-3"></div>

### Plan

1. Extract, Transform, and Load
    - Pull list of distressed properties from King County Records
    - Pull property details from related resources
    - Pull National Mortgage Database (NMDB) dataset
    - Sort and transform data in Pandas
    - import dataframes into SQL Postgres Database
2. Create subsets in Azure Data Studio
    - Using SQL queries to create data tables
3. Design Tableau dashboard
    - Map feature to filter by location
    - List for selection
    - Past due home loan data line chart
    - Display investment potential figures with params
    - Walkability Score

### Extract

- Data source: [King County Records](https://recordsearch.kingcounty.gov/LandmarkWeb/search/index?theme=.blue&section=undefined&quickSearchSelection=undefined)
- Rows of data: 214706
- Common features: location, date, cases, deaths, vaccinations, population
![screenshot](/images/projects/kingcountyrecords.png)

- Data source: [Parcel Viewer](https://gismaps.kingcounty.gov/parcelviewer2/)
- Rows of data: 214706
- Common features: location, date, cases, deaths, vaccinations, population
![screenshot](/images/projects/parcelviewer.png)

- Data source: [National Mortgage Database](https://www.fhfa.gov/DataTools/Downloads/Pages/National-Mortgage-Database-Aggregate-Data.aspx)
- Rows of data: 214706
- Common features: location, date, cases, deaths, vaccinations, population
![screenshot](/images/projects/nmdb.png)
<div class="mb-3"></div>

### Analysis

- Pandas ETL - Pre-foreclosure listings
- Pandas ETL - NMDB
- Azure Data Studio
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/king_county_foreclosures.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/nmdb.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/seattle.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Visualization

- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Affinity Designer
![screenshot](/images/projects/seattle_dash_design.png)
#### Tableau
![screenshot](/images/projects/book2.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>The improvement to market information accessability has a net benefit to the real estate investment community. Tools for gathering information and presenting it in a way that can be used directly already exist. However this dashboard is focused on the underserved pre-foreclosure market, which can benefit from the addition of lower barriers to market information. </p>
            <p>Future plans include expanding the map features so that when a user clicks on a property link it sends then to a detail page with more information. Another improvement would be to integrate the program into an app or website to be used as a service or online reference.</p> 
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



