# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Choose the number of clusters (K).
2.  Initialize cluster centroids.
3.  Assign data points to clusters.
4.  Update cluster centroids.
5.  Repeat steps 3 and 4.
6.  Evaluate the clustering results.
7.  Select the best clustering solution. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: THRIKESWAR.P
RegisterNumber:  2122222230162


import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Mall_Customers.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
  kmeans = KMeans(n_clusters = i, init = "k-means++")
  kmeans.fit(data.iloc[:, 3:])
  wcss.append(kmeans.inertia_)
  
plt.plot(range(1, 11), wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:, 3:])

y_pred = km.predict(data.iloc[:, 3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"] == 0]
df1 = data[data["cluster"] == 1]
df2 = data[data["cluster"] == 2]
df3 = data[data["cluster"] == 3]
df4 = data[data["cluster"] == 4]
plt.scatter(df0["Annual Income (k$)"], df0["Spending Score (1-100)"], c = "red", label = "cluster0")
plt.scatter(df1["Annual Income (k$)"], df1["Spending Score (1-100)"], c = "black", label = "cluster1")
plt.scatter(df2["Annual Income (k$)"], df2["Spending Score (1-100)"], c = "blue", label = "cluster2")
plt.scatter(df3["Annual Income (k$)"], df3["Spending Score (1-100)"], c = "green", label = "cluster3")
plt.scatter(df4["Annual Income (k$)"], df4["Spending Score (1-100)"], c = "magenta", label = "cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```
<br>
<br>
<br>
<br>

## Output:
data.head():

![278949588-20e28c10-49ec-4912-9b52-aa1fa6046cdd](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/e88af4cf-f5b0-4824-b46e-5a9aa864c7c5)

data.info():



![278949592-b72586a8-e2c9-46ab-bbbe-36120412beb3](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/2091a671-a894-4081-990f-1c90fdafc06f)


NULL VALUES:

![278949606-807815d1-9dd7-4139-a7d0-50d75fb3286c](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/151605f3-5026-4dcf-9ec5-c8452b49339c)

ELBOW GRAPH:

![278949617-b4d0d533-6132-4eb8-b1de-be37fee48eff](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/6733b746-6bfb-4238-b8d6-86dc21d313cc)

CLUSTER FORMATION:

![278949632-9ea2de21-b25c-473c-a445-be867560c5a5](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/b7961020-7542-4104-ae48-c5efcc1504ac)

PREDICICTED VALUE:

![278949643-7d1d3af3-1df5-4b47-baa7-2105225f1ea0](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/d9d1a1c6-6397-432a-a04f-a4c74b4f1db0)

FINAL GRAPH(D/O):

![278949652-f14deb56-9d40-4fe5-9100-677e33629c56](https://github.com/Naveensrinivasan07/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119475891/3d5d2918-2467-4bf2-95f8-2e40bcce9c9e)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
