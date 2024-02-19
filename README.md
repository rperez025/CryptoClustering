# CryptoClustering
Module 19 - Unsupervised Learning

**BACKGROUND**

In this challenge, I’ll use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

**REQUIREMENTS**

_Prepare the Data_

1. Used the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
2. Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

_Find the Best Value for k Using the Original Scaled DataFrame_

1. Used the elbow method to find the best value for k using the following steps:
   - Created a list with the number of k values from 1 to 11.
   - Created an empty list to store the inertia values.
   - Created a for loop to compute the inertia with each possible value of k.
   - Created a dictionary with the data to plot the elbow curve.
   - Plotted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
   - Answered the following question in my notebook: What is the best value for k? The best value for K is 4. 

_Cluster Cryptocurrencies with K-means Using the Original Scaled Data_

1. Used the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
   - Initialized the K-means model with the best value for k.
   - Fitted the K-means model using the original scaled DataFrame.
   - Predicted the clusters to group the cryptocurrencies using the original scaled DataFrame.
   - Created a copy of the original data and add a new column with the predicted clusters.
   - Created a scatter plot using hvPlot as follows:
     * Set the x-axis as "PC1" and the y-axis as "PC2".
     * Colored the graph points with the labels found using K-means.
     * Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

_Optimize Clusters with Principal Component Analysis_

1. Using the original scaled DataFrame, performed a PCA and reduce the features to three principal components.
2. Retrieved the explained variance to determine how much information can be attributed to each principal component and then answered the following question in my notebook:
   * What is the total explained variance of the three principal components? Array([0.3719856, 0.34700813, 0.17603793]).
3. Created a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

_Find the Best Value for k Using the PCA Data_

1. Used the elbow method on the PCA data to find the best value for k using the following steps:
   - Created a list with the number of k-values from 1 to 11.
   - Created an empty list to store the inertia values.
   - Created a for loop to compute the inertia with each possible value of k.
   - Created a dictionary with the data to plot the Elbow curve.
   - Plotted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
   - Answered the following question in my notebook:
     * What is the best value for k when using the PCA data? The best value for K continues to be 4.
     * Does it differ from the best k value found using the original data? No, both values are the same.

_Cluster Cryptocurrencies with K-means Using the PCA Data_

1. Used the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
   - Initialized the K-means model with the best value for k.
   - Fitted the K-means model using the PCA data.
   - Predicted the clusters to group the cryptocurrencies using the PCA data.
   - Created a copy of the DataFrame with the PCA data and added a new column to store the predicted clusters.
   - Created a scatter plot using hvPlot as follows:
     * Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
     * Colored the graph points with the labels found using K-means.
     * Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
   - Answered the following question in my notebook:
     * What is the impact of using fewer features to cluster the data using K-Means? By using less features, you can obtain similar performance on the model since 4 clusters exist for both (i.e., clearly identified).

**RESOURCES AND REFERENCES**

During the challenge, I referenced the following to aid in my understanding and completion of the assignment:
1. Reperformed majority of the class activites by re-watching the class instruction with Dr. A.
2. Reviewed the following instructor videos from Dr. A:
   - [Module 19 Challenge Walkthrough - Unsupervised Learning with Cryptocurrencies](https://www.youtube.com/watch?v=LNzw3mIwx2A) I referenced my review of the class activities and the above code in the video for performing my assignment. Specifically, I reviewed and followed along in the video to gain an understanding of its organization and use. I then took that understanding and incorporated my knowledge and practice from the class activities to write my scripts in [Crypto_Clustering.ipynb](https://github.com/rperez025/CryptoClustering/blob/main/Crypto_Clustering.ipynb)https://github.com/rperez025/CryptoClustering/blob/main/Crypto_Clustering.ipynb.).
