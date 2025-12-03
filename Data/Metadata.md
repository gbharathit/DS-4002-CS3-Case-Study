# Metadata

## Data Summary

Our dataset consists of the means of the maximum and minimum temperatures of each month in a certain year. Since there is an observation for each unique month and year from 2000-2023, there are a total of 288 rows. For each row, there are five columns, three of which help organize the month and year of the observations. One of the other columns gives the mean of the maximum temperatures in that month, while the last one gives the mean of the minimum temperatures in that month. Our data is in a CSV file, which can be find in our Github repository: DS-4002-Project-2 / DataFolder / AverageTemps.csv https://github.com/gbharathit/DS-4002-Project-2

## Provenance

The dataset originates from the National Oceanic and Atmospheric Administration (NOAA), “Climate” National Weather Service, which includes average temperature for each month from January of 2000 to September 2025. Initially, there was a different dataset for average minimum temperatures and average maximum temperatures. We decided to merge these into one dataset, removing repetitive columns. We also have begun applying time series formatting to our data, so that the data is displayed in a grid format with columns representing months and rows representing years. Because we do not have data for the entire year of 2025, data from this year has been removed. We also had to convert data from the NOAA website into a suitable CSV, since it was not in a downloadable format. We used AI tools in order to copy and paste the original data from the website and create code that would make this data into a table in R that we could then export to a CSV.

## License

The original dataset is made publicly available through NOAA. Our cleaned version and analysis outputs will be shared in our GitHub repository under the same open-use conditions, following NOAA’s licensing requirements and citing NOAA and National Weather Service. 

## Ethical Statements

There are no ethical considerations because our dataset deals with climate and temperatures. Because we are not predicting future weather, such as weather in November 2025 and beyond, we don’t have to worry about making any concrete statements that could be affected by external factors. We are simply comparing predictions made by our model with actual data recorded in 2024. 

## Data Dictionary

| Column | Description | Potential Response |
| :------- | :------- | :------- |
| Month_Year | Month abbreviation and year of when temperatures were collected | Jan_2000, Oct_2014, Jun_2023 |
| Year | Year of when temperatures were collected | 2000, 2010, 2023 |
| Month | Month abbreviation of when temperatures were collected | Jan, Jul, Dec|
| Max_Value | Mean maximum temperatures of each month in a certain year, rounded to the nearest tenth | 47.9, 64.8, 80.9|
| Min_Value | Mean minimum temperatures of each month in a certain year, rounded to the nearest tenth | 20.9, 38.4, 76.8|

## Exploratory Plots
![JanTrends](https://github.com/gbharathit/DS-4002-Project-2/blob/main/OUTPUT/1jantrends.png?raw=true)

We identified January and June to see if there has been a consistent increase in temperatures in both summer and winter. As we can see, despite there being some fluctuations in the data, the general trend for both average minimum and maximum temperatures in January has been increasing. 

![JunTrends](https://github.com/gbharathit/DS-4002-Project-2/blob/main/OUTPUT/2juntrends.png?raw=true)

Again, we see that the general trend for both average minimum and maximum temperatures in June has also been increasing. It is interesting though that the temperatures took a slight dip in June 2024, which is something our model might not account for due to the general increasing trend.

![MaxTimeSeries](https://github.com/gbharathit/DS-4002-Project-2/blob/main/OUTPUT/3maxtimeseries.png?raw=true)

Removing seasonality allows us to see what the trend is over time for both minimum and maximum temperatures from 2000 to 2023 (second row in both graphs). The trends for average maximum data show an increase in temperatures over the years. Seasonality component is the third row in both graphs, which shows there is a clear and consistent seasonality trend as is expected with weather data. 

![MinTimeSeries](https://github.com/gbharathit/DS-4002-Project-2/blob/main/OUTPUT/4mintimeseries.png?raw=true)

Again, we see that the trends for average minimum data also show an increase in temperatures over the years. Seasonality is also present in this data, which again makes sense due to the fact that we are dealing with weather
