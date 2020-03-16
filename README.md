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
 Analysis located in WeatherPy.ipynb
