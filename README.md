# Predicting-Stock-Prices
Mini Project for SC1015 - Introduction to Data Science and Artificial Intelligence.

## About
The financial market is complex with stock prices moving seemingly randomly and without relation to one another. Our group aims to make use of artifical intelligence as well as knowledge from the course to predict trends in stock prices and make more informed choices.

## Team Members 
- Lee Han Ni
- Ho Wei Hao
- Liaw Jia Xuan Celest

## Problem Definition
To what extent can we use various economic variables to predict trends in future stock prices?

## Contents
### Presentation Slides
This set of slides serves as a brief overview of our entire project.

### Notebook 1: Data Extraction & Cleaning
This notebook serves to extract raw data from our two sources, the yahoofinancials python module and Alpha Vantage API, and prepare the data for data visualisation and machine learning. The yahoofinancials module provides monthly stock data where we are able to retrieve each stock's monthly closing price for the past 24 months. The Alpha Vantage API provides monthly economic indicators. The "change" and "change_class" variables have been added to aid the aims of machine learning and data analysis.

### Notebook 2: Data Exploration and Analysis
This notebook presents the insights we have gained from the dataset via visualisation. Three methods were used to find out how well the economic variables correlate with the change in prices: 
1. Time series  
2. Box Plots
3. Heat Map

### Notebook 3: Machine Learning - Decision Tree
The code in this notebook uses Classification Decision Tree learning from scikit learn to create a model that can predict stock prices based on our economic predictors. We used a decision tree with max depth 4 to train the train set before testing the accuracy in the test set. An accuracy score is then assigned to the model based on the percentage of correct predictions made.

### Notebook 4: Machine Learning - K Nearest Neighbours
The code in this notebook uses the K Nearest Neighbours Algorithm to predict the class of each stock's "change_class" variable, either up or down, based on a similarity measure. Through cross validation, a small portion from the training dataset is selected  to evaluate different possible values of K. The value of K which provides the highest accuracy score and lowest misclassification error is then used to create the model. An accuracy score is then assigned to the model based on the percentage of correfct predictions made. 

### Notebook 5: Machine Learning - ARIMA 
The code in this notebook uses the Auto Regressive Integrated Moving Average(ARIMA) model to forecast future price changes based on past price changes. The ARIMA model takes in 3 parameters corresponding to: number of lag observations to be used, number of differences needed for stationarity, and number of lagged forecast errors to be used. By varying these parameters we are able to determine the optimal values to use for each stock, before fitting the model. An accuracy score based on the mean absolute percentage error is then assigned to each stock's model, where we then take the average. 

## Conclusion
- ARIMA had the highest accuracy among all 3 models.
- While predictions are still not accurate 100% of the time, we can use these models as an indicator to observe trends.
- Stock price movement is still largely random, but using economic indicators that have some relation to stock prices as well as past price movements can help us make slightly more informed choices.

## Recommendations
1. Use both ARIMA and KNN models in tandem. 
2. Next, we can focus more on predicting the volatility of an asset instead of its price.
3. Also take into account the company’s financials to predict movements in future stock prices.
