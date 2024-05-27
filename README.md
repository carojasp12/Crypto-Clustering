# Crypto-Clustering
![image](https://github.com/carojasp12/Crypto-Clustering/assets/152667250/2be26727-8ee7-4df7-ab67-ad5991338fa2)

## Use python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

### Prepare the Data
- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

### Find the Best Value for k Using the Original Scaled DataFrame
- Create a list with the number of k values from 1 to 11.
- Create an empty list to store the inertia values.
- Create a for loop to compute the inertia with each possible value of k.
- Create a dictionary with the data to plot the elbow curve.
- Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![Screenshot 2024-05-27 003524](https://github.com/carojasp12/Crypto-Clustering/assets/152667250/a9a3f306-377d-4625-87c7-8a3955b8f39f)

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data
- Initialize the K-means model with the best value for k.
- Fit the K-means model using the original scaled DataFrame.
- Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
- Create a copy of the original data and add a new column with the predicted clusters.
- Create a scatter plot using hvPlot
  
![Screenshot 2024-05-27 003505](https://github.com/carojasp12/Crypto-Clustering/assets/152667250/f78591ce-2ef9-4026-b3e7-e7f2b68862a3)

### Optimize Clusters with Principal Component Analysis
- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
- Retrieve the explained variance to determine how much information can be attributed to each principal component.
- Create a new DataFrame with the PCA data.

### Find the Best Value for k Using the PCA Data
- Create a list with the number of k values from 1 to 11.
- Create an empty list to store the inertia values.
- Create a for loop to compute the inertia with each possible value of k.
- Create a dictionary with the data to plot the elbow curve.
- Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![Screenshot 2024-05-27 003321](https://github.com/carojasp12/Crypto-Clustering/assets/152667250/13ba0c25-5bf3-43b4-b780-700ab284f342)

### Cluster Cryptocurrencies with K-means Using the PCA Data
- Initialize the K-means model with the best value for k.
- Fit the K-means model using the PCA data.
- Predict the clusters to group the cryptocurrencies using the PCA data.
- Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
- Create a scatter plot using hvPlot

![Screenshot 2024-05-27 003234](https://github.com/carojasp12/Crypto-Clustering/assets/152667250/1940ddcb-69e3-4412-9b6c-fe1f2e0f4767)
