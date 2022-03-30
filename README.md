# K-Means-Clustering
Customer segmentation identifies customers into distinct groups. You want to examine  a set of customers and identify those that behave similarly. You want to group them based on purchases of four products.
Here is the data – customers and product purchased
Customer#	ProductA	ProductB	ProductC	ProductD
1	0	0	1	1
2	0	1	0	1
3	1	1	0	0
4	1	1	0	1
5	1	0	0	0
6	0	0	1	0
7	1	0	1	1
8	1	1	0	0
9	1	0	0	0
10	0	0	1	1
11	0	0	1	1
12	1	1	0	0
13	1	0	1	0
14	0	1	0	0
15	0	1	0	1
16	0	0	1	1
17	1	0	0	0
18	0	0	0	1
19	0	1	1	1
20	0	1	0	1
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
Clusterr#	ProductA	ProductB	ProductC	ProductD
1	1	1	0	1
2	0	1	1	1
3	0	1	0	1



1.Start by calculating the distance of each customer from the three starting centroids.
Use  Euclidean Distance to measure how far apart the  customers are from the centroids.
Starting with Cluster # 1 and determine which cluster the customers belong to.
2, Update the centroids
3.Repeat steps  1 and 2 for three iterations - 

 



First Iteration 
 
For First Iteration, let us use K=3 and calculate the Euclidean Distance to measure how far apart these measures from the centroid.
Step1:Lets calculate the Euclidean distance by doing SQRT(($B2-$G$2)^2+($C2-$H$2)^2+($D2-$I$2)^2+($E2-$J$2)^2) for cluster 1 and customer 1.Similarly we are calculating the for all the customer for Centroid 1 ,2 and 3.
Step2:Assign cluster to customer based on their minimum Euclidean distance value.
First Iteration				Customer 	Cluster Assigned
1.732050808	1	1.414214		1	2
1	1	0		2	3
1	1.732051	1.414214		3	1
0	1.414214	1		4	1
1.414213562	2	1.732051		5	1
2	1.414214	1.732051		6	2
1.414213562	1.414214	1.732051		7	(1,2)
1	1.732051	1.414214		8	1
1.414213562	2	1.732051		9	1
1.732050808	1	1.414214		10	2
1.732050808	1	1.414214		11	2
1	1.732051	1.414214		12	1
1.732050808	1.732051	2		13	(1,2)
1.414213562	1.414214	1		14	3
1	1	0		15	3
1.732050808	1	1.414214		16	2
1.414213562	2	1.732051		17	1
1.414213562	1.414214	1		18	3
1.414213562	0	1		19	2
1	1	0		20	3
Step3:Update the centroids. We can calculate the new centroid values by taking average value =AVERAGE(J25:J33)
 
Updated centroid value looks like below:
Iteration1			
Cluster	ProductA	PRODUCTB	PRODUCTC	PRODUCTD
1	1	0.444444	0.222222	0.222222222
2	0	0.166667	1	0.833333333
3	0	0.8	0	0.8

Second Iteration 

Second iteration		Customer 	Cluster Assigned
1.551582227	0.235702	1.296148	1	2
1.401057801	1.312335	0.282843	2	3
0.638284739	1.840894	1.296148	3	1
0.981306763	1.649916	1.03923	4	1
0.544331054	1.649916	1.509967	5	1
1.360827635	0.849837	1.509967	6	2
1.186342028	1.027402	1.637071	7	2
0.638284739	1.840894	1.296148	8	1
0.544331054	1.649916	1.509967	9	1
1.551582227	0.235702	1.296148	10	2
1.551582227	0.235702	1.296148	11	2
0.638284739	1.840894	1.296148	12	1
0.922958207	1.312335	1.811077	13	1
1.186342028	1.545603	0.824621	14	3
1.401057801	1.312335	0.282843	15	3
1.551582227	0.235702	1.296148	16	2
0.544331054	1.649916	1.509967	17	1
1.360827635	1.027402	0.824621	18	3
1.586984095	0.849837	1.03923	19	2
1.401057801	1.312335	0.282843	20	3
Step1:Calculate the Euclidean distance for customer’s products with new centroid value. Assign the customers to one of the three clusters based on their calculated Euclidean distance(minimum).
Step 2: Update the centroid
 
Updated centroid value looks like below:
Iteration2			
Cluster	ProductA	PRODUCTB	PRODUCTC	PRODUCTD
1	1	0.5	0.125	0.125
2	0.14286	0.14286	1	0.85714
3	0	0.8	0	0.8
Third iteration
Third iteration		Customer	Cluster Assigned
1.667708008	0.247441	1.296148	1	2
1.425219281	1.332481	0.282843	2	3
0.530330086	1.789991	1.296148	3	1
1.015504801	1.577906	1.03923	4	1
0.530330086	1.577906	1.509967	5	1
1.425219281	0.880629	1.509967	6	2
1.334634782	0.880629	1.637071	7	2
0.530330086	1.789991	1.296148	8	1
0.530330086	1.577906	1.509967	9	1
1.667708008	0.247441	1.296148	10	2
1.667708008	0.247441	1.296148	11	2
0.530330086	1.789991	1.296148	12	1
1.015504801	1.220568	1.811077	13	1
1.131923142	1.577906	0.824621	14	3
1.425219281	1.332481	0.282843	15	3
1.667708008	0.247441	1.296148	16	2
0.530330086	1.577906	1.509967	17	1
1.425219281	1.030159	0.824621	18	3
1.667708008	0.880629	1.03923	19	2
1.425219281	1.332481	0.282843	20	3
Step1:Calculate the Euclidean distance for customer’s products with new centroid value. Assign the customers to one of the three clusters based on their calculated Euclidean distance(minimum).
Step 2: Update the centroid
 
Updated centroid value looks like below:
Iteration3			
Cluster	ProductA	PRODUCTB	PRODUCTC	PRODUCTD
1	1	0.5	0.125	0.125
2	0.14286	0.14286	1	0.85714
3	0	0.8	0	0.8

Now there is no change between Iteration 2 and Iteration3.
The below results conclude the customer  and the cluster they belong to.
Customer	Cluster Assigned
1	2
2	3
3	1
4	1
5	1
6	2
7	2
8	1
9	1
10	2
11	2
12	1
13	1
14	3
15	3
16	2
17	1
18	3
19	2
20	3
