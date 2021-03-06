# Python API Challenge - How Does the Weather Change as we Approach the Equator?
CWRU Data Analysis Bootcamp - HW 6 Python APIs

## Objective
  ### Part 1 - WeatherPy
* Create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator, utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

* Build a series of scatter plots to showcase the following relationships:
 
  * Temperature (F) vs. Latitude
  * Humidity (%) vs. Latitude
  * Cloudiness (%) vs. Latitude
  * Wind Speed (mph) vs. Latitude

   Analyze each plot and explain the results.
 
* Run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

  * Northern Hemisphere - Temperature (F) vs. Latitude
  * Southern Hemisphere - Temperature (F) vs. Latitude
  * Northern Hemisphere - Humidity (%) vs. Latitude
  * Southern Hemisphere - Humidity (%) vs. Latitude
  * Northern Hemisphere - Cloudiness (%) vs. Latitude
  * Southern Hemisphere - Cloudiness (%) vs. Latitude
  * Northern Hemisphere - Wind Speed (mph) vs. Latitude
  * Southern Hemisphere - Wind Speed (mph) vs. Latitude

   Analyze each plot and explain the relationships.
 
 ### Part 2 - VacationPy
 * Create a heat map that displays the humidity for every city from the part 1.
 * Narrow down the DataFrame to find your ideal weather condition. 
 * Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.
 * Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

## Contents
* WeatherPy/
  * WeatherPy.ipynb - Jupyter Notebook that created a randomized list of cities. Utilizes the OpenWeatherMap API to search for each city and stores various weather statistics about each city. Some relationships between the statistics are graphed and linear regression models are made to examine the strength of the relationships.
  * output_data/
    * Cities.csv - City data created from OpenWeatherMap API
    * 12 PNGs of graphs analyzing various relations of latitude and weather statistics
* VacationPy/
  * VacationPy.ipynb - Jupyter Notebook that reads the city data created from WeatherPy and plots them using gmaps. It searches through certain criteria to find the most desirable areas to take a vacation based on the data and uses the Google Places API to find hotels near the filtered cities. The hotels are then plotted using gmaps.
  * Cities Heatmap Full.png - Full world map of all of the cities found in WeatherPy plotted with gmaps using heatmap plugin, displaying a relative humidity level for all of the cities.
  ![heatmap](/VacationPy/Cities%20Heatmap%20Full.PNG)
  * Hotel Heatmap Popup.png - Example of the place marker function in gmaps showcasing a hotel nearby a city that fit desirable vacation conditions, displaying hotel name, city, and county in the popup. Other hotels are marked in blue along the map
  ![hotelmap](/VacationPy/Hotel%20Heatmap%20Popup.png)
  --------------------------------------------
 ## Analysis
 
 Chart analysis located in WeatherPy.ipynb
 
 ### Cities Pulled

The number of cities pulled from the citypy was 583. Of those cities, the Open Weather Map API found 527 cities. Looking at the graphs of Northern Hemisphere data vs Souther Hemisphere data, we can see just by the amount of plot points that there appear to have been more cities selected and found using the API in the Northern Hemisphere. This makes sense by looking at the globe, we can see most of the countries with the highest population are located in the Northern Hemisphere.
### Cloudiness Plateaus

Looking at the City Latitude vs Cloudiness graph for both hemispheres, we see the data plateauing across certain percentages of clouds. Some plateaus include 0% cloudiness and 100% cloudiness. Just through reading the data we can assume that latitude and cloudiness don't have a strong relationship, but we can infer that there are some areas of the planet where certain precipitation systems are moving and they can cover a wide range of latitudes. We would need to look at longitudinal data as well to see precisely where those cloudy systems may be.
### Temperature

Looking at the City Latitude vs Max Temperature graph, we can see a negative parabol curve showing the temperature rising up to a peak then dropping as the latitude increases. The majority of the highest temperatures are seen near latitude 0, or the equator. While it sounds obvious, we can infer that the closer you get to the equator, the hotter the average temperature will be, as this data was collected during winter time, and the temperatures still max out near the equator.
