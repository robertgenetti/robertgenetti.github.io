---
title: "SJ Vision Zero"
image: "/images/projects/visionzero_hero.png"
gif: "/images/projects/visionzero.gif"
link: "https://public.tableau.com/views/Book4_16695084459570/Home-Page?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---


The San Jose Vision Zero Initiative aims to eliminate fatal and severe traffic related injuries. The city initiative was implemented in 2015 and since then have expanded its safety priority corridors list to 19 high KSI rated streets. The initiative has made data collection and visualization a key component to its planning and implementation process. _What benefit might the Vision Zero Initiative gain from having a data visualization that features a corridor filtered view of the traffic related injury data?_

### Problem

Current data visualization solutions do not include a corridor map that filters and displays crash data by corridor. Not having a density map of high KSI corridors constrains data interpretation to only an aggregate level.

### Solution 

Creating a data visualization that illustrates corridor level traffic accident data may increase corridor specific metrics and improve trend forecasting.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">View Dashboard</a>
</div>

### Overview

<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a vision zero dashboard</p>
<p><b>Timeline:</b> Approximately 120 hours</p>
<p><b>Tools:</b> Apache Airflow, Python, Jupyter Lab, QGIS, SQL, Azure Data Studio, Affinity Design, Tableau</p>

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
    - Pull crash data from San Jose Open Data Portal
    - Import dataframes into SQL Postgres Database
2. Analyze data in SQL
    - Feature selection
    - Transform data, add moving average/ rolling total
    - Import into SQL Postgres Database 
3. Update shapefile with QGIS
    - Add more high KSI corridors using vector tool
    - Calculate length for added corridor rows
    - Create boolean field -- non-priority or priority corridor
4. Design Tableau dashboard
    - Overview with aggregate crash data
    - Filters to drill-down into data
    - Corridor heat map
    - Additional filters for corridor selection
    - information about Vision Zero Initiative (Refrences)

### Extract

- Data source: [Crash Locations](https://data.sanjoseca.gov/dataset/crash-locations1)
- Three different datasets were collected: Crash Locations, Crash Vehicles Involved, and Safety Corridors
- Crash Locations dataset features: date, age, lighting, weather, involved, narrative, violation 
- Crash Vehicles Involved dataset features: date, direction, damage, violation
- Safety Corridors dataset features: streetname, limits, grantamount, notes

![screenshot](/images/projects/vz_data_snap.png)
<div class="mb-3"></div>

#### Apache Airflow
- Build three DAG functions to auto extract and load data into Postgresql database  
- Set Airflow to run every week to update database 

![screenshot](/images/projects/airflow_snap.png)
<div class="mb-3"></div>

<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/airflow_vision_zero.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

### Analyze

- Feature selection - Azure Data Studio
- Data source: Vision Zero Crash data

<div class="mb-3"></div>
<div style="border: 1px solid #dcdcdc;">
  <iframe src="/images/projects/visionzerosj.html" frameborder="0" height="450" width="100%"></iframe>
</div>
<div class="mb-3"></div>

#### QGIS
- Data source: Vision Zero Corridor dataset
- Vector tool - Add corridors
- Calculate - Update length field

![screenshot](/images/projects/qgis_snap.png)
<div class="mb-3"></div>

### Visualize

- Design dashboard elements - Affinity Design

![screenshot](/images/projects/affinity_snap.png)
<div class="mb-3"></div>

#### Tableau
- Build sheets and dashboards - Tabeau
- Summary page with filters
- Details page with corridor filters
- Information page with vision zero initiative links

![screenshot](/images/projects/tableau_snap.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>In this analytical visualization the traffic accident data is represented in two areas. First a summary view of the overall trends and details of individual accidents to guide discussion and focus broad-based goals. And in the second area a more narrow view of the data that illustrates corridor specific information to focus on individual streets that have recurring high KSI rates.</p>
            <p>Apparent in the visualization are some insightful trends. The data in the summary view indicates a decrease in KSI of nearly 47% for vehicles and 29% for pedestrian related accidents from one year ago. However speeding, unsafe turn movements and running red lights still remain a leading indicator for traffic violations and resulting injury. The Data in corridor view indicates most all priority safety corridors are either maintaining of declining in KSI rates. Among other corridors not identified yet as priority on stood out. Over a three year period Santa Teresa Boulevard has shown a rise in injury rates from 1 KSI every two months to 1 every month.</p>
            <p>This project was an opportunity to create a useful tool for interpreting open source data in a way that informs further discuccion for the benefit of the Vision Zero Initiate. Any future plans to impove the dashboard would include axpanding the list of potential corridors and possibly adding a proximity to intersection filter.</p>
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

