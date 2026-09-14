# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to bedisplayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Print the outputs and end the program


## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: HARINNI S
RegisterNumber:  212224060093
*/
```python
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv(r"C:\Users\acer\Downloads\Mall_Customers.csv")
data.head()

```
<img width="1035" height="306" alt="Screenshot 2026-05-20 154045" src="https://github.com/user-attachments/assets/52a56d5d-df95-4e7a-ab26-32b9d3248743" />

```python
data.info()
```

<img width="1117" height="425" alt="Screenshot 2026-05-20 154057" src="https://github.com/user-attachments/assets/739d9587-5bb1-4640-be8d-56320c7f8144" />

```python
data.isnull()
```

<img width="1121" height="575" alt="Screenshot 2026-05-20 154113" src="https://github.com/user-attachments/assets/1cf94bc3-bda7-4bcc-9fa2-f2a93ffef912" />

```python
data.isnull().sum()
```
<img width="867" height="282" alt="Screenshot 2026-05-20 154121" src="https://github.com/user-attachments/assets/41abfe3f-83a8-4a34-a631-1aa1bd18c165" />

```python
from sklearn.cluster import KMeans
wcss= [] 
for i in range(1,11):
    kmeans=KMeans(n_clusters = i,init = "k-means++")
