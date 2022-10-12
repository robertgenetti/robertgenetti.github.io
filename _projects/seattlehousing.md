---
title: "Seattle Housing"
image: "/images/projects/seattlehousing.png"
gif: "/images/projects/seattlehousing.gif"
link: "https://public.tableau.com/views/Book2_16641659196370/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

Real Estate professionals and individual investors spend a great deal of time searching for potential investments in their respective market. None more so than the underserved pre-foreclosure market. The question I'd like to ask is _how might this market benefit from lower barriers to market information?_

### Problem

In the pre-foreclosure property market is an area of the real estate market that is underserved. The need lies in the ablility of investors to quickly find and engage with property owners to seek out favorable terms - potentially arriving at a deal. 

### Solution

My initial thoughts when starting this project focused on increasing the usefullness of the data already provided by the King County Records office. The solution would be to collect the data by merging it complimentary data and build into a useful visualization and or search tool.   

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

When market clearing mechanisms are allowed to function efficiently those market participants are better off for it. By providing investors the advantage of clear insight into the market their function in the market can lead to less time property owners spend in pre-foreclosure process.
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
<div class="whitebox-inset">
  <iframe src="/images/projects/king_county_foreclosures.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div class="whitebox-inset">
  <iframe src="/images/projects/nmdb.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>
<div class="whitebox-inset">
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
<p>The improvement to market information accessability has a net benefit to the real estate investment community. Tools for gathering information and presenting it in a way that can be used directly already exist. However this dashboard is focused on the underserved pre-foreclosure market, which can benefit from the addition of lower barriers to market information. </p>
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



