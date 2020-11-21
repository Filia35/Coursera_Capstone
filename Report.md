# <center> Capstone Project (Week 2) </center>

## <center> *Opening the pub in Moscow, Russia* </center>

<img src="https://irishpapaspub.ru/wp-content/uploads/2017/05/about-us-2.jpg">

## <center> Introduction </center>

In recent years, the number of pubs in Russia (especially in the Central region) has increased dramatically. Some attribute this not so much to British, Irish and Czech exoticism, but to the increasing culture of beer consumption in the country and the desire to abandon the low-quality product that is offered by a mass producer.
<br>In this study, I want to analyze and determine the **optimal places for the location of an Irish pub in Moscow**.</br>

<br>**Moscow** is the capital and largest city of Russia. Moscow is among the world's largest cities, being the most populous city entirely within Europe, so owners can easily find potential customers here. </br>
<br>Moscow is divided into twelve administrative okrugs and 123 districts. </br>
<br> In this city, there are people who are happy to go to the pub to have a beer with friends and relax after a hard working week, or just to have a good time together.</br>

## <center> Business problem </center>

**The owners of the pubs**  who are the target audience of this study often face the need to expand an existing pub chain or launch a completely new pub.
<br>It is obvious that the owners of pubs are interested in making their establishment bring a noticeable income. To do this, they should choose locations where there are people interested in opening a pub, and there is also a great area where they can open a pub.</br>
<br> This study aims to help owners choose the best pub location based on the following data:</br> 
* population density; 
* price of apartments in different areas;
* location of competitors (other pubs and bars).

## <center> Data sources & their description </center>

Based on the problem above, I will need the following data:
* Information about districts and settlements in Moscow (name of the district, administrative district, population density, etc.) from <a href="https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D1%80%D0%B0%D0%B9%D0%BE%D0%BD%D0%BE%D0%B2_%D0%B8_%D0%BF%D0%BE%D1%81%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B9_%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D1%8B">Wikipedia</a>;
* Each district has its own geographical coordinates, this information was obtained using the site <a href="https://nominatim.openstreetmap.org/ui/search.html">Nominatim</a>. Nominatim uses OpenStreetMap data to find locations on Earth by name and address;
* Lists of objects and geodata for all administrative-territorial divisions in Moscow <a href="https://gis-lab.info/qa/moscow-atd.html">Geo</a>;
* Rating of Moscow districts by apartment <a href="https://www.mirkvartir.ru/journal/analytics/2018/02/25/reiting-raionov-moskvi-po-stoimosti-kvartir/">price</a>;
* <a href="https://ru.foursquare.com/">Forsquare API</a> was used to find out the location of competitors (latitude and longitude).

## <center> Methodology section (data preparation & analysis)  </center>

### <center> Block 1. Data preparation </center>

I start with importing the necessary libraries and loading the all necessary data such as:
* Moscow Boroughs
![image.png](attachment:image.png)

* Coordinates of each borough
![image.png](attachment:image.png)

* Housing Price for each borough
![image.png](attachment:image.png)

* Population Density dataset
![image.png](attachment:image.png)

At the end, I created the result Moscow Boroughs dataset:

![image.png](attachment:image.png)

After this, it was necessary to create a map of Moscow Boroughs

![image.png](attachment:image.png)

Work with Foursquare API allows to get full information about each cell & venue:

![image.png](attachment:image.png)

GeoJSON file with boroughs allows to create geometry shape and correlate each venue to Moscow Boroughs where they were placed:

![image.png](attachment:image.png)

Then I removed the venues that located outside of the Moscow districts.

The first block of loading, processing, and preparing data for further analysis *is completed*.

### <center> Block 2. Data analysis </center>

The second block starts with descriptive statistical analysis, where i got basic statistics for all features:

![image.png](attachment:image.png)

Moscow Boroughs has non-uniform population from 12 264 to 254 142 people. The housing price varies from 109 421 to 438 568 rubles/m².

Then i created boxplots:

![image.png](attachment:image.png)

Right boxplot demonstrates that feature ‘District’ can be a good predictor for ‘Housing Price’.

Correlation matrix:
![image.png](attachment:image.png)

I used the Pearson Correlation Coefficient and P-value to determinate features with significant correlation & strong relationship:

![image.png](attachment:image.png)

Correlation between 'Area' to 'Population Density' is significant and the linear relationship is strong. The same we can say about 'Housing Area' and 'Population'.

Then I used K-means to get clusters of boroughs: 
![image.png](attachment:image.png)

Cluster № 1 has the highest mean population and population density, also it has the smallest mean housing price, so it is perfect for solving the task that I set myself in this project.

Clusters visualizing:

![image.png](attachment:image.png)

I used the identification of the dataset that includes our potential competitors in Cluster 1 by using the name of Venue categories:

![image.png](attachment:image.png)

Visualizing all potential competitors in Cluster 1:

![image.png](attachment:image.png)

## <center> Results </center>

As a result we define the best areas for the location of the pub, according to these criteria:

* high population in the area;
* low cost of apartments in the area.

Also we got list and location of our potential competitors.

## <center> Discussion </center>

As a result of this project, a large amount of information was collected about Moscow boroughs and venues, all collected data were listed in the Methodology section. 

Since the information will be publicly available, anyone can access it if necessary to use it in their future research. 

Perhaps future research can use a different approach to data visualization, delve into segmentation of existing pubs and bars, and take into account all existing cafes and restaurants.

## <center> Conclusion </center>

In conclusion, I would like to say that I hope that the results of my report can help owners to find the best place for their new pubs.
