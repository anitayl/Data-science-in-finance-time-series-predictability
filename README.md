# Data-science-in-finance-time-series-predictability
This project is to use the daily returns of the 10 industry portfolios to run a simple OLS regression model and build a portfolio out of it.
Throughout the analysis, I will focus on the Jan 1st, 2000 to Dec 31st, 2019 period.
I constructed the portfolio step by step by answering below questions:

1. For each of the industries, estimate a regression relating its daily returns to lagged returns of all other industries. Which industry appears to be most influenced by the lag of other industries?

2. Use the estimated regression coefficients to form daily return predictions for each of these industries.

3. Use the daily predictions in (2) to form a portfolio that attempts to trade on these predictions. What is the performance of this portfolio and how does it compare to the market. 

There are a lot of options for the strategy, here, I pick the top 3 industries and build an equal-weighted portfolio.

I use sharpe ratio as a measurement of performance, which is Mean/SD.
For this one, I only run a simple OLS regression model, which could lead to problems.

The data source:
https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
