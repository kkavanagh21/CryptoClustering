# CryptoClustering

CryptoClustering

Overview

CryptoClustering uses K-means clustering and Principal Component Analysis (PCA) to classify cryptocurrencies based on price changes over various timeframes: 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year.

Project Structure

crypto_market_data.csv: Cryptocurrency market data.
Crypto_Clustering.ipynb: Jupyter notebook with the project code.
README.md: This document.
Requirements

Python 3.x
Pandas
Scikit-learn
Matplotlib
HvPlot
Install the required libraries using:

bash
copy code:
pip install pandas scikit-learn matplotlib hvplot


Instructions

1. Load and Prepare Data
Load crypto_market_data.csv into a Pandas DataFrame.
Normalize the data using StandardScaler.
Create a DataFrame with scaled data, using coin_id as the index.
2. Determine Optimal Clusters with K-means
Use the Elbow method to find the best k.
Plot inertia values for different k values to find the "elbow point".
Select the optimal k based on the plot.
3. Cluster Cryptocurrencies
Initialize and fit the K-means model with the best k.
Predict clusters for the scaled data.
Visualize clusters with a scatter plot.
4. Optimize Clusters with PCA
Apply PCA to reduce features to three principal components.
Determine the explained variance for each component.
Use the Elbow method on the PCA data to find the best k.
Cluster the PCA data and visualize with a scatter plot.
5. Determine Feature Influence
Analyze PCA components to understand the influence of each feature.
Identify features with the strongest positive and negative influences.

Analysis Results

Elbow Method
The optimal number of clusters (k) was determined by inspecting the Elbow plot for both the original scaled data and the PCA data.

Cluster Visualization

Scatter plots visualize the clustering of cryptocurrencies based on:
24-hour and 7-day price changes using original scaled data.
Principal components (PC1 and PC2) using PCA data.

PCA Feature Influence
PC1: 1y (positive), 24h (negative)
PC2: 30d (positive), 1y (negative)
PC3: 7d (positive), 60d (negative)



Completed by Kathryn Kavanagh
katiekavanagh21@gmail.com
