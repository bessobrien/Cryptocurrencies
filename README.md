# Cryptocurrencies

## Overview

The purpose of this project is to do an analysis for a client, Accountability Account, a prominent investment bank. The company has asked for a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new ivestment.

Since there is no known output for what we are looking for, we have decided to use unsupervised learning and a clustering algorithms.

## Results

The first step was to preprocess the data for a PCA (Principal Component Analysis) algorithm.

This was done using Pandas. After going through the data, I modified by:

1. Removing all cryptocurrencies that are not being traded.
2. Drop the IsTrading column.
3. Remove rows that had at least one null value.
4. Remove rows that do not have coins being mined.
5. Drop the CoinName column.

Afterwards, I reduced the data dimensions to three principal components by using a Principal Component Analysis algorithm. I created a new DataFrame that had the components.

The next step was to cluster the cryptocurrencies using K-means algorithm. To do this:

1. Created an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame.
2. Run the K-means algorithm to predict the K clusters for the cryptocurrencies' data.


![elbow](https://github.com/bessobrien/Cryptocurrencies/blob/main/Resources/elbow.png)


Finally, I visualized the distict groups that correspond to the three pricipal components, and then created a table with all the currently tradable cryptocurrencies.

![scatter](https://github.com/bessobrien/Cryptocurrencies/blob/main/Resources/scatter.png)


## Summary

The purposed of unsupervised machine learning is to discover patterns within data when we have no known output. By using the PCA and K-means algorithm, we were able to group cryptocurrencies into 4 clusters which was the ideal number. This analysis will be a start for the company to begin investing in cryptocurrencies.
