# python-api-challenge
CWRU Data Analysis Bootcamp - HW 6 Python APIs

## Contents
* WeatherPy/
  * WeatherPy.ipynb - Jupyter Notebook that created a randomized list of cities. Utilizes the OpenWeatherMap API to search for each city and stores various weather statistics about each city. Some relationships between the statistics are graphed and linear regression models are made to examine the strength of the relationships.
  * output_data/
    * Cities.csv - City data created from OpenWeatherMap API
    * 12 PNGs of graphs analyzing various relations of latitude and weather statistics
* VacationPy/
  * VacationPy.ipynb - Jupyter Notebook that reads the city data created from WeatherPy and plots them using gmaps. It searches through certain criteria to find the most desirable areas to take a vacation based on the data and uses the Google Places API to find hotels near the filtered cities. The hotels are then plotted using gmaps.
  * Cities Heatmap Full.png - Full world map of all of the cities found in WeatherPy plotted with gmaps using heatmap.
  ![heatmap](/VacationPy/Cities%20Heatmap%20Full.PNG)
  * Hotel Heatmap Popup.png - Example of the place marker function in gmaps showcasing a hotel nearby a city that fit desirable vacation conditions, displaying hotel name, city, and county in the popup. Other hotels are marked in blue along the map
  ![hotelmap](/VacationPy/Hotel%20Heatmap%20Popup.png)
  --------------------------------------------
 ## Analysis
 
 ### Cities Pulled

The number of cities pulled from the citypy was 583. Of those cities, the Open Weather Map API found 527 cities. Looking at the graphs of Northern Hemisphere data vs Souther Hemisphere data, we can see just by the amount of plot points that there appear to have been more cities selected and found using the API in the Northern Hemisphere. This makes sense by looking at the globe, we can see most of the countries with the highest population are located in the Northern Hemisphere.
### Cloudiness Plateaus

Looking at the City Latitude vs Cloudiness graph for both hemispheres, we see the data plateauing across certain percentages of clouds. Some plateaus include 0% cloudiness and 100% cloudiness. Just through reading the data we can assume that latitude and cloudiness don't have a strong relationship, but we can infer that there are some areas of the planet where certain precipitation systems are moving and they can cover a wide range of latitudes. We would need to look at longitudinal data as well to see precisely where those cloudy systems may be.
### Temperature

Looking at the City Latitude vs Max Temperature graph, we can see a negative parabol curve showing the temperature rising up to a peak then dropping as the latitude increases. The majority of the highest temperatures are seen near latitude 0, or the equator. While it sounds obvious, we can infer that the closer you get to the equator, the hotter the average temperature will be, as this data was collected during winter time, and the temperatures still max out near the equator.
