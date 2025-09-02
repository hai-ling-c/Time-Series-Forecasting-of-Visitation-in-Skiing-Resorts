# Time-Series-Forecasting-of-Visitation-in-Skiing-Resorts
This repository is part of the work completed during InterUniversity Datathon 2025 organised by student societies from 4 leading universities in Australia. It aims to provide forecasts on the number of visitor days in 2026 for 9 different skiiing resorts in Australia using Exponential Smoothing model, ARIMA model and RNN model.

## Table of Contents
- [Visitation data information](https://github.com/hai-ling-c/Time-Series-Forecasting-of-Visitation-in-Skiing-Resorts/edit/main/README.md#visitation-data-information)
- [Python packages requirements](https://github.com/hai-ling-c/Time-Series-Forecasting-of-Visitation-in-Skiing-Resorts/edit/main/README.md#python-package-requirements)
- [Overview](https://github.com/hai-ling-c/Time-Series-Forecasting-of-Visitation-in-Skiing-Resorts/edit/main/README.md#overview)

## Visitation data information
Visitation Data is measured in visitor days. A "visitor day" is a unit of measure used to quantify the use of a site or facility by visitors, typically representing 12 visitor hours. It can refer to a single person spending 12 hours or multiple people contributing to the 12-hour total. This term is often used by state and federal agencies to track and analyse visitor activity, particularly in recreation areas.

Victorian visitor day data has been obtained from Alpine Resorts Victoria. 

NSW resort visitation data has been estimated using annual visitor day estimates.	

The data has been provided on a week-by-week basis based on the ski season. The exact dates of the ski season is available below:

| Ski season  | Dates |
| ------------- | ------------- |
| Week 1  | 9-Jun  |
| Week 2  | 16-Jun   
| Week 3	| 23-Jun |
| Week 4 | 30-Jun |
| Week 5 | 7-Jul |
| Week 6 | 14-Jul |
Week 7	| 21-Jul
Week 8	| 28-Jul
Week 9	| 4-Aug
Week 10	| 11-Aug
Week 11	| 18-Aug
Week 12	| 25-Aug
Week 13	| 1-Sep
Week 14	| 8-Sep
Week 15	| 15-Sep

## Python package requirements
The project requires packages which are sepcified in the requirement.txt and can be installed through:
```
pip install -r requirements.txt
```

## Overview
### 1. Import libraries
### 2. Import and clean data
### 3. Time series modelling for visitation data (perfomance and possible improvements discussed)
1. Convert data to time series
2. Forecast using exponential smoothing 
3. Forecast using AutoARIMA
4. Forecast using RNN-LSTM
### 4. Model evaluation and backtesting
### 5. Plots comparing Exponential Smoothing and AutoARIMA forecasting results
### 6. Calculating visitation index
Formula to calculate the index
$$I_{\text{visitation}} = \exp\left(-0.159 * \text{No. of Visitor days}\right)$$

Note that:
- The coefficient of '-0.159' comes from the result in https://www.tandfonline.com/doi/full/10.1080/10548408.2020.1763229#d1e897. 
- The exponential function is used to restrict the index to take values between 0 and 1.
- The formula has not been validated and the numbers were only used to rank resorts.


