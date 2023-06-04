---
title: "Seattle Housing"
order: 1
image: "/images/projects/seattlehousing.png"
gif: "/images/projects/seattlehousing.gif"
link: "https://public.tableau.com/views/SeattlePre-foreclosureInvestmentTool/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

When residential property is in financial distress so too is the owner. In these trying times owners have little to guide them out from under this burden and often must wait to be foreclosed on. However this does not have to be the case, and in other instances can be an opportunity. When the going gets tough, the tough get going. Investors may step in before the foreclosure process and rescue the distressed property so that it may retain its value at the market rate.

### Goal

The challenge of investing in pre-foreclosure property is the increase in costs associated with identifying investment opportunities. In this project we aim to lower the research costs by improving investment prospects through a data-driven approach. 

### Outcome

A more streamline research experience for investors looking into the pre-foreclosure market has the benefit of lower barriers to entry and increased market clearing capacity.

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
            <h3>Visualize</h3>
            <img src="/images/projects/Visual.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
    </div>
</div>

<div class="mb-3"></div>

### Plan (3 Steps)
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

### Extract, Transform, and Load
- Data sources: [King County Records](https://recordsearch.kingcounty.gov/LandmarkWeb/search/index?theme=.blue&section=undefined&quickSearchSelection=undefined), [Parcel Viewer](https://gismaps.kingcounty.gov/parcelviewer2/), [National Mortgage Database](https://www.fhfa.gov/DataTools/Downloads/Pages/National-Mortgage-Database-Aggregate-Data.aspx)
- All fields were collected: property details, mortgage deliquency rates

#### Jupyter Notebook
- Build Python functions to extract and load data into Postgresql database  
- Transform and join data from two sources 
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: JupyterLab (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#python1" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/king_county_foreclosures.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

#### Jupyter Notebook
- Build Python functions to extract and load data into Postgresql database  
- Filter data to only include most relevant 
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: JupyterLab (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#python2" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/nmdb.html" frameborder="0" height="330" width="100%"></iframe>
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
    <iframe scrolling="no" src="/images/projects/seattle.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

### Evaluate Results
- Design dashboard elements - Affinity Design
- Build sheets and dashboards - Tabeau
- Main section with map for geographic context
- Details section with investment costs estimates
- Additional section with market context illustrating national deliquency rates

<div class="mb-3"></div>

#### Tableau Dashboard Shapshot 📸
![screenshot](/images/projects/book2.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>Not long ago the nation experienced a deep and painful recession and in this period of financial uncertainty many residential property under financial strain flooded the market. Market participants were slow to react and as a result prolonged the market clearing process. Pre-foreclosures being a prime example of this, represented an opportunity for unlocking great value.</p>
            <p>How this value can be unlocked is not with anyone solution. But with this research tool we have created, I aim to reduce the costs of investment uncertainty and market research if it is only an incremental improvement. The greatest value is to the owners of these properties for which may improve their opportunities to recover and progress in their future.</p>
            <p>This project examines potential areas for cost reduction and research efficiency by using a data-driven approach. Included in the research tool capability is a contextual map feature, delinquency rates graph, and investment costs estimation calculator. If interested in this market, and would like to become an investor yourself, pick up a copy of <i>Cashing In On Pre-foreclosures and Short Sales</i> by Chip Cummings.</p> 
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



