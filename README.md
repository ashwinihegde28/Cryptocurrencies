# Cryptocurrencies
Unsupervised Learning algorithm to discover unknown patterns

## Overview:

The purpose of this analysis was to use data from to provide a report and visualization of currently traded cryptocurrencies that can be grouped together to create a new classification system. This report would be used to help **Accountability Accounting** offer a new investment portfolio in the exciting world of cryptocurrency to its customers. 

Since the data does not have any known outcome, we needed to preprocess it to fit an unsupervised `Machine Learning` model that will enable us to run a clustering algorithm that will allow us to group the cryptocurrencies.

In this analysis we learned and applied:
* ** Differences between supervised and unsupervised learning. 
* **Data Preprocessing** (Selection, Transformation, Scaling) - the process of helping to prepare data for `Machine Learning` Algorithms.
* **Elbow Curve** - method to determine the best number of clusters needed for the algorithm to group the objects by.
* **Principal Component Analysis (`PCA`)** - statistical technique to speed up machine learning algorithms when the number of features is too high.
* **Clustering Algorithms (`KMeans`)** - the process of grouping similar objects/data points into clusters.
* **Visualization (`hvPlot`, `Plotly`)** - graphic libraries that allows us to create 2D and 3D graphs such as, scatter plots.

The code for the challenge can be found in [Module Challenge](https://github.com/ashwinihegde28/Cryptocurrencies/tree/main/ModuleChallenge)

## Results:
### Preprocessing the Data for PCA
- Initially the original dataset contained 1,252 records, in which only 1,144 cryptocurrencies were currently trading.
- All the rows that do not have coins being mined are removed.
- Only required columns are kept, dropping others.
- The final results identified 532 tradable cryptocurrencies which is displayed below. <br>
![Deliverable1](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/CleanCryptoDF.PNG)<br><br>

### Reducing Data Dimensions Using PCA
- Created a new DataFrame named pcs_df that includes the following columns, PC 1, PC 2, and PC 3, and uses the index of the crypto_df DataFrame as the index. Which is shown below.<br>
![pcs_df](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/Deliverable2.PNG)

### Clustering Crytocurrencies Using K-Means
- An elbow curve is created using hvPlot to find the best value for K. Here the value of K is 4 from the diagram.<br>
![Elbow Curve](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/ElbowCurve.PNG)<br><br>
- Predictions are made on the K clusters of the cryptocurrencies’ data
- A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class <br>
![Deliverable3](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/Deliverable3.PNG)<br><br>

### Visualizing Cryptocurrencies Results
- The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover <br>
![3D scatter plot](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/ScatterPlot.PNG)<br><br>
- Created a table with tradable cryptocurrencies using the hvplot.table() function. <br>
![HvpTable](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/HvpTable.PNG)<br><br>
- A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns.<br><br><br>
![PlotDf](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/plotDf.PNG)<br><br>
- A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point.<br>
![hvplot scatter plot](https://github.com/ashwinihegde28/Cryptocurrencies/blob/main/ModuleChallenge/images/Deliverable4.PNG)<br><br>


 


