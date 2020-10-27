# <center> Capstone Project (Week 1) </center>

## <center> *Opening the Irish Pub in Moscow, Russia* </center>

<img src="https://irishpapaspub.ru/wp-content/uploads/2017/05/about-us-2.jpg">

## <center> Introduction </center>

In recent years, the number of pubs in Russia (especially in the Central region) has increased dramatically. Some attribute this not so much to British exoticism, but to the increasing culture of beer consumption in the country and the desire to abandon the low-quality product that is offered by a mass producer.
<br>In this study, I want to analyze and determine the **optimal places for the location of an Irish pub in Moscow**.</br>
<br></br>
<br>**Moscow** is the capital and largest city of Russia. Moscow is among the world's largest cities, being the most populous city entirely within Europe, so owners can easily find potential customers here. </br>
<br>Moscow is divided into twelve administrative okrugs and 123 districts. </br>
<br> In this city, there are people who are happy to go to the pub to have a beer with friends and relax after a hard working week, or just to have a good time together.</br>

## <center> Business problem </center>

**The owners of the pubs**  who are the target audience of this study often face the need to expand an existing pub chain or launch a completely new pub.
<br>It is obvious that the owners of pubs are interested in making their establishment bring a noticeable income. To do this, they should choose cities where there are people interested in opening a pub, and there is also a great area (preferably with low competition) where they can open a pub.</br>
<br></br>
<br> This study aims to help owners choose the best pub location based on the following data:</br> 
* population density; 
* location of competitors (other pubs, restaurants, and cafes).

## <center> Data sources & their description </center>

Based on the problem above, I will need the following data:
* Information about districts and settlements in Moscow (name of the district, administrative district, population density, etc.) from <a href="https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D1%80%D0%B0%D0%B9%D0%BE%D0%BD%D0%BE%D0%B2_%D0%B8_%D0%BF%D0%BE%D1%81%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B9_%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D1%8B">Wikipedia</a>;
* Each district has its own geographical coordinates, this information was obtained using the site <a href="https://nominatim.openstreetmap.org/ui/search.html">Nominatim</a>. Nominatim uses OpenStreetMap data to find locations on Earth by name and address;
* <a href="https://ru.foursquare.com/">Forsquare API</a> was used to fing out the location of competitors (latitude and longitude).
