# Amazon_Vine_Analysis

## Overview
Analyze reviews written by members of the Amazon Vine program and compare them to reviews from non-Vine members. Determine if the Amazon Vine program has a higher 5-star review percentage than the non-Vine program users. 

### Tools
- **PostgreSQL**: to create the schema, load the transformed data frames, and export the vine_table data.
- **Amazon RDS**: to store big data 
- **Google Colab**: to extract data and transform with **PySpark**
- **Jupyter Notebook**: to load vine_table csv and perform analysis with **Pandas** from **Python**


## Results
After filtering the reviews by:
- 1) At least 20 total star reviews
- 2) At least 50% "helpful" reviews 
Here are the summaries for Vine and non-Vine members:
![paid_sum](https://user-images.githubusercontent.com/30487641/139776716-ad5b07e6-2282-4620-91e2-f95ddf0622a1.PNG)
![non-paid_sum](https://user-images.githubusercontent.com/30487641/139776724-21d8085d-529a-4463-ba9b-d5ea57f28913.PNG)





## Summary


