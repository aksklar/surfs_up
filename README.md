# Surfs Up!
## Advance Data Storage &amp; Retrieval

In this project, I was tasked with creating a climate analysis API with Hawaii weather data.  In order to achieve the goal of this project, I did the following:
1. **Data Engineering:** With the provided climate data, I created a Jupyter Notebook file to clean the data.
2. **Database Engineering:** With the cleaned data, I created a Jupyter Notebook file to create a sqlite database for the climate data.
3. **Climate Analysis and Exploration:**  I created another Jupyter Notebook file to reflect the sqlite database with SQLAlchemy.
    * Precipitation Analysis: I designed a query to retrieve the last twelve months of precipitation data.  With this data, I created a bar chart with Matplotlib and a statistical summary.
    * Station Analysis: I designed a query to retrieve the last twelve months of temperature observation data.  With this data, I created a histogram chart with Matplotlib.
    * Temperature Analysis: I created a function that accepts and start and end date (YYYY-MM-DD format) and returns the minimum, average, and maximum temperatures for the range of dates.  With the returned results, I plotted a singular bar chart with Matplotlib that uses the average temperature and the minimum and maximum temperatures as the y error bar.
4. **Climate App:** I created a Flask API based on the queries in the previous step. There are four routes:
    1. /api/v1.0/precipitation: Returns a json list of dates and corresponding temperature observations.
    2. /api/v1.0/stations: Returns a json list of stations from the dataset.
    3. /api/v1.0/tobs: Returns a json list of temperature observations
    4. /api./v1.0/<start> and /api./v1.0/<start>/<end>: Returns a json list of the minimum temperature, the average temperature, and the maximum temperature of a given start or start-end date range.
