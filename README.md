Task 8: K-Means Clustering for Customer Segmentation
Objective

The primary objective of this project is to perform unsupervised learning using the K-Means clustering algorithm. By analyzing customer data from a mall, we aim to identify distinct customer groups or segments based on their annual income and spending score. This type of segmentation is valuable for targeted marketing and business strategy.

About the Dataset

This project uses the Mall Customers dataset.
Source: Mall_Customers.csv
Features Used for Clustering:
Annual Income (k$): The annual income of the customer in thousands of dollars.
Spending Score (1-100): A score assigned by the mall based on customer behavior and spending habits.
Goal: To group customers into a small number of segments without any predefined labels, allowing us to discover natural patterns in the data.

Project Pipeline

The project follows a comprehensive unsupervised learning workflow:
Data Loading and Preparation:
The Mall_Customers.csv dataset is loaded using Pandas.
The two key features, Annual Income (k$) and Spending Score (1-100), are selected for the analysis.
The data is scaled using StandardScaler. This is a critical step for distance-based algorithms like K-Means to ensure that all features contribute equally to the cluster formation.
Finding the Optimal Number of Clusters (K):
The Elbow Method is implemented to find the optimal value for K.
The K-Means algorithm is run for a range of K values (from 1 to 10).
The inertia (within-cluster sum of squares) is calculated for each K.
A plot of Inertia vs. K is generated to visually identify the "elbow point"—the point where adding more clusters no longer provides a significant decrease in inertia.

Model Fitting and Visualization:

A final KMeans model is trained using the optimal K determined from the Elbow Method.
The fit_predict() method is used to assign each customer to a specific cluster.
The results are visualized on a 2D scatter plot, with each cluster color-coded for clear differentiation.
The centroids (centers) of each cluster are plotted to represent the "average" customer profile for that segment.

Clustering Evaluation:
The quality of the clustering is quantitatively evaluated using the Silhouette Score.
This score measures how dense and well-separated the clusters are. A higher score (closer to 1) indicates better-defined clusters.
