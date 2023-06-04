---
title: "SJ Vision Zero"
order: 3
image: "/images/projects/visionzero_hero.png"
gif: "/images/projects/visionzero.gif"
link: "https://public.tableau.com/views/VisionZero_16858311589970/Home-Page?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---


San Jose joined the effort of cities across the United States to eliminate severe and fatal traffic related accidents. The Vision Zero Initiative is a bold new way of solving a long standing issue. Reduce traffic related injuries by upgrading street design to better safeguard transportation activity.

### Goal
The data collected from traffic accidents will serve as a guide to monitor and evaluate safety outcomes.

### Outcome 
Adding the corridor map view was an improvement to the insights gathering process. Through this I was able to identify several other corridors with frequently occurring traffic related injuries.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Dashboard</a>
    <!-- <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Report</a> -->
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

### Plan (4 Steps)
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

### Extract, Transform, and Load
- Data source: [Crash Locations](https://data.sanjoseca.gov/dataset/crash-locations1)
- Three different datasets were collected: Crash Locations, Crash Vehicles Involved, and Safety Corridors
- Crash Locations dataset features: date, age, lighting, weather, involved, narrative, violation 
- Crash Vehicles Involved dataset features: date, direction, damage, violation
- Safety Corridors dataset features: streetname, limits, grantamount, notes

#### Apache Airflow
- Build three DAG functions to auto extract and load data into Postgresql database  
- Set Airflow to run every week to update database 

<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: Apache Airflow (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#airflow" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/airflow_vision_zero.html" frameborder="0" height="330" width="100%"></iframe>
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
    <iframe scrolling="no" src="/images/projects/visionzerosj.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>


#### QGIS
- Data source: Vision Zero Corridor dataset
- Vector tool - Add corridors
- Calculate - Update length field

![screenshot](/images/projects/qgis_snap.png)
<div class="mb-3"></div>

### Evaluate Results
- Design - Affinity Design
- Visualization - Tableau
<div class="mb-3"></div>

#### Tableau Dashboard Shapshot 📸
![screenshot](/images/projects/tableau_snap.png)
<div class="mb-3"></div>

### Conclusion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p>Downtown San Jose has always been a troublesome area for bicyclists, pedestrians, and motorists. Because of its busy streets and dense population the chances of being involved in a traffic related accident is more likely. In the last three year 7,728 traffic related injuries were recorded, most were minor injuries, but a significant amount were severe and even fatal. The Vision Zero Initiative aims to target these most troublesome streets and reimagine its use with safety as the priority.</p>
            <p>While the San Jose Vision Zero Initiative has done a good job of targeting and redesigning several corridor streets labeling them as priority, other injury prone streets have not made the list. 10th street and Santa Clara street has a record of multiple severe and fatal injuries from motorists running red lights. Capital avenue and McKee road has multiple pedestrian injuries severe and fatal caused from jaywalking. A stretch of San Carlos from Race to Bascom has multiple severe and fatal injuries by pedestrians failing to yield to cars. The opportunity to improve yet more unsafe street designs still exists.</p>
            <p>In this project we gathered traffic accident data to evaluate the safety outcomes of San Jose Vision Zero. The results of which revealed eleven corridors of interests for safety redesign in addition to the existing nineteen corridors that are already priority. For San Jose to achieve it objective and fully eliminate severe and fatal injures from traffic accidents the progress of previous redesign efforts must be focused towards safeguarding other corridors. If your interested visit <a href="https://www.sanjoseca.gov/your-government/departments-offices/transportation/safety/vision-zero" style="text-decoration:none;" target="_blank">https://www.sanjoseca.gov</a> to learn more about current action plans for San Jose Vision Zero.</p>
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

