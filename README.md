# Customer-Segmentation-using-K-Means-Clustering
Customer Segmentation using K-Means Clustering
This project uses the K-Means clustering algorithm to segment a customer dataset based on their annual income and spending score. The goal is to identify distinct customer groups, which can be useful for developing targeted marketing strategies.

Project Overview
The analysis follows a standard machine learning workflow:

Data Loading and Exploration: The project begins by loading a CSV file (Mall_Customers.csv) and examining its structure and summary statistics.

Feature Selection: We focus on two key features for clustering: Annual Income (k$) and Spending Score (1-100).

Optimal K Determination: The Elbow Method is used to find the best number of clusters (K) to use for the K-Means algorithm.

Model Training: The K-Means algorithm is applied with the optimal number of clusters to group the customers.

Visualization: The final clusters and their centroids are visualized on a scatter plot to provide a clear understanding of the customer segments.

Code Explanation
The provided Python script (untitled21.py) breaks down the process into clear, numbered steps.

Step 1: Import Libraries
This step imports the necessary Python libraries:

pandas for data manipulation.

matplotlib.pyplot for creating visualizations.

sklearn.cluster.KMeans for the K-Means clustering algorithm.

Step 2: Load the Dataset
The Mall_Customers.csv file is loaded into a pandas DataFrame. You should ensure this file is in the same directory as your script.

Step 3: Explore Dataset Features
This step prints essential information about the dataset, including data types, missing values, and descriptive statistics, to ensure the data is clean and ready for analysis.

Step 4: Select Features for Clustering
The script creates a new DataFrame X containing only the Annual Income (k$) and Spending Score (1-100) columns. These are the two variables used for clustering.

Step 5: Use Elbow Method to Find Optimal K
This is a critical step for K-Means. The code calculates the Within-Cluster Sum of Squares (WCSS) for a range of clusters (from 1 to 10) and plots the results. The "elbow" in the resulting graph indicates the optimal number of clusters, which in this case is determined to be 5.

Step 6: Apply K-Means with Optimal K
Based on the Elbow Method, the K-Means algorithm is run with n_clusters=5. The fit_predict() method trains the model and returns the cluster label (0 to 4) for each customer. A new Cluster column is then added to the original DataFrame to store these labels.

Step 7: Visualize the Clusters
The final step creates a scatter plot to visualize the results. Each cluster is plotted with a different color, and the centroids of the clusters are marked with large black 'X's. This visualization clearly shows the five distinct customer segments identified by the algorithm.

How to Use
Make sure you have the required libraries installed:

Bash

pip install pandas scikit-learn matplotlib
Place the Mall_Customers.csv file in the same directory as the Python script.

Run the script:

Bash

python untitled21.py
The script will print information about the dataset and display two plots: the Elbow Method graph and the final customer segmentation plot.
