# Time Series MTA Bridges and Tunnels
Albert Um - DS Cohort 06-22-20

# Project
For this project, my objective is to forecast NYC bridges and tunnels traffic (not congestion but number of cars). 

# Structure of Respository

-readme.md


# Business Case
1. Who would be interested in this?
2. What does the forecast look for different bridges?
3. 


## Data


The dataset can be found [here](https://data.ny.gov/Transportation/Hourly-Traffic-on-Metropolitan-Transportation-Auth/qzve-kjga). The data is collected by Metropolitan Transportation Authority (MTA) Bridges and Tunnels. 


Information about the data.
1. The data contains hourly counts of 10 unique bridges.
2. The hourly count per bridge is separated to EZ-Pass and Cash
3. The data ranges from 2010-2020


For more information about the dataset, please look to plaza_id.txt or [here](https://data.ny.gov/api/views/qzve-kjga/files3cc7ddd0-d7f2-4bf7-befd-2c0dcd0031fa?download=true&filename=MTA_HourlyTrafficBridgeTunnel_DataDictionary.pdf) for the original data dictionary.

## Preprocessing
For this project, I have done 
1. Use the sum count of EZ-Pass and Cash for each bridge.
2. Resample hourly data to daily by summing.
3. Use data collected from 2018 and on.
4. Join Triboro Bronx and Triboro Manhattan counts to 'Triboro'


### *Summing EZ-Pass/Cash and Hourly to Daily*
Since I am interested in the forecast of daily counts per bridge, it makes sense to add the ez-pass and cash counts and sum hourly instances by days.

### *Use data collected from 2018 and on*
On 2017, NYC finishes installing cash-less tolls. I decided to use the data from 2018 and on because pre-2017, the data was collected in a different way. The article of cashless tolling completion can be found [here](https://www.governor.ny.gov/news/governor-cuomo-announces-completion-cashless-tolling-all-mta-bridges-and-tunnels-three-months).

### *Join Triboro Bronx and Triboro Manhattan*
The Triboro Bridge consists of three bridges that connect Manhattan, Bronx, and Queens. For this project, I have decided to treat these three bridges as one.

# Exploratory Visualizations


### Month


### Day of Week


### 2020 - 2019 comparison


### 2020 events


### Train Test Split

Train-test split 
Training set:
2018-01-01:2020-08-22

Test set:
2020-08-23:2020-09-12
In order to evaluate the model, I split th

I used root mean squared error as the metric as it is more sensitive to robust errors than mean absolute error. 

# Modeling

SARIMAX
Prophet
LGBM

### Cross Bay/Henry Hudson

### Queens Midtown Tunnel

### Brooklyn Battery Tunnel

# Conclusion
Given that NYC stays in phase 4, I have showed forecasts for bridges for the rest of the year. 

# Further Steps
I would like to experiment with other models such as keras LSTM and Dilated CNN to see if model performs better. 
Forecasting weather data can be a preliminary step as it can help the accuracy of the forecast(specifically the Cross Bay and )
Including number of lanes available to the forecast can help manage urban developers when it is optimal to do maintenance work.

# Recommendations

