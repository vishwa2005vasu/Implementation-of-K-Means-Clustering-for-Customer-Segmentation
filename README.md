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

5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Vishwa Vasu R
RegisterNumber: 212222040183


import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No.of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

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
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
   
*/
```

## Output:

data.head()

![Screenshot (94)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/dea6dcb5-ffab-4bd7-8ec7-ada3d814cc88)







DATA.info():



![Screenshot (95)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/ddc425e2-3c89-421b-b465-cf7e649ccbd7)








NULL VALUES:




![Screenshot (96)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/4c510013-61d2-4e3d-94e9-d4a869286c8c)








ELBOW GRAPH:



![Screenshot (97)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/85fec3ce-99b3-4a75-9966-2be7dd3e038e)





CLUSTER FORMATION:






![Screenshot (98)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/0eaee223-1403-4944-b2e3-fda11158c92e)






PREDICICTED VALUE:







![Screenshot (99)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/ae364a9e-447f-4e6b-b07e-f993ab531768)









FINAL GRAPH(D/O):







![Screenshot (100)](https://github.com/MaheshMuthuL/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/135570619/df0df64b-eb7b-4853-b926-c3bb9d78d08f)










## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
