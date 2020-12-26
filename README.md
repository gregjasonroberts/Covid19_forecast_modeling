
## Covid model comparison and forecasting death predictions
### Overview

* Model comparison looks at various time series to forecast future deaths.  
* While confirmed case levels have received mixed coverage, the number of deaths have served as a stark reminder of the virus severity and thus a more meaningful indicator of our social trajectory, if not economic one.
* Read in latest US Covid-19 confirmed cases and deaths from the following github repo:  COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University
* Optmized time series forecasting and compared US death prediction models including ARIMA, SARIMAX, Prophet, XGBOOST and Neural Networks(NN)

### Code and Resources Used
Python Version: 3.7
Environment: Google Colab
Packages: pandas, numpy, statsmodels, sklearn, matplotlib, keras
**Covid Modeling Comps code along** Compare time series predictions of COVID-19 deaths(https://www.coursera.org/projects/compare-time-series-predictions-of-covid19-deaths)
**Covid Case Fatality Ratio article** Delphi Research Group and the COVID tracking and forecasting (https://htmlpreview.github.io/?https://github.com/cmu-delphi/covidcast-modeling/blob/master/cfr_analysis/cfr_analysis.html)

### Data Cleaning
After reading in the data, it was necessary to transform the data to prepare it for modeling it in the formats required by the time series models.
* The dates columns were transposed and placed in a separate variable to later get added to a new dataframe
* The original dataset values are cumulative and in order to create a time series of incremental changes, the new dataset was differenced.
* The early dataset was quite sparse so for all models the time period was standardized to analyze from May through late December 2020.

### EDA
I looked at the case fataltity ratio and lagged correlations to understand the relationships that will drive the best predictions of future deaths.  Below are a few highlights:
![alt text](
