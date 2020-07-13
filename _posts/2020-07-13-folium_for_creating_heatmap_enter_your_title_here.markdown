---
layout: post
title:      "Folium for creating heatmap# Enter your title here"
date:       2020-07-13 20:57:38 +0000
permalink:  folium_for_creating_heatmap_enter_your_title_here
---


I was given a project to predict house prices and analyze location’s effect on house prices. I found Folium which helps to create a heatmap with Choropleth() function showing average price for each zip code.
For obtaining data I imported necessary packages and load the data.
Image for post
Introduction to Folium
Folium is a powerful data visualisation library in Python that was built primarily to help people visualize geospatial data. With Folium, we can create a map of any location in the world as long as latitude and longitude values are known.
The maps created by Folium are interactive which means we can zoom in and out after the map is generated.
Folium builds on the data wrangling strengths of the Python where the data is manipulated in Python and after that visualised in a Leaflet map via Folium.
Installation of Folium
Before using Folium, we need to install it on the system by any of the two methods below:
$ pip install folium
or
$ conda install -c conda-forge folium
My project is based on King county dataset and I used King county zipcode data which is open source data. To get the average price per zipcode I calculated each zipcode’s price mean.
After that I loaded the data and filtered zipcodes.(
Image for post
Now time to call Folium for help. This wonderful tool will give us interactive functionality. It will let us drop markers on the map, build heatmaps, build heatmaps that change with time and much more. Isn’t it awesome!
Once the map object is created with Folium, we display the choropleth map using the .choropleth() method. This method binds the data contained in the data frame with the geometries of the json file.
Image for post
Image for post
As we can see from our map which is based on King county dataset it is observed that the Bellevue, Seattle and Mercer Island have the highest average house prices. Let’s see whether the top zip codes will match with the most expensive areas.
For above reason we will create list of zipcodes, lat and long and then we can create markers.
Image for post
Image for post
As recognized from the above map Northwest part of the county has higher average house prices than the rest. In additon, some zip codes average house price are remarkably high compared to the rest. It can be concluded that zipcodes can effectively predict when performing Multiple Regression Analysis on King county house data.


https://medium.com/@kristinelpetrosyan/folium-for-creating-heatmap-f3f88bd17840
