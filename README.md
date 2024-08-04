# sqlalchemy-challenge

## Module 10 Challenge - Advanced SQL

#### Congratulations to me! I've decided to treat myself to a long holiday vacation in Honolulu, Hawaii! To help with my trip planning, I wanted to do some climate analysis for the area. The following outlines are the guidelines I needed to follow to get the best possible information to make my stay so awesome:

### Task 1 - Climate Analysis and Exploration
#### To begin, I used Python and SQLAlchemy to do basic climate analysis and data exploration of my climate database. All of the following analysis was completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

#### * Use the provided starter notebook and hawaii.sqlite files to complete my climate analysis and data exploration.
#### * Choose a start date and end date for my trip. Make sure that my vacation range is approximately 3-15 days total.
#### * Use SQLAlchemy create_engine to connect to my sqlite database.
#### * Use SQLAlchemy automap_base() to reflect my tables into classes and save a reference to those classes called Station and Measurement.

### Precipitation Analysis
#### * Design a query to retrieve the last 12 months of precipitation data.#### Select only the date and prcp values.
#### * Load the query results into a Pandas DataFrame and set the index to the date column.
#### * Sort the DataFrame values by date.
#### * Plot the results using the DataFrame plot method.
#### * Use Pandas to print the summary statistics for the precipitation data.

### Station Analysis
#### * Design a query to calculate the total number of stations.
#### * Design a query to find the most active stations                                                                  
#### * List the stations and observation counts in descending order.
#### * Which station has the highest number of observations?
#### * Design a query to retrieve the last 12 months of temperature observation data (tobs).
#### * Filter by the station with the highest number of observations.
#### * Plot the results as a histogram with bins=12.

## Task 2 - Climate App
### Now that I have completed my initial analysis, design a Flask API based on the queries that I have just developed.
#### * Use FLASK to create my routes.

### Routes

* `/`
  * Home page.
  * List all routes that are available.
* `/api/v1.0/precipitation`
  * Convert the query results to a Dictionary using `date` as the key and `prcp` as the value.
  * Return the JSON representation of your dictionary.
* `/api/v1.0/stations`
  * Return a JSON list of stations from the dataset.
* `/api/v1.0/tobs`
  * query for the dates and temperature observations from a year from the last data point.
  * Return a JSON list of Temperature Observations (tobs) for the previous year.
* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`
  * Return a JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.
  * When given the start only, calculate `TMIN`, `TAVG`, and `TMAX` for all dates greater than and equal to the start date.
  * When given the start and the end date, calculate the `TMIN`, `TAVG`, and `TMAX` for dates between the start and end date inclusive.
#### Hints
* You will need to join the station and measurement tables for some of the analysis queries.
* Use Flask `jsonify` to convert your API data into a valid JSON response object.





