# Amazon Vine Analysis
## Overview of Project
A client, Sellby, has requested the analysis of reviews of similar products sold by their competitors. The results will help them create a marketing strategy to launch a large catalog of products on a leading retail website. The research was completed using Amazon Vine Review data, a program were companies pay a small fee to Amazon and provide products to Vine members in exchange for a published review. The data was analyzed using PySpark to perform an ETL process to extract the dataset, transform the data, connect it to an AWS RDS instance, and load the transformed data into pgAdmin. 

## Resources
Data
* [Amazon Review Data](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
* [Amazon Beauty Review Data](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Beauty_v1_00.tsv.gz)
Software:
* AWS
* Google Colab Notebook
* PostegreSQL 11
* pgAdmin4

## Results
Table 1. Number of Five Star Paid v. Unpaid Reviews for Amazon's Beauty Products

![image1](https://user-images.githubusercontent.com/57520471/175845715-36c276cb-3917-4d2a-812d-9cb7f958d727.png)

* These results are based on reviewers that have written more than or equal to 20 votes and write 50% or above helpful reviews.
* Vine (paid) results:
  * Total Reviews: 647 out of 74,760
  * Number of 5 Star Reviews: 229 out of 43,446
  * Percentage of 5 Star Reviews: 35.4%
* non-Vine (unpaid) results:
  * Total Reviews: 74,113 out of 74,760
  * Number of 5 Star Reviews: 43,217 out of 43,446
  * Percentage of 5 Star Reviews: 58.3%

## Summary 
* Based on the data for paid Amazon Beauty reviews, the Vine program does not yield the best results. Those that were paid to review were more likely to leave less than 5 stars as compared to unpaid reviewers (35.4% vs 58.3%). 
* The number of paid reviews vs unpaid reviews is very significant (647 vs 74,113). 
  * This observation caused by either paid reviewers not writing many reviews or writing less helpful reviews which would have caused the majority of paid reviews to be filtered out. 
  * Or this observation could be due to the lack of Beauty companies participating in a Vine program for Amazon. I do not think paid reviewers for beauty products have a positivity bias because only 35.4% of Vine reviewers were five stars. 
  * To further assess the benefits of the Vine program the average of Vine v non-Vine reviews should be calculated, as well as the mode.
  * Final thoughts: I think the Vine program is good if you have the extra budget for it because the program will place reviews on a newly marketed product (vs starting off with zero reviews). However, the program has not yielded significantly beneficial results and should not be the main marketing strategy. 
