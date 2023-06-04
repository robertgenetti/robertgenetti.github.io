---
title: "Covid-19 Vacc"
order: 0
image: "/images/projects/covid19vacc.png"
gif: "/images/projects/covid19vacc.gif"
link: "https://public.tableau.com/views/Book1_16627808205440/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link"
---

In the early days of the Covid-19 Pandemic, international policy makers and world health officials were put in the precarious position of crafting policy in response to growing demand for defensive measures against the spread of the virus. This project takes a look at the aggregate effects of restrictive social and economical policy during this time and asks the question _how were national vaccination rates impacted by policy decisions?_ 

### Goal
The project measures both aggregate and national health data to assess the impacts of national policy responses. The intent of this project is to provide information and a means for identifying future opportunities of improvement in tracking and measurement of vaccinaitons rates across income groups.

### Outcome 
The outcome of this project illustrate a clear distinction between high and low income demographics in response to policy encouraging vaccinations. High and middle high income groups have the largest percentage of vaccination rates compared to that of lower income groups. More interestingly this pattern holds true for most of the world population and across rich/poor nations.

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Dashboard</a>
    <!-- <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;" target="_blank">Report</a> -->
</div>


### Project Overview
<p><b>Role:</b> Data Analyst</p>
<p><b>Requirements:</b> Develop a global vaccinations dashboard</p>
<p><b>Timeline:</b> Approximately 80 hours</p>
<p><b>Tools:</b> Python, JupyterLab, Docker, SQL, Azure Data Studio, Tableau</p>

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
            <h3>Evaluate</h3>
            <img src="/images/projects/Visual.png" style="width:100px; height:auto; object-fit: cover;">
        </div>
    </div>
</div>

<div class="mb-3"></div>

### Plan (3 Steps)
1. Extract, Transform, and Load
    - Pull dataset from Our World in Data
    - Transform data in Pandas
    - Load datasets into PostgreSQL Database
2. Query PostgreSQL Database
    - Get vaccination data by nation
    - Get List of countries by fatality count
    - Get vaccination data by income
3. Design Tableau dashboard
    - List highest fatality countries
    - Map of vaccination data
    - Graph vaccination status by income

### Extract, Transform, and Load
Utilizing a data science stack in Docker I was able to run an ETL Python script in JupyterLab to extract data from Our World In Data dataset, transform, and load it into PostgreSQL database. The only challenge in this part of the project was isolating the correct data fields to be converted into string and date data types, all other data types remain unchanged. This step, while minor, saved time later when importing the datasets and building a data visualization.

- Tools: JupyterLab, Postgresql Database, Docker
- Data source: [Our World In Data - Coronavirus Pandemic](https://ourworldindata.org/coronavirus)
- Rows of data: 214706
- Pandas ETL - Our World In Data
<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: JupyterLab Code (Python)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#python" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/owid-covid.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

### Analyze Data
Once the data was stored in Postgresql, I began to analyze the data with SQL queries using Azure Data Studio. Feature selection is a process the defines the research question and narrows the scope context. In this case, looking at the data, it was clear the analysis would benefit from scoping the research question to vaccination rates and income groups. I also wanted to include other critical measures to support the analysis.

- Tools: Azure Data Studio
- Features of interest: location, date, cases, deaths, vaccinations, population

<div class="my-3">
    <div class="row justify-content-between mt-4 px-1">
        <h4>Code Snippet: Azure Data Studio Code (SQL)</h4>
        <a href="{{site.baseurl}}{{ page.url }}/code#sql" class="button button-primary" style="text-decoration:none;">View Code</a>
    </div>
    <div style="border: 1px solid #dcdcdc;">
    <iframe scrolling="no" src="/images/projects/covid.html" frameborder="0" height="330" width="100%"></iframe>
    </div>
</div>

### Evaluate Results
One of the most important features of this Tableau Dashboard is the segmentation of income groups by vaccination rates, which shows clearly the differences in global vaccination rates between income groups.

- Tools: Tableau Desktop
- Illustrate vaccination rates for income groups
- Show aggregate values for national health metrics
- Map countries with vaccination rates by color variance

<div class="mb-3"></div>

#### Tableau Shapshot 📸
![screenshot](/images/projects/book1.png)
<div class="mb-3"></div>

### Discussion
<div class="container">
    <div class="row justify-content-between">
        <div class="col-12 col-md-6 mb-5">
            <p></p>
            <p></p>
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



