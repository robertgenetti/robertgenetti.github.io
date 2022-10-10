---
title: "Seattle Housing"
image: "/images/projects/seattlehousing.png"
gif: "/images/projects/seattlehousing.gif"
link: "https://public.tableau.com/views/Book2_16641659196370/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link"
---

This project takes publicly available data from Washington's King county records to look at recent in foreclosure properties. The data is collected then merged with geolocation to be used in an interactive map representation.

### Problem

My initial thoughts when starting this project focused on increasing the usefullness of the data. As it was the publicly available date was just a table of records. By collecting the data in python and merging it with geolocation data I was able to display the data as a much more useful visualization. 

### Solution

The project makes use of several python packages that are essential to the collecting, formating and displaying of data.   

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-2 mb-6" style="text-decoration:none;">View Dashboard</a>
</div>

### Method

The first few cells of the jupyter notebook are just for initialization purposes. After that the user can input how many weeks of records to collect. Selenium sebdriver and Beautiful soup then scrape the website for data and return it as Pandas data tables. 

![screenshot](/images/projects/records.png "King County Records")

After the records are collected as Pandas tables they get merged with location data. The data is then used in Folium to generate a map vizualization. The final result can be seen below - a map of pins for each record along with summery information when clicked.

### Content

The result is a user friendly visualization of the data. The user can easily look in the area of interest and select the property for more information. The summary information that is displayed is as follows:

- Address
- Neighborhood
- Metropolitan
- Appraised Value
- Parcel Identification Number
- Record Date

The python code is available at [king_county_foreclosures.ipynb](#https://colab.research.google.com/drive/1aG52L321RsyHK6OJNmJmdugBtXDewjSH?usp=sharing).

### Conclusion
<div class="row justify-content-start">
<div class="col-6">
Future plans include expanding the map features so that when a user clicks on a property link it sends then to a detail page with more information. Another improvement would be to integrate the program into an app or website to be used as a service or online reference. 

<div class="col-12 text-center">
    <a href="{{page.link}}" class="button button-primary mt-6" style="text-decoration:none;">View Dashboard</a>
</div>

</div>
<div class="col-6">
<div class="whitebox" ><a href="{{page.link}}" target="_blank">
<img src="{{page.gif}}" alt="{{page.title}}" style="width:100%; height:auto; object-fit: cover;">
</a>
</div>
</div>
</div>



