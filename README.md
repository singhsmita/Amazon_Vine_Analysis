# Amazon Vine Review Analysis
![enter image description here](https://github.com/singhsmita/Amazon_Vine_Analysis/blob/main/Results/amazon_vine.png)

Analysis using PySpark , AWS RDS , pgAdmin.

## Project Overview
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

### Purpose
I am analyzing a dataset which provides reviews about shoes. I use  PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I have used PySpark to determine if there is any bias toward favorable reviews from Vine members in your dataset. Based on my analysis the summary /results are being shared with the stakeholders.


## Results
Using the dataset , I extracted , cleaned the data and transformed the dataset into dataframes to suit the requirement.

 -  **How many Vine reviews and non-Vine reviews were there?**
Findings :-
Total Number of Vine reviews  = 27009
Total number of Paid reviews = 22
Total number of Unpaid reviews = 26987
![enter image description here](https://github.com/singhsmita/Amazon_Vine_Analysis/blob/main/Results/Review_count.png)


 -  **How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?**
 Findings :-
 Total number of 5 star reviews = 14488
  Total number of  paid 5 star reviews = 13
   Total number of unpaid  5 star reviews = 14475
 
![enter image description here](https://github.com/singhsmita/Amazon_Vine_Analysis/blob/main/Results/5_Star_Reviews.png)


-   **What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?**

Findings :-
 Paid reviews as % of  total 5-star reviews = 0.09
  Percentage of 5-star reviews as part of total vine Paid  = 59.09
 Unpaid reviews as % total 5-star reviews = 99.91
 percentage of 5-star reviews part of total vine  unpaid = 53.64
![enter image description here](https://github.com/singhsmita/Amazon_Vine_Analysis/blob/main/Results/Total_percentage_of_5Star_Rating.png)

## Summary

The findings of the analysis suggest that there is a notable tendency towards a positivity bias in favor of the Vine program, where a significant percentage of Vine reviews were rated with 5 stars. Specifically, the data reveals that 59% of all Vine reviews received a 5-star rating, which is slightly higher than the corresponding percentage of 5-star ratings in non-Vine reviews, which was 53%. This difference in percentage suggests that the Vine program may have a higher rate of positive reviews compared to non-Vine reviews.

To establish the statistical significance of this observation, it may be useful to further explore the statistical distribution of star ratings between Vine and non-Vine reviews. By calculating the distribution measures such as the mean, median, and mode of the star ratings in each category, we could potentially reveal more information about the nature and magnitude of the differences between the Vine and non-Vine reviews.

![enter image description here](https://github.com/singhsmita/Amazon_Vine_Analysis/blob/main/Results/Bias_Analysis.png)

By comparing the two dataframes, we can see how the ratings and number of reviews differ between Vine and non-Vine customers. It looks like the Vine customers have given fewer reviews overall (22 compared to thousands in the non-Vine group) but they have a higher proportion of 5-star reviews (13 out of 22) compared to the non-Vine customers (14,475 out of almost 25,000). This could suggest that Vine customers may be more positive or enthusiastic about reviewing products, or that the products they receive are of higher quality. However, it's important to note that this is based on a small sample size and further analysis would be needed to draw any strong conclusions.
