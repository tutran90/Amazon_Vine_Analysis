# **Amazon Beauty Product Vine Review Analysis**

## **Overview**
The purpose of this analysis was to determine whether a gift/reward type program for reviews would be beneficial. 

The following analysis was conducted on ratings for Amazon beauty products. PySpark was used to perform the ETL process: extract the data, transform the data, connect to an AWS RDS instance, and load the transformed data to pgAdmin: ![dataset](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Amazon_Beauty_Products_Data.png).
PySpark and SQL was used to perform the analysis on the dataset. 

## **Results**

### How many Vine reviews and non-Vine reviews were there? 
- A dataframe was created to show the all reviews (both vine and non-Vine reviews) ![code](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Creating_vine_df.png) ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/Vine_DF.png). 
- The dataframe was filtered to show only products that had more than 20 total reviews/votes ![dataframe](https://github.com/tutran90/Amazon_Vine_Analysis/blob/main/filtered_vine_df.png).
- 
