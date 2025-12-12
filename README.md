# **Predicting ATCEMS Ambulance Arrival Times**

Final Project Repository for I 320D: Applied Machine Learning

Gummy Bears: Ruhama Kabir, Katherine Mundey, Krishna Pillai, Aurelia Tan

## **Description**
In New York City, the average ambulance response time for life-threatening emergencies increased from 9 minutes and 34 seconds in 2021 to 11 minutes and 21 seconds in 2025, representing a nearly 20% rise in response time over four years. These growing delays are occurring as emergency call volumes continue to rise while the city faces chronic staffing shortages, high employee attrition, and longstanding concerns about compensation and working conditions within FDNY Emergency Medical Services (EMS). 

To address this critical public safety challenge, this project aims to develop a machine learning–based system that predicts the arrival time of New York City EMS units following a 9-1-1 call. By analyzing historical EMS service data, our goal is to identify patterns, forecast delays, and provide insights that can support faster emergency response, better resource allocation, and improved health outcomes. 

## **Repository Description**

### 1. **era5_weather_data**

*This folder contains all data files and scripts related to the ERA5 Weather Dataset.*

--> `ERA5_2023_weather_data.grib` - The raw GRIB data file downloaded from the ECMWF, Copernicus Climate Change Service data platform. Contains ERA5 weather and climate data from 1 Jan 2023 to 31 Dec 2023.

--> `ERA5_2024_weather_data.grib` - The raw GRIB data file downloaded from the ECMWF, Copernicus Climate Change Service data platform. Contains ERA5 weather and climate data from 1 Jan 2024 to 31 Dec 2024.

--> `era5_2023_2024_weather_data.csv` - The cleaned CSV data file of combined 2023 and 2024 ERA5 weather data. This is the data file used to train our models. 

--> `extract_era5_data.ipynb` - A Python script for transforming the raw GRIB data files into a clean, usable CSV for model development. 

### 2. **models**

*This folder contains the Python scripts for creating our machine learning models.*

--> `Linear_Regression_Model.ipynb` - Contains the linear regression model and its variants. Uses the NYC EMS dataset.

--> `xgboost_model_development.ipynb` - Contains the gradient boosting regression model. Uses the NYC EMS dataset and the ERA5 Weather dataset.

### 3. **nyc_ems_data**

*This folder contains all data scripts and files related to the NYC EMS Incident Dispatch Dataset.*

--> `NYC_EMS_incident_dispatch_data_description.xlsx` - Defines the variables in the NYC EMS dataset. 

--> `extract_ems_data.ipynb` - A Python script for extracting the raw NYC EMS data (JSON) from 1 Jan 2023 to 31 Dec 2024 via the New York City Open Data Portal and Socrata API. Cleans and transforms the data into a downloadable CSV.

--> `nyc_ems_2023_2024_data.csv` - The cleaned CSV data file of the NYC EMS data. This is the data file used to train our models.
