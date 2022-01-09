# **Amazon Beauty Product Vine Review Analysis**

## **Overview**
The purpose of this analysis was to determine whether a gift/reward type program for reviews would be beneficial. 

The following analysis was conducted on ratings for Amazon beauty products. PySpark was used to perform the ETL process: extract the data, transform the data, connect to an AWS RDS instance, and load the transformed data to pgAdmin: ![dataset](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Amazon_Beauty_Products_Data.png).
PySpark and SQL was used to perform the analysis on the dataset. 

## **Results**

### How many Vine reviews and non-Vine reviews were there? 
- A dataframe was created to show the all reviews (both vine and non-Vine reviews): There was a total of 5,115,666 reviews ![image](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Updated_Amazon_dataset_png.png)
- The dataframe was filtered to show only products that had more than 20 total reviews/votes: 79,227 reviews ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Count_filtered_votes.png)
- The data was filtered further to only show reviews that had more than 50% of people that believed the review was helpful. The total number of helpful reviews with more than 50% was **74,760 reviews** ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/helpful_votes_df.png)
- From this dataframe, 2 separate dataframes were created to show how many of the helpful votes were **Vine reviews: 647** ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/paid_vine_df.png) **non-Vine reviews: 74113** ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/unpaid_votes_df.png)

### How many Vine Reviews were 5-star reviews? How many non-Vine 5-star reviews?
- The 2 separate dataframes for Vine reviews and non-Vine Reviews were filtered to show only 5-star reviews. 
- Vine 5-star reviews total was 229 
- non-Vine 5-star reviews total was 43217 
- Total 5-star reviews for both Vine and non-Vine reviews were 43446 
![image](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Analysis_code.png)

### What percentage of Vine reviews were 5-stars? What percentage of non-Vine reviews were 5-stars? 
- Percentage was calculated by taking the total number of Vine 5-star reviews (non-Vine 5-star reviews) divided by the total number of 5-star reviews multiplied by 100. 
- 5-star Vine reviews had a .53% and 5-star non-Vine reviews had 99.5% 
![image](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Analysis_code.png)

## **Summary**
- The majority of helpful 5-star reviews were non-Vine reviews. There were a total of approx. 5 million reviews and roughly 75,000 reviews had more than 20 people review it and had more than 50% of people view it as helpful. That is only 1.5% of the whole dataset which is a very small amount. We can infer that not that many reviews are being made. From the helpful 5-star reviews the majority of those reviews were non-Vine reviews. 

- In order to determine if creating a gift/reward program for reviews is beneficial, an analysis should also be conducted on all reviews and not just 5-star reviews. We're missing a big piece of information here since we don't know if some of those low reviews were paid or not. Currently, it appears that there are more helpful reviews from non-Vine clients. 

- This information would be beneficial for the business analytics department to determine what their goal would be for the next quarter whether it is to promote more movement on $ellby's site by having this gift/reward program, or whether it's trying to determine which products to promote or discontinue. 