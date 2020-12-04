# rolling-averages-for-deaths-testing-hospitalizations-maryland-COVID-19
This repository shows how Python can be used to see the moving average trends for Covid-19 cases and deaths in Maryland. Over the past few months, the composition of what define's Maryland's experience with Covid-19 has changed. [From crowded hospitals to expanding testing](https://www.wbaltv.com/article/timeline-coronavirus-in-maryland/31394971), Maryland's padnemic response has had to adapt to ab unpredictable disease. 

Findings from my mini project are meant to be used in conjunction with my group members'. 

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





#### Pivot Tables
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.53.39%20PM.png)

![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.54.44%20PM.png)

- In Baltimore, employment for people with high-income parents is 78.9%, middle-income parents is 75.0%, and low-income parents is 69.7%.
- In Chicago, employment for people with high-income parents is 80.2%, middle-income parents is 76.8%, and low-income parents is 72.1%.

Chicago exhibits higher employment rates for each income group. The most notable differences are 1) The 2.4% higher employment for the low-income parent group 2) The smaller employment delta between those with high-income parents and low-income parents. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OydoEiz-Q99r4Tz1ehHyobecL2W-I3VW?usp=sharing)

#### Multiple Linear Regression
* Note that I did not determine the statistical significance of the coefficients. 

The goal was to determine whether or not one's parent-income group (high, medium, or low) would be a predictor of average employment for all parent-income groups. 
- Assuming all variables are significant: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OydoEiz-Q99r4Tz1ehHyobecL2W-I3VW?usp=sharing)
  - Chicago's intercept is more than double that of Baltimore's
  - Middle-income parents have relatively the same impact on employment in both cities
  - Being in the high or low-income parent group has double the impact on employment in Chicago than in Baltimore
  
Baltimore Linear Regression
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.56.15%20PM.png)

Chicago Linear Regression
![alt text](https://github.com/matthewprk/comparing-baltimore-and-chicago-employment-rates-based-on-parent-income-using-PYTHON/blob/main/Screen%20Shot%202020-11-22%20at%205.57.21%20PM.png)

## Comparing Python and Excel
There were three main differences between my experiences with Excel and Python:
- Data Prep: When data cleaning and aggregating, Colab required the importing of certain modules. In contrast, Excel has most of the functionality already built in. I personally found it easier to clean and aggregate data in Excel. This is because the dataset is always viewable in Excel, which makes it easier for me to appy filters, standardize columns, and merge worksheets. However, I see myself using Python for larger datasets for which Excel slows down. 
- Data Analysis: Python in Colab required downloading modules like pandas and numpy. Similar to Excel, which required downloading Data Analysis Tool Paks like Solver. Personally, I found it easier to create pivot tables, charts, and linear regressions in Excel. Likewise, I found the customizability of Excel's visuals to be more intuitive, especially with Pivot Charts. While I see myself using Excel for future analyses, Python can be valuable for larger datasets.
- Organization: When organizing my data analysis, I was pleased by how structured Colab is. The ability to create headers, leave comments, and create text cells makes it easier to follow the my analysis. Likewise, it was useful knowing where an error was in my code. In collaborative environments, I can see myself preferring to use Python because it is easier for others to follow the work or pinpoint errors. 

## Summary and Next Steps 
Parent income affects employment rates in both Baltimore and Chicago. Generally, average employment rate increases as parent income increases for both cities, though we cannot assert causation. Chicago's employment rate is higher than Baltimore's for each parent-income group. Baltimore's employment rate for people with low-income parents is >2% lower than Chicago's, which could be driving lower overall employment. This means that Chicago residents with high-income parents and low-income parents are more likely to be employed than their comaprable groups in Baltimore. Thus, it'd be interesting to explore why it's easier for both of these groups to be employed in Chicago. 

The next steps are to look at why parent income influences employment rates. 
- Person-specific factors: education, demographics, incarceration 
- City-specific factors: prevalent industries, available jobs, economic growth, policies

This is important to me, because addressing employment rates, especially amongst those with low-income parents, is critical to social mobility and thriving cities. Balitmore is a city where there is a strong [disconnect between one's skills and job opportunities](https://www.baltimoresun.com/opinion/op-ed/bs-ed-op-0115-baltimore-unemployment-20200115-urcqmi467vcqnlw4usgtonzwja-story.html). If we can determine what the root cause for the employment difference is, Baltimore can solve its lower employment issue. 
