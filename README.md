# Amazon_Vine_Analysis

## Overview
Analyze reviews written by members of the Amazon Vine program and compare them to reviews from non-Vine members. Determine if the Amazon Vine program has a higher 5-star review percentage than the non-Vine program users. 

### Tools
- **PostgreSQL**: to create the schema, load the transformed data frames, and export the vine_table data.
- **Amazon RDS**: to store big data 
- **Google Colab**: to extract data and transform with **PySpark**
- **Jupyter Notebook**: to load vine_table csv and perform analysis with **Pandas** from **Python**


## Results
From (https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) I chose "Electronics" to analyze. After filtering the reviews by: 1) At least 20 total star reviews, and 2) At least 50% "helpful" reviews, here are the summaries for Vine and non-Vine members:

![paid_sum](https://user-images.githubusercontent.com/30487641/139776716-ad5b07e6-2282-4620-91e2-f95ddf0622a1.PNG)

![non-paid_sum](https://user-images.githubusercontent.com/30487641/139776724-21d8085d-529a-4463-ba9b-d5ea57f28913.PNG)

## Summary
Of the 50,753 reviews that made it through the filter (described above) over 97.8% of them were from non-paid reviews. The relatively small sample size of 1,080 for paid reviews is not ideal. However, there does not appear to be any positivity bias for the reviews in the Vine program since the non-paid reviews have a 5-star percentage that is over 4% higher than paid reviews.

Knowing the 5-star percent is important but misses some information. What was the average ratings? What do the ratings distributions look like? Are they distributed similarly? To be more confident in my assertion of no bias, I would first compare the average ratings between the two groups. Then I would bin each of them from 0 to 5 stars with 0.5 star intervals. If there is no positivity bias, then the averages should be close (or the paid reviews should be larger), and the distributions should be similarly shaped.

I would also suggest testing a couple different category datasets from Amazon to make sure Electronics isn't an isolated case.
