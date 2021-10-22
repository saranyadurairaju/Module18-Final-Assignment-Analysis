# Cryptocurrencies Analysis with Unsupervised Machine Learning

Unsupervised Learning is a machine learning technique in which the users do not need to supervise the model. Instead, it allows the model to work on its own to discover patterns and information that was previously undetected. It mainly deals with the unlabelled data. 

There are two types of unsupervised learning: transformations and clustering algorithms.

A cryptocurrency (or “crypto”) is a digital currency that can be used to buy goods and services, but uses an online ledger with strong cryptography to secure online transactions.

## Overview

In this project we are going to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data we will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output, we are going to use unsupervised learning. To group the cryptocurrencies, we have decided on a clustering algorithm and we will use data visualizations to share the findings.

Below are the list of Deliverables:

  * Deliverable 1: Preprocessing the Data for PCA
  * Deliverable 2: Reducing Data Dimensions Using PCA
  * Deliverable 3: Clustering Cryptocurrencies Using K-means
  * Deliverable 4: Visualizing Cryptocurrencies Results

## Analysis and Results

We will use jupyter notebook with python packages for our Analysis. First we will import the dependencies, define the columns, Load the data. Then we will follow different steps to create the final visualization. Below are the four deliverable details: 

## Deliverable 1: Preprocessing the Data for PCA

With our knowledge of Pandas, we’ll preprocess the dataset in order to perform PCA.

* All cryptocurrencies that are not being traded are removed
* IsTrading column is dropped
* All the rows that have at least one null value are removed
* All the rows that do not have coins being mined are removed
* The CoinName column is dropped
* A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame.

![image](https://user-images.githubusercontent.com/85472349/138504387-b18e1da2-155e-4217-90c0-cb20a3da4aa9.png)

* The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame X.

![image](https://user-images.githubusercontent.com/85472349/138504492-fc8fbe18-f8da-4aa6-a412-562f6b609a65.png)

* The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function.

![image](https://user-images.githubusercontent.com/85472349/138504708-7b549598-df39-4857-ba4e-acda024999de.png)


## Deliverable 2: Reducing Data Dimensions Using PCA

Using the knowledge of how to apply the Principal Component Analysis (PCA) algorithm, we’ll reduce the dimensions of the X DataFrame to three principal components and place these dimensions in a new DataFrame. So, the pcs_df DataFrame is created with three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame.

![image](https://user-images.githubusercontent.com/85472349/138506107-09364499-4eba-42c8-aa3d-ea9c3068dc46.png)


## Deliverable 3: Clustering Cryptocurrencies Using K-means

Using the knowledge of the K-means algorithm, we’ll create an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created in the above Deliverable. Then, we’ll run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

### An elbow curve using hvPlot to find the best value for K

![image](https://user-images.githubusercontent.com/85472349/138506621-7d443ea9-1e3a-4e37-adbe-e01fdaeb671e.png)

### Predictions on the K clusters of the cryptocurrencies’ data 

![image](https://user-images.githubusercontent.com/85472349/138506738-fd92ec5c-ca2c-4d6e-9daa-b3514877ccf3.png)

### A new DataFrame with the same index as the crypto_df DataFrame with columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.

![image](https://user-images.githubusercontent.com/85472349/138506824-d45786ce-8ae2-41d7-8e1e-c3e3d6a9724f.png)


## Deliverable 4: Visualizing Cryptocurrencies Results

Using the knowledge of creating scatter plots with Plotly Express and hvplot, we’ll visualize the distinct groups that correspond to the three principal components created in Deliverable 2, then we’ll create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

### 3D-Scatter with Clusters

![image](https://user-images.githubusercontent.com/85472349/138507255-de0669e5-bf03-455b-b362-fc6919f1f6d2.png)

### A table with tradable cryptocurrencies.

![image](https://user-images.githubusercontent.com/85472349/138507344-5bb5caef-bd59-4f63-ba7c-a33a43c8c12d.png)

### hvplot.scatter plot using TotalCoinsMined and TotalCoinSupply

![image](https://user-images.githubusercontent.com/85472349/138507548-3eaf9cff-0dad-487e-bcc5-9f7cfd0a1755.png)


## Summary

We have preprocessed the Data, and using PCA we reduced the Data Dimensions. Finally we Clustered the Cryptocurrencies Using K-means to bring the final Visualization.
So, the data visualizations can be shared with the board. Hurry!
