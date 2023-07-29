# Electricity-Price-Forecasting

## Data
**[Hourly energy demand generation and weather | ENTSOE & REE](https://www.kaggle.com/datasets/nicholasjhana/energy-consumption-generation-prices-and-weather)**</br>
The dataset includes hourly data on Energy Generation, Consumption, Pricing, and Weather from 2015 to 2018.


| Feature-type | Column |
| :----------  | :-----------  |
| Date         | time          |
| Energy       | generation biomass, generation fossil gas, generation nuclear, etc.|
| Weather      | temp, pressure, humidity, wind_speed, weather_description, etc.|
| Forecast     | total load forecast, price day ahead, etc.|
| Target       | price_actual, total load actual |


## Overview
• The project focuses on forecasting electrical prices in the energy market for Spain.</br>
• The goal is to predict electrical prices based on generation, consumption, and weather data.</br>
• The project also explores the influence of different features on electrical prices.</br>
• Time-series models, boosting models, and an LSTM model are implemented and evaluated to determine the suitable model and features.


## Data Preprocessing
• Drop columns with all null values, zero values, unientifiable icon info.</br>
• Convert specific column to appropriate datatypes.</br>
• Merge the Energy and Weather datasets on time==dt_iso, handle the duplicates and save the data as csv.


## EDA
► We can observe a pattern where can see an increase, then decrease, then increase in price actual year wise over time.</br>
- ![image](https://github.com/sohamthirty/Electricity-Price-Forecasting/assets/56295513/c7c4f39b-6d8c-4879-9c62-fa1a2d2519da)
- 
► We can see a lot of variation in price actual over days in a month.</br>
- ![image](https://github.com/sohamthirty/Electricity-Price-Forecasting/assets/56295513/8e2957cf-c603-41ea-b4cc-9a3be9c5a027)
- 
► 2016 has lower price than other years.</br>
► Months of Feb to Jun have lower values for price.</br>
- ![image](https://github.com/sohamthirty/Electricity-Price-Forecasting/assets/56295513/b075180d-a7dd-4702-98c5-d696acc4d0d5)
- 
► Sunday has the lowest load value.</br>
► Temp generally increases for summer months.</br>
- ![image](https://github.com/sohamthirty/Electricity-Price-Forecasting/assets/56295513/6ff7beca-9967-424f-bd7b-f17175656b14)

► wrt price as target,</br>
strong +ve correlation for price day ahead, total load actual, total load forecast, generation fossil gas, generation fossil hard coal.</br>
strong -ve correlation for generation hydro pumped storage consumption, generation wind offshore, forecast wind offshore day ahaead.</br>
- ![image](https://github.com/sohamthirty/Electricity-Price-Forecasting/assets/56295513/96c9f2d2-94d7-4d48-95df-3a4bd4136062)


## Modelling
### Traditional ML models:

| Model | RMSE loss |
| :----------  | :-----------  |
| Linear             | 9.78|
| Ridge              | 9.78|
| Lasso              | 9.78|
| Descision Tree     | 1.20|
| Random Forest      | 0.73|


## References
**[1]** Rolnick, D., Donti, P. L., Kaack, L. H., Kochanski, K., Lacoste, A., Sankaran, K., Ross, A. S., Milojevic-Dupont, N., Jaques, N., Waldman-Brown, A., Luccioni, A., Maharaj, T., Sherwin, E. D., Mukkavilli, S. K., Kording, K. P., Gomes, C., Ng, A. Y., Hassabis, D., Platt, J. C., … Bengio, Y. (2019, November 5). Tackling Climate Change with Machine Learning. arXiv.org. https://arxiv.org/abs/1906.05433 
