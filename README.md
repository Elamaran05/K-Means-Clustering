# K-Means-Clustering
 Examine a set of customers and identify those that behave similarly. You want to group them based on purchases of four products.
Here is the data – customers and product purchased


![image](https://user-images.githubusercontent.com/96159329/160776312-da8a235b-2967-462f-b8ea-3dc384964d9a.png)

Data Exploration: 20 customers. 4 products + customer ID. Binary where 1 = purchased. 0 = no purchase.
•	9 / 20 (45%) have purchased product A
•	9 / 20 (45%) purchased product B
•	8 / 20 (40%) purchased product C
•	11/ 20 (55%) purchased product D

PROCEDURE 
Group the individuals into three clusters using K-Means cluster method and the Euclidean distance measure. Show your work. 
Show each step in how records are added to a cluster. This will be based on the mean vector (centroids). Remember the mean vector is recalculated each time a new member is added to the cluster. At the end you will want to make sure that each record is assigned to the closest mean. 
Applying K Means: Pick random K centroids and then iteratively assign all other points to one of the K clusters by looking for the smallest distance to the centroids. In this case  use K = 3 and determine the customers in the  three clusters. 
Define the initial cluster centroids as:

![image](https://user-images.githubusercontent.com/96159329/160776794-0093732f-d3e5-4179-ae7c-c976e93d2820.png)


1.Start by calculating the distance of each customer from the three starting centroids.
Use  Euclidean Distance to measure how far apart the  customers are from the centroids.
Starting with Cluster # 1 and determine which cluster the customers belong to.
2, Update the centroids
3.Repeat steps  1 and 2 for three iterations - 

