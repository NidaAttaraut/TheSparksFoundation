What is k means clustering?

K-means clustering is a popular and widely used machine learning algorithm that can find groups of data that are similar to each other. This is done by creating K number of clusters, and then assigning each data point to the cluster with the nearest mean. The process continues until the groups do not change significantly any more.
I’ll be using r programming for this, import necessary libraries
The factoextra package, which provides functions for visualizing and analyzing clustering results.
We’ll be using the iris dataset where the species column will be our target variable
As this a unsupervised learning model we’ll remove our target variable from the dataset
 Then we’ll standardizes the data by scaling it, ensuring that all features have a mean of 0 and a standard deviation of 1 to make the clustering process easy 
This line calculates the Euclidean distance matrix between data points based on the standardized feature data.The Euclidean distance is a metric that calculates the straight-line distance between two points in a coordinate system.
the fviz_nbclust function is used to apply the Elbow Method to determine the optimal number of clusters for k-means clustering based on the within sum of squares. The elbow method, a common technique for selecting 'K,' involves plotting the variance against different values of 'K' and identifying the point where the decrease in variance slows down, resembling an "elbow.”In this case the optimal number of clusters are 3
We’ll use kmeans function to perform k-means clustering on the scaled data
the cluster means are the center points of the three clusters, while the clustering vector shows the cluster assignments for each data point.
The table function is used to construct frequency tables of the given factors. It creates a table of frequencies that helps in identifying the patterns and trends in the data.
In the given example, table(km.clusters, iris$Species) is creating a frequency table that shows the number of occurrences of each species (setosa, versicolor, or virginica) in each cluster of the K-means clustering algorithm applied to the iris dataset. This can be used to understand the distribution of the species in the different clusters and analyze the separation of species by the algorithm.

Reference: SpencerPao 
https://youtu.be/NKQpVU1LTm8?si=zQuXHQacQwpN3vgI
