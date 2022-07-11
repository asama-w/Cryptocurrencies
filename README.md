# Unsupervised Machine Learning: Cryptocurrencies

## Overview
### Purpose of the Analysis
Using unsupervised machine learning to analyze cryptocurrencies dataset and group the data in order to create a classification for the cryptocurrency investment report. The data grouping is carried out by using clustering algorithm, of which the clusters are determined by K-means algorithm.

### Resources
+ **Programming Language:** Python (Unsupervised Machine Learning)
+ **Libraries:** sklearn, KMeans, pandas, hvplot
+ **Software platform:** Jupyter Notebook
+ **Raw Dataset:** crypto_data.csv

### Methodology
The cryptocurrencies dataset will undergo 4 processes in order to determine the clusters and visualize the results:
1. Preprocessing the Data for PCA with Pandas (Deliverable 1)
2. Reducing Data Dimensions Using PCA (Principal Component Analysis) algorithm (Deliverable 2)
3. Clustering Cryptocurrencies Using K-means (Deliverable 3):
    + Using elbow curve to determine the best value for K.
    + Predict the K clusters for the Cryptocurrencies' data by running K-means algorithm.
4. Visualizing Cryptocurrencies Results (Deliverable 4)
    + 3D-scatter plot of the clusters
    + Tradable Cryptocurrencies Table
    + 2D-scatter plot of TotalCoinSupply and TotalCoinsMined columns with class distiction 

## Results
+ **Script:** [crypto_clustering.ipynb](https://github.com/asama-w/Cryptocurrencies/blob/main/crypto_clustering.ipynb)

### PCA (Principal Component Analysis)
Using PCA to reduce the dimensions of the data to three principal components and store them in `pcs_df` DataFrame as shown in the following image.

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/PCA.png width="30%" height="30%">

### Elbow Curve
Create the elbow curve to find the best value for K using the three principal components from `pcs_df`.

From the following image of the elbow curve, **the best K value is 4.**

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/Elbow_curve.png width="90%" height="90%">

### Cluster DataFrame with three principal components and predictions
The following image shows the `cluster_df` dataframe which includes columns of the three principal components and the class predictions.

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/clustered_df.png width="90%" height="90%">

### 3D-scatter plot
3D-scatter plot showing the three clusters from `clustered_df` DataFrame with detail's box when hover over each data point.

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/3D_scatter_plot.png width="90%" height="90%">

### Tradable Cryptocurrencies Table
Use `hvplot.table()` to create the Tradable Cryptocurrencies Table from `clustered_df` DataFrame.
<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/tradable_cryptocurrencies.png width="90%" height="90%">

### 2D-scatter plot
The following images show `plot_df` dataframe which contains the scaled "TotalCoinSupply" and "TotalCoinsMined" columns, and the scatter plot of the `plot_df`.

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/plot_df.png width="50%" height="50%">

<img src= https://github.com/asama-w/Cryptocurrencies/blob/main/Additional_images/2D_scatter_plot.png width="90%" height="90%">
