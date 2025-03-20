# Customer Segmentation Analysis


This project showcases a complete workflow for banking customer segmentation using a K-Means clustering approach. By analyzing demographic and financial features, we derive meaningful customer groups and gain insights that can guide marketing, risk management, and customer outreach strategies.

Project Overview

Data Exploration: Assesses shape, missing values, and key statistics.

Univariate Analysis: Visualizes distributions of both numerical and categorical features (e.g., age, balance, job, etc.).

Outlier Handling: Caps extreme values at the 1st and 99th percentiles, ensuring more robust segmentation.

Preprocessing: Cleans and encodes data using pipelines for numeric (median imputation, scaling) and categorical (most frequent imputation, one-hot encoding) features.

Dimensionality Reduction (PCA): Reduces data to 2 principal components for simplified 2D visualization.

Optimal Clusters: Uses the Elbow Method (plotting inertia) to decide on k = 3.

K-Means Clustering: Groups observations into 3 clusters.

Evaluation: Assesses clustering quality using the Silhouette Score and silhouette plots.

Insights & Visualizations: Creates bar plots (e.g., balance, age, subscription distribution) to interpret each cluster.

Dataset & Features

Source: Banking dataset with attributes like age, balance, job, duration, etc.

Key Columns:

Numeric: age, balance, duration, campaign, previous

Categorical: job, marital, education, default, housing, loan, contact, poutcome, month

Target: deposit (whether a customer subscribed to a term deposit)

Repository Files

Notebook/Script: The core code performing all steps (exploration, outlier handling, preprocessing, PCA, clustering, evaluation).

Generated Plots:

numerical_distribution.png: Histograms of numeric columns.

distribution_{col}.png: Distribution of each categorical column.

elbow_plot.png: Visualizes different k-values to identify the elbow.

pca_clusters.png: 2D PCA scatter colored by cluster.

cluster_balance.png, cluster_age.png, cluster_deposit.png: Summaries of important features across clusters.

silhouette_plot.png: Silhouette coefficients per cluster.

Key Results & Observations

Optimal K = 3:

The Elbow method indicated a noticeable bend at k=3.

Cluster Characteristics (Numeric Summary):

Cluster 0: Middle-range average balance, moderate age.

Cluster 1: Possibly younger with lower average balance.

Cluster 2: Potentially older with higher average balance.

Categorical Summary:

Job distribution across clusters differs—some roles are more dominant in certain clusters.

Deposit Subscription shows variation by cluster, indicating different propensities to subscribe.

Silhouette Analysis:

Silhouette Score is around ~0.4 (example range), suggesting moderate separation among clusters.

The silhouette plot shows each cluster's internal cohesion and separation from others.

How to Use

Install dependencies:

Run the Jupyter Notebook or Python script.

Outputs (plots) will be saved in the working directory.

Examine cluster distributions to glean marketing or business insights.

Business Relevance

Detailed Insights

Based on the data:

Cluster 2 generally comprises older customers with higher average balances. They also appear more inclined to subscribe to term deposits, indicating they have both the resources and a willingness to invest. As a result, Cluster 2 represents a prime segment for marketing deposit products, wealth management services, or premium banking features.

Cluster 0 holds customers with moderate balances, who might be open to mid-tier offerings but may need more incentives to increase deposits or upgrade products.

Cluster 1 often includes younger customers with lower balances. This group may require different, more introductory financial products, such as basic savings accounts or educational financial planning programs, potentially improving future loyalty.

Which Cluster to Target?

For maximizing immediate returns on term deposit marketing:

Target Cluster 2, as they have higher balances and a demonstrated propensity for deposits.

Secondary Approach: With the right strategy, either Cluster 0 or Cluster 1 can be nurtured over time for future up-selling or cross-selling opportunities.

Additional Business Benefits

Resource Allocation: Focus campaigns on high-value or high-potential segments (e.g., older, higher-balance customers).

Product Personalization: Tailor features to each cluster’s financial needs—premium vs. entry-level.

Customer Satisfaction: Deliver appropriate product offerings, likely improving retention.


Next Steps

Experiment with alternative clustering algorithms (e.g., Hierarchical, DBSCAN) or more advanced dimension reduction (UMAP, t-SNE).

Compare multiple metrics, including Calinski-Harabasz and Davies-Bouldin.

Feature Engineering to incorporate new relevant data and refine segmentation.


Thank you for exploring this Customer Segmentation Analysis. For improvements, feel free to open issues or submit pull requests!



