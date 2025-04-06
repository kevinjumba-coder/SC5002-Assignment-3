# SC5002-Assignment-3
---
This lab uses the data obtained here: https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset/data
## Steps
---
1. Setting up environment on Jupyter Notebook
2. Dataset was loaded from the .csv file posted on this repository
3. Checking data for any missing data. None found, continue
4. Dropped irrelevant columns to make it neater, and decrease chances it may interfere with important data
5. Encoding categorical data To handle the nominal data (which has no order), one-hot encoding was used. To handle the ordinal data, label encoding was done to label a unique integer to each cataegory in specific columns.
6. Split into training/test As per regular ML practice, the training and test set was split with a 20% test ratio
7. Use a Classification model, MLP and Clustering model, k-means. We use elbow method for k-means, and plot the graph of k against inertias. After the training the MLP, we find the test accuracy score to be 34.6%, close to the mean of 34.7%
8. I then performed a 5 fold cross-validation on k-means, with the resulting values clustered closely together
9. A 5-fold cross validation was also performed on MLP, with near exact values each time as the result.
10. The Analysis and comparison was started. For MLP, we found that the performance was realistic and matched the dummy classifier. The results indicated the current features are not strongly predictive of the category. The dataset might also be noisy and lack discriminative features. For k-means clustering, the best k value was selected from a value of 4-6. Both models are sensitive to hyperparameters; MLP is more sensitive to data quality and overfitting, while k-means is highly sensitive to k and may form meaningless clusters if data isn't scaled or cleaned.
11. Model Limitations: For MLP - Needs labelled data, risk of overfitting, accuracy depends on features, not suitable if labels are noisy.
12. Model Limitations: For k-means - No labels required, risk of poorly separated clusters, output not directly interpretable, may fail if clusters overlap
13. Sensitivity of k-means to initial centroids happens when: The data has overlapping or unevenly distributed clusters. Clusters are of different densities or sizes. Initial centroids are poorly spaced.
14. What happens when Centroids are poorly initialised:The algorithm may converge to a local minimum, not the global optimum. The resulting clusters can be misleading or unstable. The inertia value may be higher, indicating worse compactness. The consistency of results across runs may vary significantly.
Practical Applications for MLP: Predicting Product Categories. Why? It uses labels to learn mappings
Practical Applications for k-means: Customer segmentation of targeting. Why? It finds groups without needing labels
