# Time Series Analysis on Iran Temperature

## Requirements

* Python 3.5 or higher
* Numpy
* Pandas
* Matplotlib
* Statsmodels

## Dataset

Kaggle [Dataset](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data)

## Exploratory Data Analysis

First we use pandas to read the CSV file. After that we perform Data Cleaning such as removing unwanted columns, identifying and filling the missing values.

##  Checking Time Series Data Stationarity

This is achieved using Augmented Dickey-Fuller test which assists finding out the stationary properties in the Time series data.

The stationarity check is carried out using the plot and p-value is tested.

![Stationary_Check](https://github.com/meysamfozi/Time-Series-Analysis-on-Iran-Temperature/blob/master/rolling_mean.png)

## Modelling and Forecasting Temperature

I used ARIMA model which stands for "Auto-Regressive Integrated Moving Average".

In this case as the data is stationary therefore only AR and MA have been taken into account.

Then AIC is calculated and then I found values of p and q having lowest AIC where the p represents the number of Auto-Regressive (AR) terms and q represents the number of Moving Average (MA) terms.

Finally the results are predicted. Here is the example of results. 


| Year  | Temperature Forecasting (Deg C) |
| :---: | :---: |
|2023-01-01 |  6.379692 |
|2023-02-01 |  7.642691 |
|2023-03-01 | 11.786761 |
|2023-04-01 | 17.700356 |
|2023-05-01 | 23.797296 |
|2023-06-01 | 28.442224 |
|2023-07-01 | 30.389251 |
|2023-08-01 | 29.116132 |
|2023-09-01 | 24.964353 |
|2023-10-01 | 19.047527 |
|2023-11-01 | 12.952701 |
|2023-12-01 |  8.314664 |

