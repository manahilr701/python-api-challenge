WeatherPy Challenge
Overview
The WeatherPy challenge involves retrieving weather data from the OpenWeatherMap API for a list of randomly generated cities around the world. The main goals of this challenge are to analyze the weather data and visualize the relationships between various weather parameters and the latitude of the cities.

Table of Contents
Overview
Table of Contents
Part 1: Weather Analysis
1.1: Generate Cities List
1.2: Perform API Calls
1.3: Create Scatter Plots
Part 2: Vacation Analysis
2.1: Create a Heatmap of Weather Conditions
2.2: Narrow Down Ideal Weather Conditions
2.3: Map Hotels
Files
Installation
Usage
Conclusion
License
Part 1: Weather Analysis
1.1: Generate Cities List
Generate a list of cities using random latitude and longitude combinations and identify the nearest cities using the citipy library.

1.2: Perform API Calls
Fetch weather data for each city from the OpenWeatherMap API. The data includes:

Latitude and Longitude
Maximum Temperature
Humidity
Cloudiness
Wind Speed
Country
Date
1.3: Create Scatter Plots
Create scatter plots to visualize the relationships between latitude and the following weather parameters:

Maximum Temperature
Humidity
Cloudiness
Wind Speed
Additionally, compute the linear regression for each relationship and plot the regression line along with the scatter plot.

Part 2: Vacation Analysis
2.1: Create a Heatmap of Weather Conditions
Create a heatmap that displays the humidity of each city on a world map.

2.2: Narrow Down Ideal Weather Conditions
Filter the cities to find the ones with ideal weather conditions for a vacation. For example:

Maximum temperature between 21°C and 27°C
Wind speed less than 4.5 m/s
Zero cloudiness
2.3: Map Hotels
Using the Geoapify API, find the first hotel located within 10,000 meters of the coordinates of each city that meets the ideal weather conditions. Create a map that displays the hotel names along with the city and country information.

Files
WeatherPy.ipynb: Jupyter Notebook containing the code for Part 1 and Part 2 of the challenge.
output_data/cities.csv: CSV file containing the weather data for the cities.
output_data/Fig1.png: Scatter plot for Latitude vs. Max Temperature.
output_data/Fig2.png: Scatter plot for Latitude vs. Humidity.
output_data/Fig3.png: Scatter plot for Latitude vs. Cloudiness.
output_data/Fig4.png: Scatter plot for Latitude vs. Wind Speed.
api_keys.py: File containing the API key for OpenWeatherMap and Geoapify (not included in the repository, should be created locally).
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/your_username/python-api-challenge.git
Navigate to the project directory:
bash
Copy code
cd python-api-challenge/WeatherPy
Install the required libraries:
bash
Copy code
pip install -r requirements.txt
Usage
Obtain API keys from OpenWeatherMap and Geoapify.
Create a file named api_keys.py in the project directory and add your API keys:
python
Copy code
weather_api_key = "YOUR_OPENWEATHERMAP_API_KEY"
geoapify_key = "YOUR_GEOAPIFY_API_KEY"
Open WeatherPy.ipynb in Jupyter Notebook or Jupyter Lab and run the cells to generate the weather data analysis and visualizations.
Conclusion
Weather Analysis:
Latitude vs. Temperature: As expected, temperature decreases as one moves away from the equator. This is evident in both the Northern and Southern Hemispheres.
Latitude vs. Humidity: The relationship between latitude and humidity is not very strong, but some patterns suggest higher humidity near the equator.
Latitude vs. Cloudiness: The data shows no strong correlation between latitude and cloudiness, indicating that cloud cover is influenced by more localized factors.
Latitude vs. Wind Speed: There is a slight increase in wind speed as one moves away from the equator, particularly noticeable in the Northern Hemisphere.
Vacation Analysis:
Ideal Weather Conditions: By filtering for ideal weather conditions, we identified several cities around the world that would make good vacation destinations.
Hotel Mapping: Using the Geoapify API, we were able to find and map hotels in these ideal cities, providing valuable information for potential travelers.
The analysis demonstrates the ability to leverage APIs and data visualization tools to gain insights from real-world data, helping to make informed decisions based on weather patterns.
