# Customer Behavior Segmentation and Analysis with PCA and K-Means Clustering
This project focuses on analyzing customer data to identify distinct segments using Principal Component Analysis (PCA) for dimensionality reduction and K-Means Clustering to group customers. The resulting groups provide insights into customer behavior, enabling more targeted marketing strategies.

## Dataset

The full description of the dataset and the file can be obtained from: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis/data

## Workflow
1. Exploratory Data Analysis
   a. Preliminary Data Cleaning
   b. Univariate Analysis
     - Descriptive Statistics: Examine the Education and Marital Status distribution
     - Demographic Analysis: Examine the age, income and household (number of children) distribution and checking for outliers
     - Product Purchase Analysis: Examine the spending patterns of the customers on different products
     - Promotional Response Analysis: Examine the campaign effectiveness as well as the number of purchases made with a discount
     - Channel Analysis: Examine the number of purchases made via different channels (Website, Store, Catalog)
   c. Bivariate Analysis: Examine relationships and correlation between different features

2. Preprocessing
   - Standard scaling the data
   - Principal Component Analysis (PCA) dimensionality reduction to 3
   - Lemmatization
   - Punctuations removal and lowercasing of all texts

3. Clustering
   - Elbow Method to determine the optimum amount of clusters
   - Perform different clustering algorithms, particularly, K-Means, DBSCAN and Hierarchical Clustering
   - Evaluate the clustering algorithms based on:
     a. Silhouette Score: Measures how similar an object is to its own cluster compared to other clusters. Higher scores indicate better-defined clusters.
     b. Davies-Bouldin Index: Measures the average similarity ratio of each cluster with the cluster that is most similar to it. Lower scores indicate better clustering.
     c. Visualzing clustering results
   - K-Means Clustering performed best from all the evaluation, thus it was used

4. Cluster Profiling
   - In-depth analysis of each cluster to understand the behavior of the customers in each cluster to provide better business decisions
   - Cluster Description:
     a. Cluster 0 (Light Pink):
         - Customers in this cluster have moderate incomes.
         - Their total spending is clustered more on the lower end.
     b. Cluster 1 (Pink):
         - The incomes of these customers also have moderate incomes, but are generally on the higher end.
         - Their spending is also relatively high.
     c. Cluster 2 (Purple):
         - These customers have incomes ranging from the lower to mid-range.
         - These customers also have the lowest spending out of the other clusters.
         - Most number of customers
     d. Cluster 3 (Dark Purple):
         - This cluster contains customers with higher incomes.
         - Their spending is generally higher compared to the rest as well.
         - Least number of customers
   - Behavior Analysis:
     a. All the campaigns done performed very poorly for Clusters 0, 1 and 2, but performed best on Cluster 3. However, since it was found that Cluster 3 had the least number of customers, it would be wise to not focus on campaigns going forward as it would be a waste of costs, since the majority of their customers do not accept the campaigns.
     b. Discounted promotions perform much better compared to campaigns, and it also captured Cluster 0 the most, which is the cluster with the second most number of customers. Thus, the business may want to focus more on giving discounted promotions.
     c. In terms of where the customers like to purchase products, there is a considerable amount of traction for web purchase by Cluster 0, and therefore, the company may want to grow its website further to increase the tractions.
     d. Cluster 3 stands out as the high-value segment with significantly higher spendings, especially on wines and meats, with Cluster 1 coming in second. Thus the company may want to target Clusters 2 and 3 for premium products or creating budget-friendly offerings for Cluster 2.
