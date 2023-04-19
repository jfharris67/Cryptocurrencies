# Cryptocurrencies

In this project, I worked on clustering cryptocurrencies to group them based on their features.

### Initial Imports
I imported necessary libraries for data manipulation, visualization, and clustering.

## Deliverable 1: Preprocessing the Data for PCA
### Data Loading and Cleaning
1. Loaded the crypto_data.csv dataset.
2. Kept all the cryptocurrencies that are being traded.
3. Removed the "IsTrading" column.
4. Removed rows with any null values.
5. Kept the rows where coins are mined (TotalCoinsMined > 0).
### Data Transformation
1. Created a new DataFrame that holds only the cryptocurrency names.
2. Dropped the 'CoinName' column as it's not going to be used in the clustering algorithm.
3. Used get_dummies() to create variables for text features (Algorithm and ProofType).
4. Standardized the data with StandardScaler.
## Deliverable 2: Reducing Data Dimensions Using PCA
1. Used PCA to reduce dimensions to three principal components.
2. Created a DataFrame with the three principal components.
## Deliverable 3: Clustering Cryptocurrencies Using K-Means
1. Finding the Best Value for k Using the Elbow Curve
2. Created an elbow curve to find the best value for K.
3. Initialized the K-Means model with the optimal K value.
4. Fitted the model with PCA data and made predictions.
### Creating the Clustered DataFrame
1. Created a new DataFrame including predicted clusters and cryptocurrency features.
2. Added a new column, "CoinName" to the DataFrame that holds the names of the cryptocurrencies.
3. Added a new column, "Class" to the DataFrame that holds the predictions.
## Deliverable 4: Visualizing Cryptocurrencies Results
Created a 3D scatter plot with the PCA data and the clusters, including hover data for the coin name and algorithm.
