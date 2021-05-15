## Portfolio optimisation using *PyPortfolioOpt*
**This is not an investment advise | For educational purposes only** <br/>
<br>

## Overview
We create a optimised portfolio of stocks present in various NSE indices for any desired amount.\
Documentation - https://pyportfolioopt.readthedocs.io/en/latest/UserGuide.html 

## Procedure
1. Get historical data using *historical_data.ipynb*
    * First we get a dictionary of ticker symbol and company name for all the listed companies in NSE using *nsetool* library
    * Then we get historical data for the past 5 years from yahoo finance for all the tickers and save them in a text file for further processing.
3. Create master dataset using *data_preparation.ipynb*
    * This creates a master dataset with all the stocks as columns and date as index
    * You can chooose criteria according to your prefrence
    * I have choosen the data for 3MINIDA as my base data as it had all the datapoints for my time period of interest(for past 5 years)
    * This only selects tickers with all data points with the time frame of interest.
5. Optimize portfolio for desired amount using *portfolio_optimisation.ipynb*
    * Firstly, get index constituents for indices of interest from NSE 
    * Give the amount for which portfolio is to be optimised
    * Loop over all the indices to get the stock distribution for each index(refer sample_output.txt)
