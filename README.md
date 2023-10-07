# Cryptocurrency Clustering with K-Means

This repository contains code and instructions for clustering cryptocurrencies using K-Means, exploring the impact of feature reduction with Principal Component Analysis (PCA). The following sections provide a step-by-step guide to using this repository.

## Table of Contents

1. [Introduction](#introduction)
2. [Find the Best Value for k Using the Original Scaled DataFrame](#find-best-k-original)
3. [Cluster Cryptocurrencies with K-Means Using the Original Scaled Data](#cluster-original-scaled)
4. [Optimize Clusters with Principal Component Analysis](#optimize-pca)
5. [Find the Best Value for k Using the PCA Data](#find-best-k-pca)
6. [Cluster Cryptocurrencies with K-Means Using the PCA Data](#cluster-pca)
7. [Impact of Using Fewer Features with PCA](#impact-pca)

## Introduction

In this project, we'll explore how to cluster cryptocurrencies using K-Means and assess the impact of feature reduction through Principal Component Analysis (PCA). We aim to find the optimal number of clusters (k) and visualize the clustering results. Below are the detailed steps for this process.

## Find the Best Value for k Using the Original Scaled DataFrame <a name="find-best-k-original"></a>

1. Create a list with the number of k values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Create a for loop to compute the inertia with each possible value of k.
4. Create a dictionary with the data to plot the elbow curve.
5. Plot a line chart with all the inertia values computed with different values of k to visually identify the optimal value for k.
6. Answer the following question in your notebook: What is the best value for k?

## Cluster Cryptocurrencies with K-Means Using the Original Scaled Data <a name="cluster-original-scaled"></a>

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the original scaled DataFrame.
3. Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
4. Create a copy of the original data and add a new column with the predicted clusters.
5. Create a scatter plot using hvPlot as follows:
   - Set the x-axis as "PC1" and the y-axis as "PC2".
   - Color the graph points with the labels found using K-means.
   - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Optimize Clusters with Principal Component Analysis (PCA) <a name="optimize-pca"></a>

1. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
2. Retrieve the explained variance to determine how much information can be attributed to each principal component and answer the following question in your notebook: What is the total explained variance of the three principal components?
3. Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the PCA Data <a name="find-best-k-pca"></a>

1. Create a list with the number of k-values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Create a for loop to compute the inertia with each possible value of k.
4. Create a dictionary with the data to plot the Elbow curve.
5. Plot a line chart with all the inertia values computed with different values of k to visually identify the optimal value for k.
6. Answer the following question in your notebook: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

## Cluster Cryptocurrencies with K-Means Using the PCA Data <a name="cluster-pca"></a>

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the PCA data.
3. Predict the clusters to group the cryptocurrencies using the PCA data.
4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
5. Create a scatter plot using hvPlot as follows:
   - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
   - Color the graph points with the labels found using K-means.
   - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Impact of Using Fewer Features with PCA <a name="impact-pca"></a>

Answer the following question: What is the impact of using fewer features to cluster the data using K-Means?

Feel free to explore this repository, run the code in your environment, and document your findings in the provided notebook. Enjoy your cryptocurrency clustering project!
