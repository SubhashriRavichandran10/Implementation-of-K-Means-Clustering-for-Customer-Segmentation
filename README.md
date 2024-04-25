# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the necessary packages using import statement.


2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().


3.Import KMeans and use for loop to cluster the data.


4.Predict the cluster and plot data graphs.


5.Print the output and end the program.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: R.Subhashri
RegisterNumber:212223230219


import numpy as np
import pandas as pd

import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range (1,11):
kmeans=KMeans(n_clusters = i,init="k-means++")
kmeans.fit(data.iloc[:,3:])
wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No. of clusters")
plt.ylabel("wcss")
plt.title("Elbow matter")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-
100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-
100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-
100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-
100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-
100)"],c="magenta",label="cluster4")

plt.legend()
plt.title("Customer Segmets")

*/
```

## Output:

DATASET:


![Screenshot 2024-04-24 205722](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/69d1e9ad-79ac-4d7b-a98d-244a27a54346)


data.head():

![Screenshot 2024-04-24 205728](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/eadbb363-7834-4cf8-9791-11dc737ef45d)



data.info():


![Screenshot 2024-04-24 205735](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/f1d2fa72-2d43-4b61-ba25-464a594c2a4f)


data.isnull() & sum():

![Screenshot 2024-04-24 205742](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/778190df-76e3-43fe-93a7-5d15b6228b65)




Elbow method graph:

![Screenshot 2024-04-24 205750](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/2946f0a2-cd03-4feb-9c3f-68c47ed85f84)


K means cluster:

![Screenshot 2024-04-24 205757](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/5ad9207b-b47d-4f7b-82c2-ed7cdff69cb5)


Y_prediction value:
![Screenshot 2024-04-24 205804](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/6469b886-6c37-468f-b969-f5f78258f382)



Customers Segments Graph:


![Screenshot 2024-04-24 205811](https://github.com/SubhashriRavichandran10/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145743413/ae6d411a-989e-4481-9ff8-403f58f92d6a)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
