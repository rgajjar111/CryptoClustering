# CryptoClustering

This repository contains code for performing clustering analysis on cryptocurrency data using K-Means and Principal Component Analysis (PCA). The analysis is conducted on both the original scaled data and the reduced PCA data.

## Overview
### Data Normalization:
The StandardScaler module from scikit-learn is used to normalize the data. A DataFrame is created with the scaled data, and the "coin_id" index from the original DataFrame is set as the index for the new DataFrame.

### Finding the Best Value for k (Original Scaled DataFrame): 
The elbow method is employed to determine the optimal value for k. A list is generated with k values ranging from 1 to 11, and inertia values are computed for each k. A line chart visualizes the elbow curve, helping identify the best k value.

### Clustering Cryptocurrencies with K-Means (Original Scaled Data): 
The K-means model is initialized with the best value for k. The model is fitted using the original scaled DataFrame, and predicted clusters are assigned to group the cryptocurrencies. A scatter plot is created using hvPlot to visualize the clusters in reduced dimensions.

### Optimizing Clusters with PCA (Original Scaled DataFrame): 
Principal Component Analysis is performed on the original scaled DataFrame to reduce features to three principal components. Explained variance is calculated, and a new DataFrame with PCA data is created.

### Finding the Best Value for k (PCA Data): 
Similar to the original data, the elbow method is applied to the PCA data to find the optimal value for k. A line chart visualizes the elbow curve for different k values.

### Clustering Cryptocurrencies with K-Means (PCA Data): 
The K-means model is initialized with the best value for k obtained from PCA data. The model is fitted using the PCA data, and predicted clusters are assigned. A scatter plot using hvPlot visualizes the clusters in a reduced feature space.
