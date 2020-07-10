# Coursera Capstone Project Report

## Applied Data science Capstone by Coursera/IBM

## Table of contents
* Introduction: Business Problem
* Data
* Methodology
* Analysis
* Results and Discussion
* Conclusion

## Introduction: Business Problem 

<p> In this project I will be exploring the location data for Toronto, Canada to come up with possible areas that can be used to open an Chinese restaurant This can be used by any stakeholders who may be looking for an optimal location to open a Chinese restaurant. The stakeholders are looking forward to invest in one of these areas and would want a location that they can be able to make the best out of what they are investing that is such that they dont open in a wrong location or a place where they may never be able to make profit since its a business and not some charity organization. So for this project We are going to focus on areas that do not have any Chinese restaurant and as well as areas that are not crowded with any restaurants yet, also we will also look at areas that have a dense population. These will serve as the key elements we will be using for our analysis </p>

<p> For this we will be using our analytics knowledge to come up with few possible locations that we will be suggesting for the stakeholders involved</p>

## Data 

For this project we will focus on using data that is related to the conditions that we have mentioned above like

* number Chinese restaurants in each neighborhood
* number of people living per the surface area in the neighborhoods
* number of restaurants in each neighborhood

<p> The sources we will be using are: Foursquare api in order to get the neighborhoods around Toronto, the number of restaurants and the type of restaurants located in them. This is going to help us get all the venues that are in all the locations in Toronto. The category we are going to be using here is food so that we get only data related to food. With this data we will be analysing to see areas where we can suggest to open the restaurants We will also use the Google's geopy api in order to get the location data of Toronto city like the longitude and latitud. This is going to help us when we are trying to plot the various locations as are on the map of Toronto </p>

<p> We will also be scraping data on Toronto neighborhoods from a wikipedia page using the beautiful soup package. This data will contain all the Boroughs that are in Toronto as well as their neighborhoods. This data will also have the location data (longitude and longitude) which we will use to get the venues with the foursquare api </p>

## Data Analysis

We performed exploratory data analysis on the data to understand the data better. After getting the Toronto location data using geopy and added all the various neighborhoods to it as can be seen below.

![Screenshot](map.png)
![Alt text]("enter repository image URL here")

After that we continued exploring the data and merged the different columns that were in the different datasets to a single dataframe

![Screenshot](merged.png)

Later removed features that were not relevant and grouped by neighborhood in order to calculate the number of restaurants in each area and to check if there were chinese restaurants there 

![Screenshot](chinese.png)

from the dataframe we saw that there are very few locations with chinese restaurants in them

![Screenshot](bar.png)

We later scale the data and try using the elbow method to check the optimal value to be used in the kmeans clustering algorithm using different inertia values from 1 to 20

![Screenshot](clusters.png)

From the above visualization we then decided to move forward with five clusters in our kmeans algorithm and eventually came up with our clusters


## Methodology

<p>In this project we focused more on three main components which are the number of restaurants in the area, if there is already a restaurant in the area and the population density.</p>

<p>Firstly, we collected data that we will be using in the project from foursquare api, scraped a wikipedia page for the Toronto neighborhood data, the geopy api to get the location cordinates for Toronto and Toronto census data to get the population density of all the neighborhoods</p>

<p>Secondly, we looked at the two dataset and removed the features that we needed and merged them into a single table for our analysis</p>

<p>Thirdly, we segmented the dataset into different clusters based on the different patterns in the data. We used the elbow method where we had to plot different inertia values for different clusters and eventually came up with the optimal number of clusters for our dataset</p>

## Results and Discussions

<p>From our analysis, we discovered that there are a few neighborhoods that have chinese restaurants in them so there is a great opportunity for stakeholders to take advantages of since they will not have any competitors in those areas.</p>

<p>Also after trying to plot the elbow of the various inertias we saw that five could be an optimal value to plot, as can be seen in the graph. This then gave us five different clusters which seemed to have really close properties. The first cluster has just 1 value with 12 having restaurants and no chinese restaurant but with a high population density, cluster two has just two neighborhoods with 1 restaurant only but no chinese restaurant. Cluster 3 has no values, Cluster 4 has a mixture of a lot of different restaurants but then they all have a chinese restaurant already so we will not really focus on it. And finally the fifth cluster which also seems explorable as most of the locations have just one or two restaurants and no chinese restaurant but then the population density is a bit low.</p>

<p>Since these are the three main factors we agreed on with the stakeholders, we will be limiting our analysis to this only for now</p>

## Conclusion

<p>The main purpose of this project was to come up with possible locations that stakeholders can use to pick and optimal location to open a restaurant.We used different data collection methods like foursquare api to get the data, so from here we will be giving our proposed locations to the stakeholders who will then perform further analysis to eventually pick their final location. Major categories have been discovered from our analysis through clustering of the data which will then give the stakeholders a direction on how to go</p>

<p>For further analysis stakeholders may want to look at factors like household income level, ethnic groups, accessibility to the area, noise and a lot more</p>