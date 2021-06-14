# Starbucks_Clustering

This is a very interesting dataset that I found in Kaggle and Github (the primary source is from Udemy Project) about Starbucks' customer behaviour after receiving offer from Starbucks. <br>

<p align="center">
  <img width="" height="400" src="https://user-images.githubusercontent.com/38918617/120599976-67b28280-c472-11eb-970d-47083e2c4bbd.jpeg">
</p>

Hope will give you more insight and experience by my analysis. Have fun!

## 1. **Data Preparation** ([prep.ipynb](https://github.com/miqbalrp/Starbucks_Clustering/blob/main/notebook/1.%20prep.ipynb))
Will be described soon.

## 2. **Exploration Data Analysis** ([eda.ipynb](https://github.com/miqbalrp/Starbucks_Clustering/blob/main/notebook/2.%20eda.ipynb))

## 3. **Clustering Using K-Means** ([clustering.ipynb](https://github.com/miqbalrp/Starbucks_Clustering/blob/main/notebook/3.%20clustering.ipynb))

### Determine The Best Number of Cluster
![Elbow and Silhoute Method](https://user-images.githubusercontent.com/38918617/121834478-18cdde00-ccf9-11eb-8a13-bf646fe53f89.png)

From SSE chart we can observe that value starts to be smooth (*arm* side) at either k=3 or k=4. <br>
To get more confidence, we will use Silhouette Score where the value for k=3 is greater than k=4.<br> 
Therefore we will choose **k=3** as the number of clusters.

![Number of Clusters](https://user-images.githubusercontent.com/38918617/121834678-8b3ebe00-ccf9-11eb-9ca3-b7f6a2d5bc2a.png)

From the results of clustering with k = 3, we get the number of customers who are evenly distributed ~5000 people per cluster.

The chart cluster exploration series from the [notebook](https://user-images.githubusercontent.com/38918617/121834678-8b3ebe00-ccf9-11eb-9ca3-b7f6a2d5bc2a.png) gives us an idea of the characteristics of each cluster.

### Age and Gender
* Customers with an older age (50-70) are mostly in cluster 0, while in clusters 1 and 2 are dominated by younger customers.
* Although not significantly different, in each cluster it shows that the average age of women is older than men.

### Seniority
* In terms of seniority, cluster 0 and cluster 2 share a similar distribution where customers who became members in 2015-2016 are mostly spread across these two clusters. Meanwhile, customers who recently joined (in 2018) dominate in cluster 1.

### Income
* The distribution of income can be seen from the scatter plot of the comparison of income and amount.
* Since most of the older customers are in cluster 0, we can also observe that the large income distribution (> 80,000) is in cluster 0.
* For customers with income less than 80,000, they are divided into clusters 1 and 2 which are distinguished by the amount of transactions made.

### Amount of Transaction
* We use sum and average to aggregate the amount of transactions.

* Cluster 1 and cluster 2 are well distinguished from the total amount where cluster 1 has a smaller total amount than cluster 2.

* Although cluster 0 dominates the entire range of total amount with income > 80,000, customers with this cluster also have a smaller income but have a large total amount (> 400).

* From the point of view of an average transaction, cluster 1 is in the upper right corner which indicates a customer with a high value in terms of income and average amount.

* For cluster 1 and cluster 2, there is overlap in the average amount, but in general cluster 1 (as before) has a smaller value than cluster 2.

### Possibility of Completing Offers
* On the violin plot, it can be clearly seen that cluster 1 has a small probability of completion from both the BOGO and Discount offers.

* Meanwhile, in Informational offers, the three clusters do not show a significant difference (keep in mind that specifically for informational offers, what is calculated is the number of views, different from other types of offers).

* To be more specific in comparing cluster 0 and cluster 2, we will use a point plot that shows cluster 2 has a slightly higher average completion value.

## 4. Conclusion and Recomendation
The results of the cluster analysis obtained from the K-Means method above provide some insight to us. The offers that have been given previously, BOGO and Discount, should be focused on customer cluster 0 and and cluster 2 which gives a greater possibility to complete the offer compared to cluster 1.<br>

When compared between cluster 0 and cluster 1, cluster 0 which is dominated by customers with an older age and high income provides the biggest profit (in terms of total amount and average amount per transaction). However, cluster 0 still has a slightly lower probability of completing the offer. This needs to be a concern for the next offer period. <br>

We recommend continuing to investigate some variables that have not been discussed in this project. Among them is the role of channel giving offers. Is there any influence between offers via web, email, mobile, or social channels? In addition, we have not paid attention to the reward points and dificulty of each offer given. Some of these things are potentials that can be explored further in the next project.

## 5. Dig Deeper
In addition to Python notebooks, we have also created a dashboard using Tableau Public which can be accessed at the following link:

https://public.tableau.com/app/profile/iqbal5898/viz/Starbucks_Clustering/StarbucksCustomerClustering

![image](https://user-images.githubusercontent.com/38918617/121834826-ec669180-ccf9-11eb-8cb6-2c424ad338da.png)
