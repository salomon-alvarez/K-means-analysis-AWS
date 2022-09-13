# K-means on Amazon Web Services 

## Background

You are a Senior Manager at the Advisory Services team on a Big Four firm, one of your most important clients, a prominent investment bank, is interested in offering a new cryptocurrencies investment portfolio for its customers, however, they are lost in the immense universe of cryptocurrencies, they ask you to present a report of what cryptocurrencies are on the trading market and how cryptocurrencies could be grouped towards creating a classification for developing this new investment product.
In this homework assignment, you have the opportunity to put in action unsupervised learning and Amazon SageMaker to cluster cryptocurrencies and create some plots to present your results.

You are asked to accomplish the following main tasks:


Data Preprocessing: Prepare data for dimension reduction with PCA and clustering using K-Means.


Reducing Data Dimensions Using PCA: Reduce data dimension using the PCA algorithm from sklearn.


Clustering Cryptocurrencies Using K-Means: Predict clusters using the cryptocurrencies data using the KMeans algorithm from sklearn.


Visualizing Results: Create some plots and data tables to present your results.


Deploy your notebook to Amazon SageMaker.

## Instructions

### Data Preprocessing

In this section, you have to load the information about cryptocurrencies from the provided CSV file and perform some data preprocessing tasks. The data was retrieved from  CryptoCompare using this endpoint: https://min-api.cryptocompare.com/data/all/coinlist.


Create dummies variables for all the text features, store the resulting data on a DataFrame.


Use the StandardScaler from sklearn to standardize all the data of the DataFrame.


### Reducing Data Dimensions Using PCA

Use the PCA algorithm from sklearn to reduce the dimensions of the DataFrame down to three principal components.
Once you have reduced the data dimensions, create a DataFrame named pcs_df using as columns names "PC 1", "PC 2" and "PC 3";  use the crypto_df.index as the index for this new DataFrame.

### Clustering Cryptocurrencies Using K-Means

In this section, you will use the KMeans algorithm from sklearn to cluster the cryptocurrencies using the PCA data.

Perform the following tasks:


Create an Elbow Curve to find the best value for k, use the pcs_df DataFrame.


Once you define the best value for k, run the Kmeans algorithm to predict the k clusters for the cryptocurrencies data. Use the pcs_df to run the KMeans algorithm.


Create a new DataFrame named clustered_df, that includes the following columns "Algorithm", "ProofType", "TotalCoinsMined", "TotalCoinSupply", "PC 1", "PC 2", "PC 3", "CoinName", "Class".

### Visualizing Results

In this section, you will create some data visualization to present the final results. Perform the following tasks:


Create a 3D-Scatter using Plotly Express to plot the clusters using the clustered_df DataFrame. 


Create a data table with all the current tradable cryptocurrencies. 


Create a scatter plot to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins.
