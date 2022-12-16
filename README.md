# Crypto-Trading-Using-Hurst-Exponent
In this notebook, we will create a strategy using the Hurst exponent and the RSI.

# 1. Import the libraries and data 
First, we will import the necessary libraries and then, fetch the minute data for Ethereum data from csv files using the pandas 'read_csv' function.

# 2. Convert the Unix timestamp to datetime
Convert the Unix epoch time to normal datetime format and set it as index

# 3. Compute the hurst value for the data
A Hurst value that is greater than 1 does not have much theoretical interpretation or physical significance. The most likely way the value would be greater than 1, is if there exists a Stochastic trend in the input series. These are trends that increase and decrease inconsistently.

Such scenarios may arise due to following reasons:

1. If the input data series is non - stationary: A non - stationary time series is one whose properties change depending on the time at which the series is observed. Thus, time series with trends, or with seasonality, are not stationary.

2. Unsuccessful detrending: Detrending is removing a trend from a time series. A trend usually refers to a change in the mean over time. When you detrend data, you remove an aspect from the data that you think is causing some kind of distortion.

# 4. Compute the rolling hurst values
Compute the rolling hurst values for with a lookback period of 240 minutes

# 5. Generate the persitence signals
Compute the signals to indicate the persistent nature of the market

# 6. Compute the RSI

# 7. Compute the market return

# 8. Compute the strategy returns
We use RSI here to gauge the overbought/oversold condition of the market.

We buy when

1. RSI is more than 75 and Persistence signal is 1
2. RSI is less than 25 and Persistence signal is -1

We sell when

1. RSI is more than 75 and Persistence signal is -1
2. RSI is less than 25 and Persistence signal is 1

# 9. Compute the total slipapge cost

# 10. Plot the cumulative returns of the strategy
Compute the cumulative strategy return and plot it

# 11. Compute the net profit after slippage
