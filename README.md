# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries
2. Load the customer dataset using Pandas.
3. Store the selected features in variable X.
4. Choose the optimal number of clusters from the elbow graph.
5. Apply the K-Means clustering algorithm:
6. Add the predicted cluster labels to the dataset.

## Program:
```

Program to implement the K Means Clustering for Customer Segmentation.
Developed by: DHAMODHARAN S
RegisterNumber:  212225230049

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Downloads/Mall_Customer.csv")

X = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(X)

plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)

plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')

plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()
```
## Output:
<img width="1295" height="770" alt="image" src="https://github.com/user-attachments/assets/330b971a-35f7-450f-90d3-3f2c4d763af2" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
