# python-api-challenge

This challenge had two parts: (1) WeatherPy and (2) VacationPy.

## WeatherPy

In this part of the challenge we needed to generate random geographical coordinates and compare that to weather data, based on the hypothesis that as you travel closer to the equator, the air temperature is warmer.

In order to accomplish this, we used an approach based on citypy, a program that will find the nearest city given a pair of coordinates (latitude & longitude). We then used the OpenWeather API to get data for those cities.

My program generates sets of cities, 10 at a time, based on a function I created to generate latitude & longitude (using starter code) and leveraging citypy to return a city name. I then programmed a while-loop that would continue generating sets of cities, checking to see if OpenWeather contains data for them, until we had a list of over 500 cities. The data we were asked to pull were:

• Max Temperature
• Humidity
• Cloudiness
• Wind Speed
• Country Code
• Date Timestamp

Using the data we were then asked to generate several scatterplots and linear regressions in order to see if there was a relationship between latitude and any of the weather phenomena we pulled. The only relationship that was indicated by a strong correlation was temperature, but it wasn't a perfect correlation.

## VacationPy

Part II of the challenge involved taking this city data and creating a heatmap of humidity using the gmaps program. The idea was to narrow down our list of 500 cities in order to plan a potential vacation.

After creating a heatmap of humidity, we then were asked to input a set of ideal weather conditions and find cities that met that criteria (narrowing it down until we could have just 10 cities). We then took those 10 cities and requested data from the Google Places API in order to locate the nearest hotels.

Adding these hotels to the heatmap, we created a final product that allowed us to see where we might travel for a "perfect getaway". Alas, at the time of writing this program this seems like a fantasy given we are in the middle of a global pandemic… but hopefully someday I can actually take a nice vacation somewhere with ideal weather!
