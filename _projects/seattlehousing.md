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
<p><b>Tools:</b> Python, Jupyter Lab, SQL, Azure Data Studio, Affinity Design</p>

Define -> Plan -> Data -> Analysis -> Visualize
<div class="mb-3"></div>

### Define

When market clearing mechanisms are allowed to function efficiently those markets perform optimally. By providing investors a clear view into the pre-foreclosure market, search costs can be greatly minimized and time more appropriately spent on researching and engaging with distressed property owners.
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

### Data

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

### Visualize

- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Affinity Designer
![screenshot](/images/projects/seattle_dash_design.png)
#### Tableau
![screenshot](/images/projects/book2.png)
<div class="mb-3"></div>

### Conclusion
<div class="row justify-content-start">
<div class="col-6">
<p>This dashboard is a proof of concept that when applied effectively, online data records can be a great benefit to the modernization of out-dated tools to aid in more efficient market clearing. King County being the example has given the opportunity to develop tools that investors can utilizes in their search for pre-foreclosure property. The dashboard features a map, list and graph that give investors context and insight into this segment of the market. Also featured is a useful invetment forcasting tool that aids in the research phase of investing.</p>
<p>Future plans include expanding the map features so that when a user clicks on a property link it sends then to a detail page with more information. Another improvement would be to integrate the program into an app or website to be used as a service or online reference.</p> 

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



