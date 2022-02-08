# Amazon_Vine_Analysis

## Overview of the analysis:

This project analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

The Amazon Vine program has about 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. In this project, we pick one of these datasets and use **PySpark** to perform the ETL process to extract the dataset, transform the data, connect to an **AWS RDS (PostgreSQL)** instance, and load the transformed data into pgAdmin. Next, we use PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. Then, we write a summary of the analysis.

## Data Source:
This analysis use the [Pet Products Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz) from the [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) as the data source.

## Results:
1. How many Vine reviews and non-Vine reviews were there?
    * There are **170** Vine reviews
    * There are **37,840** non-Vine reviews
2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    * There are **65** 5-stars Vine reviews
    * There are **20,612** 5-stars non-Vine reviews
3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    * **38.24%** of Vine reviews were 5-stars
    * **54.47%** of non-Vine reviews were 5-stars

## Summary:
* Since the percentage of 5-stars reviews of the Vine program 
(**38.24%**) is much lower than the non-Vine reviews (**54.47%**), this indicates that having a paid Vine review may have bias on the review. However, we cannot conclude the reasons of causing the difference.
* We may run the same analysis on other [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), and compare the percentage of Vine & non-Vine 5-stars reviews, and see if there are similar results or not.
