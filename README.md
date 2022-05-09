# Big Data - Cloud ETL Process - Amazon Vine


* In 2 Google Colab notebooks, 2 datasets (baby product and toy product reviews) were extracted from [review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), one into each notebook. 

* In each notebook the datasets were transformed to fit the tables in the [schema file](../Resources/schema.sql).

* Then DataFrames that correspond to the tables were loaded into an RDS database.

* For the baby product data, the reviews were analyzed to see if vine reviews are bias for higher ratings. From the tables below that count the number of vine and non-vine reviews, for each star rating (1-5), the vine reviews appear to be skewed as higher rated.

![vine review](images/vine.png)
![vine review percentages](images/vine_percentages.png)
![nonvinereview](images/nonvine.png)
![non-vine review percentages](images/nonvine_percentages.png)

* The average star rating for all the reviews was about 4 stars. 84.73% of vine reviews scored at or above average where as only 77.4% of non-vine reviews scored at least average. So it seemes that vine reviews may generally be bias to favor the product being reviewd.
