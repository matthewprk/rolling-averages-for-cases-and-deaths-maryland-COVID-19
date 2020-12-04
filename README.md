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
Parent income affects employment rates in both Baltimore and Chicago. Generally, average employment rate increases as parent income increases for both cities, though we cannot assert causation. Chicago's employment rate is higher than Baltimore's for each parent-income group. Baltimore's employment rate for people with low-income parents is >2% lower than Chicago's, which could be driving lower overall employment. This means that Chicago residents with high-income parents and low-income parents are more likely to be employed than their comaprable groups in Baltimore. Thus, it'd be interesting to explore why it's easier for both of these groups to be employed in Chicago. 

The next steps are to look at why parent income influences employment rates. 
- Person-specific factors: education, demographics, incarceration 
- City-specific factors: prevalent industries, available jobs, economic growth, policies

This is important to me, because addressing employment rates, especially amongst those with low-income parents, is critical to social mobility and thriving cities. Balitmore is a city where there is a strong [disconnect between one's skills and job opportunities](https://www.baltimoresun.com/opinion/op-ed/bs-ed-op-0115-baltimore-unemployment-20200115-urcqmi467vcqnlw4usgtonzwja-story.html). If we can determine what the root cause for the employment difference is, Baltimore can solve its lower employment issue. 
