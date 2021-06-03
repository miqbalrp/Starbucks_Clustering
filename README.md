# Starbucks_Clustering

This is a very interesting dataset that I found in Kaggle and Github (the primary source is from Udemy Project) about Starbucks' customer behaviour after receiving offer from Starbucks. <br>

Hope will give you more insight and experience by my analysis. Have fun!

## 1. **Data Preparation** ([prep.ipynb](https://github.com/miqbalrp/Starbucks_Clustering/blob/main/notebook/1.%20prep.ipynb))
Will be described soon.

## 2. **Exploration Data Analysis** ([eda.ipynb](https://github.com/miqbalrp/Starbucks_Clustering/blob/main/notebook/2.%20eda.ipynb))

### Demographic Information
![Individual Demographic Distribution](https://user-images.githubusercontent.com/38918617/120574281-3a051380-c449-11eb-9ac7-55bd1bfd2dce.png)

![Individual Demographic Relation](https://user-images.githubusercontent.com/38918617/120574302-44271200-c449-11eb-866d-6dd0ef85c0ec.png)

* As we can see above that most of customers are **male**, and followed by **female**. For other genders the number is very small so that in the next analysis **we will focus on male and female gender**.
* The age of the customer follows a normal distribution where the data center around the age of 40-70. We can divide age data into 4 part: **youth** (<35), **middle** (35-48), **older** (48-80), and **senior** (80>)
* From income distribution we can say that **lower-middle income** (30k-80k) has the largest number while **upper-middle income** (80k-10k) is the second largest number. The rest is the **high income** custome (10k>).
* Scatter plot tells us that youth customer only has lower-middle income, middle age can be in a upper-middle one, and for high income only for older and senior customer.

### Became a Member Trend
![Became a Member Trend trough Time](https://user-images.githubusercontent.com/38918617/120574446-86e8ea00-c449-11eb-9d72-ccfd09e3947e.png)
* In general, we can see that the daily trend of new member registrations **increased in the middle of 2015**. Then it **rose again in the middle of 2017** before **the decline in early 2018**.
* From year to year more male customers become new members except in 2016 where there are slightly more female customers.
* Older customers always dominate every year as does the lower-middle income group.

### Customer Spend Amount
![Spend Amount Distribution](https://user-images.githubusercontent.com/38918617/120574643-e941ea80-c449-11eb-8ed5-f2cd54446ceb.png)

![Spend Amount by Demographic](https://user-images.githubusercontent.com/38918617/120574652-ee069e80-c449-11eb-9cec-fc221ad42554.png)

* First, for making sense of how amount distribution really is, we plot the histogram of amount. We get that small amount has the largest number of distribution and decrease to the large amount. From amount of 400 to 1600 we get really small number of customer that spend in that much, it must be our outlier for the next analysis (it can be prove from the next boxplot).
* Second, we draw amount with demographic segementation in boxplot. 
* We get here that even the female customer has less number of customer than male, but female customers spend more in transaction. 
* By the age group, we get that youth customer tends to spend in small number of amount than any other groups.
* As well ass the youth customer, the lower-middle also has the smallest number of amount. Since youth customer has lower-middle income, we can conclude a connection here.

### The Relation between How Many Offer Process Occur and the Transaction Amount
![Number of Offer Relation with Spend Amount](https://user-images.githubusercontent.com/38918617/120574749-18585c00-c44a-11eb-96c3-0b8178b2ee69.png)

* The three charts above will show is there any difference on customer that received more offer and less offer to amount of transaction spend.
* From visualization only (*statistical test can be conducted if needed*), we get that for customers that received more than two times offer tend to purchase in the relative some amount. But this fact is not true with viewed and completed offer where the more viewed and completed offer the more purchase amount.


