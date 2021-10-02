# World_Weather_Analysis

## Background
### Jack recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data you’ve already retrieved in this module. Next, the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. Using the list of potential travel destinations, the user will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, a travel route between the four cities as well as a marker layer map will be generated.

## Deliverable One: Retrival of Weather Data
### Numpy random number generator was used to generate 2,000 random numbers within the logical bounds of latitude (-90 to 90) degrees respectively; and 2,000 random numbers between the logical bounds of longitude (-180 to 180) degrees, respectivly. These number pairs were used to create a pair of latitudes and longitudes over the entire earth.  Next, citypy was used to find the closest city the matched the latitude and longitude coordinate pair.  For the coordinates used in this analysis, 705 cities were populated.  Of the 766 cities, 655 contained data without error.  
### Now that the cities are populated, an API key was used to request current weather data of all 655 cities and the following data was collected and tabulated from the internet query request: 
### City | Country | Lat | Lng | Max Temp | Humidity | Cloudiness | Wind Speed | Current Description | Date
### This data was used then exported into a tabular storage excel file labeled WeatherPy_Database.csv
### ![Fig 1 - City DataFrame]()

## Deliverable Two: Create a Customer Travel Destinations Map
### Using the WeatherPy_Database.csv file from Deliverable One; the user is asked a range of temperatures preferred for the planned vacation setting and filtering a high and low.  Cities with temperatures outside of the requested range are not included in continued analysis for vacation planning.  The temperture criteria used for the beta test was between 50 and 75 degF.  This returned 291 data complete destinations.  Next, of the 291 cities, a Google API request script was developed and used to locate hotels within 5 km of the lat/long coordinates.
### ![Fig 2 - Hotel DataFrame]()
### ![Fig 3 - WeatherPy_vacation_map.png]()

## Deliverable Three: Create a Travel Itinerary Map
### Utilizing Google Maps and Directions a travel itinerary was created from a selected four (4) cities that are within driving distance.  This beta test chose: Port Hardy, BC, Canada / Stettler, AB, Canada / Polson, MT, US / Hoquiam, WT, US
### ![Fig 4 - City_df]()
### ![Fig 5 - WeatherPy_travel_map.png]()
### A heatmap was generated using the locations chosen for the road trip to the four cities with a hotel option in each city.  The hotel returned does not check for hotel availibility.
### ![Fig 6 - WeatherPy_travel_map_markers.png]()


















