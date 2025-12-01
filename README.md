# Charlottesville Weather Forecast Project

This repository contains everything needed to reproduce a time series model (ARIMA model, to be specific) that is built using weather data from Charlottesville, VA in 2000-2023 in order to predict weather in 2024. It includes a dataset of historical weather data for Charlottesville, VA, as well as scripts and outputs to forecast 2024 monthly average temperatures. This project analyzes trends, seasonality, and anomalies in monthly minimum and maximum temperatures from 2000–2023 using ARIMA modeling. The cleaned dataset, exploratory analyses, and model predictions are included to enable reproduction of all results.

## Contents of this repository
This repository contains everything needed to reproduce the analyses and results for this project: raw and cleaned weather data, R scripts for preprocessing and analysis, output plots, and predicted 2024 temperature data. The sections below outline software requirements, repository structure, and step-by-step instructions to reproduce the results.

---

## Section 1: Software and platform

**Software Used:**
- R Studio for data cleaning, exploratory analysis, and ARIMA modeling.
- Git for version control and GitHub for hosting.

**Add-on R packages required (install with `install.packages()` or via `renv`)**
- `tidyverse` (includes `dplyr`, `ggplot2`, `readr`, `tibble`, etc.)
- `rmarkdown`, `knitr` (rendering reports) , `vader`, `forecast`

## Section 2: Map of Documentation

 1. **Data Folder**
  - **Initial Data Folder**
    - `mean_max_monthly_temps_2000_2025.csv` – Just the mean maximum monthly temperature data. 
    - `mean_min_monthly_temps_2000_2025.csv` – Just the mean mimimum monthly temperature data.
  - **Final Data Folder**
    - `AverageTemps.csv` – Full dataset with months and years, as well as the mean maximum and minimum temperature values used in analysis.  
  
 2. **Scripts Folder**
  - `1) Data Cleaning and EDA.Rmd` – Script where data is cleaned and combined into one .csv file, as well as setting up for time series analysis and creating EDA plots
  - `2) Model Building.Rmd` – Script where time series model is built and analyzed

3. **Supplemental Materials Folder**
  - `Forecasting the Future_ The Role of Artificial Intelligence in Transforming Weather Prediction and Policy.pdf` - How can AI be used to optimize weather forecast prediction
  - `Time Series Analysis in R.pdf` - Basic introduction to conducting time series analysis in R
  - `Why warming makes weather less predictable _ Stanford Report.pdf` - Why are weather forecasts less accurate, and how has global warming contributed to this?

4. `CS3 Hook Document - Weather.pdf` - Hook Document (hard copy provided)
5. `CS3 Rubric - Weather.pdf` - Rubric (hard copy provided)

## Section 3 – How to Reproduce Our Results

If you want to reproduce our analysis and see all the figures and tables from our project, follow these steps:

1. **Get the Repository**
   - Clone the repo using Git:
     ```bash
     git clone https://github.com/gbharathit/DS-4002-CS3-Case-Study.git
     ```
   - Or download it as a ZIP file and extract it.
   - Open RStudio and set your working directory to the project folder.

2. **Make Sure the Data Files Are There**
   - The following CSV files need to be in the **same folder** as `1) Data Cleaning and EDA.Rmd` and `2) Model Building.Rmd`:
     - `mean_max_monthly_temps_2000_2025.csv`
     - `mean_min_monthly_temps_2000_2025.csv`
     - `AverageTemps.csv`
   - These files are included in the repository, so you shouldn’t need to download anything else.

3. **Install R and Packages**
   - We used **R** (version 4.0 or higher) and RStudio.
   - Install the packages we used if you don’t already have them:
     ```r
     install.packages(c("tidyverse", "dplyr", "ggplot2",
                        "tidytext", "forecast", "knitr", "rmarkdown"))
     ```
4. **Clean the Data and Perform EDA**
   - Open `1) Data Cleaning and EDA.Rmd` in RStudio
   - Click **Knit** to run all the code and generate the full report.
   - This will produce the HTML (or PDF) report with our EDA plots.

4. **Run the Analysis**
   - Open `2) Model Building.Rmd` in RStudio.
   - Click **Knit** to run all the code and generate the full report.
   - This will produce the HTML (or PDF) report with all of our results and model outputs.

5. **Troubleshooting**
   - Make sure your working directory is the project folder and the CSV files are in the right place.
   - If anything seems off, you can run `sessionInfo()` in R to check your package versions.
   - 
## References

[1] National Oceanic and Atmospheric Administration, “Climate,” National Weather Service. [Online]. Available: https://www.weather.gov/wrh/Climate?wfo=lwx. [Accessed: Oct. 6, 2025]. National Weather Service

[2] A. Coghlan, “A Little Book of R for Time Series.” [Online]. Available: https://a-little-book-of-r-for-time-series.readthedocs.io/en/latest/src/timeseries.html. [Accessed: Oct. 6, 2025]. A Little Book of R for Time Series

[3] J. Noble, “What are ARIMA Models?,” IBM THINK. [Online]. Available: https://www.ibm.com/think/topics/arima-model. [Accessed: Oct. 6, 2025].  IBM

[4] J. D. Long and P. Teetor, R Cookbook: Proven Recipes for Data Analysis, Statistics, and Graphics, 2nd ed., O’Reilly Media, 2019. [Online]. Available: https://rc2e.com/timeseriesanalysis. [Accessed: Oct. 6, 2025]. R Cookbook

[5]  R. Lindsey, “Climate change: global temperature,” Climate.gov, May 29, 2025. [Online]. Available: https://www.climate.gov/news-features/understanding-climate/climate-change-global-temperature. [Accessed: Oct. 8, 2025].

[6] “How Has Technology Changed Weather Forecasting for Meteorologists?,” Visual Crossing, Jul. 30, 2024. [Online]. Available: https://www.visualcrossing.com/resources/blog/how-has-technology-changed-weather-forecasting-for-meteorologists/ [Accessed: Oct. 8, 2025].

[7] OpenAI, “ChatGPT conversation: ‘Model and tutorial assistance,’” ChatGPT, Oct. 20, 2025. [Online]. Available: https://chatgpt.com/share/68f6ae26-429c-8004-9ffd-14853e60839d
. [Accessed: Oct. 22, 2025].

[8] World Meteorological Organization, “Forecasting the future: The role of artificial intelligence in transforming weather prediction and policy.” [Online]. Available: https://wmo.int/media/magazine-article/forecasting-future-role-of-artificial-intelligence-transforming-weather-prediction-and-policy
. [Accessed: Dec. 1, 2025].

[9] A. Marin, “Warming makes weather less predictable,” Stanford University News, Dec. 15, 2021. [Online]. Available: https://news.stanford.edu/stories/2021/12/warming-makes-weather-less-predictable
. [Accessed: Dec. 1, 2025].

[10] GeeksforGeeks, “Time Series Analysis in R.” [Online]. Available: https://www.geeksforgeeks.org/r-language/time-series-analysis-in-r/
. [Accessed: Dec. 1, 2025].
