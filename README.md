# Data-science-in-finance-time-series-predictability
## Goal
This project is to use the daily returns of the 10 industry portfolios to run regression models and build a portfolio out of it.
Throughout the analysis, I will focus on the Jan 1st, 2000 to Dec 31st, 2019 period.
## Questions
I constructed the portfolio step by step by answering below questions:

1. For each of the industries, estimate a regression relating its daily returns to lagged returns of all other industries. Which industry appears to be most influenced by the lag of other industries?

2. Use the estimated regression coefficients to form daily return predictions for each of these industries.

3. Use the daily predictions in (2) to form a portfolio that attempts to trade on these predictions. What is the performance of this portfolio and how does it compare to the market. 
## Methodology
There are a lot of options for the strategy, here, I pick the top 3 industries and build an equal-weighted portfolio.
I use sharpe ratio as a measurement of performance, which is Mean/SD.

I use two models to build the portfolio:
### A simple OLS regression model

![Strat_v s_Market](https://user-images.githubusercontent.com/102770592/223020283-6d8a766b-b36a-4053-b90e-d50304d21b54.png)

The sharpe ratio of this portfolio is 1.7128 , much higher than that of the market,which is only 0.3316
While the simple OLS model has the problem of using future data to predict, which leads to overfitting. So .we need to use Rolling out of sample to fix this problem

### OLS Rolling out of sample
rolling window: 40 days
The sharpe ratio of this portfolio is 0.6086, much higher than that of the market,which is only 0.3363.
While the sharpe ratio of the portfolio calculated based on rolling basis is way less than that of previous result in (1).
rolling window: 80 days
rolling window: 20 days

The data source:
https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
