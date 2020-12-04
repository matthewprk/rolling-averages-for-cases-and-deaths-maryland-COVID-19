# rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19

This repository shows how Python can be used to see the moving average trends for Covid-19 cases and deaths in Maryland. Over the past few months, the composition of what define's Maryland's experience with Covid-19 has changed. [From crowded hospitals to expanding testing](https://www.wbaltv.com/article/timeline-coronavirus-in-maryland/31394971), Maryland's padnemic response has had to adapt to ab unpredictable disease. 

Findings from my mini project are meant to be used in conjunction with group members. This analysis focuses on time-series data.

# Business Question

- How has the Covid-19 pandemic evolved in Maryland and where should policymakers target their response? 

## Data Analysis
### Data Sources
#### [Maryland.gov COVID Data](https://coronavirus.maryland.gov/datasets/md-covid-19-data-dashboard)
- [Deaths by Date](https://github.com/matthewprk/rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19/blob/main/MDC19_DeathsbyDate.csv) 
- [Hospitalizations by Date](https://github.com/matthewprk/rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19/blob/main/MDC19_HospitalizationsByDate.csv) 
- [Testing by Date](https://github.com/matthewprk/rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19/blob/main/MDC19_TestingbyDate.csv) 

### Data Question

- What are the weekly simple-moving averages for deaths, tests, and hospitalizations in Maryland and how do they differ for each variable?

### Data Answer

- Metric explored: Weekly Simple Moving Average 


![alt text](https://github.com/matthewprk/rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19/blob/main/SMA.png) 

#### Plotly Express

These graphs show the weekly simple moving averages for deaths, tests, and hospitalizations by date in Maryland.
  - Start Date: 3/26/2020
  - End Date: 12/01/2020

![alt text](https://github.com/matthewprk/rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19/blob/main/Screen%20Shot%202020-12-03%20at%2010.48.04%20PM.png) 

- From these graphs we can determine that:
  - The highest weekly moving average of deaths, 54.57, occurred on 4/30/2020.
  - The higest weekly moving average of tests, 42.3km occurred on 11/26/2020.
  - The highest weekly moving average of hospitalizations, 1673,occured on 5/10/2020. 

- Trends we observed:
  - SMA Hospitalizations and SMA Deaths appear to follow a similar story. Peaking in late April/early May, then decreasing to lows in October, then beginning to increase again. 
  - SMA Testing has consistently increased as capacity has expanded during the pandemic. 

To view methodology and calculations for rolling averages in Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10ZE6mmDmrSa-LYPKPn0hQOVz1uDfzyC-?usp=sharing) 

## Summary and Next Steps 
These findings pose some considerations for Maryland's Department of Health in how they can ensure an effective Covid response. The analysis shows that both weekly moving averages for hospitalizations and deaths are beginning to increase again. If deaths are related to hospitalizations, it's important for the DoH to implement responses that keep people out of hospitals in the first place (developing severe symptoms for which medical treatment is needed). Testing doesn't appear to reduce hospitalizations or deaths (based solely on the variables investigated). Thus, it doesn't appear to be a way to keep people from having to seek medical help. What the data does show is that from July to November, the rolling averages for deaths and hospitalizations were at their lows. This could indicate a reference point of the DoH to implement again (lockdowns, closed businesses, etc).

In our final project, we explore further characteristics of the disease in Maryland, predictors of deaths using linear regression, and where infections occur using clusters.


