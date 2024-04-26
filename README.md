# Project: Analysis of Capital Bike Share Database
## Premise of the project: 
Capital Bikeshare (also abbreviated CaBi) is a bicycle-sharing system which serves Washington, D.C. The goal of our projects is to find what is the behavior of the customers at night(22pm-5am), 
as well as to create a Machine Learning model which would support the planning team by forcasting the night rides per hour in order to ensure regular maintenance of the bikes during the right hours.
## DATA: 
 * provided by Code Academy Berlin
 * 3 separate datasets: Hourly, Daily Records (including weather codes and temperature BUT no station names) and Full Dataset (including station names BUT no data about the weather)
 * time period: 2021-2023 
 * Original data: https://capitalbikeshare.com/system-data

# Part 1(EDA): Night usage of the Capital bike share 2021-2023
## Python libraries used: numpy, pandas, matplotlib, seaborn,folium
## The full dataset was filtered to rides staring 22pm - 5am, reference: night.ipynb
## Steps:
   * data preparation and wrangling
   * feature engineering
   * creating plots based on year, month, hour, season, user type, bike type
   * mapping top 5 stations from which bikes had disappeared (unknown end station)
   * mapping acitvity in different hours and days
   * creating a moving heatmap per hour for different seasons
# Part 2: Machine Learning model for forecasting number of rides
## Python libraries used: numpy, pandas, matplotlib, seaborn,sklearn
## I have used the Hourly dataset which does not include station names but weather conditions, reference: Hourly.ipynb
## the datasets was filtered again to show the same time period: 22pm - 5 am
## Steps:
   * data preparation and wrangling
   * feature engineering
   * creating some plots for verification purposes (in order to make sure that the data is representing the same findings as in the EDA)
   * creating relational plots like scatterplots in order to find out if there is a need to remove some of the features which were created
   * dropping some of the features
   * creating a heatmap with the features
   * creating a Multiple Linear Regression Model without scaling
   * creating a Multiple Linear Regression Modeil with scaling
   * creatinga Polynomial Regression
   * testing the results while removing different features (I only left the result for comparison)
   * doing a cross-validation for a more robust model (I was removing different features and comparing the results with the previous models)
   * visualization of the final models
# Part 3: EDA Findings:
 * You can view all the findings and company KPIs based on the findings here:
 https://www.canva.com/design/DAGA4AilbOA/DXX3dhBEBht1OCaxtCdWgw/edit?utm_content=DAGA4AilbOA&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
 * 100% of the lost bikes are classical bikes
 * We obseerve ride count increase and ride duration decrease per year
 * At 4 am we have a ride count increase during the workdays
 * The bike rides with electric bikes increased rapidly during 2023
 * At 3 am we have an increase of the ride duration for classic bikes 
