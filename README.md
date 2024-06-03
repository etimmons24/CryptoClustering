# Cryptocurrency Price Fluctuations 

## Description
This notebook is an illustration of cryptocurrencies and their price fluctuations across various timeframes using the K-means algorithm and principal component analysis (PCA).  The price changes are tracked over intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days and 1 year.  Data was provided by Columbia University as a .csv.  

## Analysis

### Scatter Plot of Clusters with K-Means Using Original Scaled Data
![image](https://github.com/etimmons24/CryptoClustering/assets/163076822/33466dc6-7a5e-4f5d-af54-c8263567850a)

The model predicted 4 clusters of cryptocurrencies using the 7 day percentage change and the 24 hour percentage change.  The variation in percent change was understandably more in the 7 day period than in the 24 hour period.  There was one cryptocurrency that had its price greatly decreased in the 24 hour period.  It could be from some event that negatively impacted that particular crypto's price.  It appears to be a bit of an outlier.

### Scatter Plot After PCA Optimization
![image](https://github.com/etimmons24/CryptoClustering/assets/163076822/3d6f70e3-0093-492d-802c-0d72b6d2172c)

The model was optimized for 4 clusters, similar to the above.  There is not much variation for PCA1.  For PCA2, the data points are variable. 

## Conclusions
Using the weights of each feature on each principal componet revealed the following results:

* PCA1: price_change_percentage_200d and price_change_percentage_1y have the strongest positive influence, while price_change_percentage_24h has the strongest negative influence.

* PCA2: price_change_percentage_14d and price_change_percentage_30d have the strongest positive influence, while price_change_percentage_1y has the strongest negative influence.

* PCA3: price_change_percentage_7d has the strongest positive influence, while price_change_percentage_60d and price_change_percentage_24h has the strongest negative impact.
