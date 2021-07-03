# Amazon_Vine_Analysis

# Overview of Project

This  larger project is analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In the project, I have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I will use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, I will write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

# Outline of the project

  . Deliverable 1: Perform ETL on Amazon Product Reviews
  
  . Deliverable 2: Determine Bias of Vine Reviews
  
  . Deliverable 3: A Written Report on the Analysis README.md
  
 ## Deliverable 1: Perform ETL on Amazon Product Reviews
 
 #### Deliverable Requirements:
 
 ##### Steps
 
 1. pick a dataset to analyze from the following Amazon Review datasets:
 
 ![image](https://user-images.githubusercontent.com/80365882/124341672-cdc61e80-db72-11eb-97de-d8e9e77c1304.png)

 2. Create a new database with Amazon RDS
 3.In pgAdmin, create a new database inAmazon RDS server
 4. Download the challenge_schema.sql file
 5. In pgAdmin, run a new query to create the tables 
 6. Download the Amazon_Reviews_ETL_starter_code.ipynb file, then upload the file as a Google Colab Notebook, and rename it Amazon_Reviews_ETL.
 7. First extract one of the review datasets, then create a new DataFrame
 8. Next, follow the steps below to transform the dataset into four DataFrames that will match the schema in the pgAdmin tables:

### Results

#### The customers_table DataFrame

To create the customers_table, use the code in the Amazon_Reviews_ETL_starter_code.ipynb file and follow the steps below to aggregate the reviews by customer_id.

. Use the groupby() function on the customer_id column of the DataFrame you created in Step 6.

. Count all the customer ids using the agg() function by chaining it to the groupby() function. 

. After you use this function, a new column will be created, count(customer_id).

. Rename the count(customer_id) column using the withColumnRenamed() function so it matches the schema for the customers_table in pgAdmin.

 The final customers_table DataFrame should look like this:
 
 ![image](https://user-images.githubusercontent.com/80365882/124341850-44afe700-db74-11eb-9847-bd83e472fb3c.png)
 
 #### The products_table DataFrame
 
The products_table DataFrame To create the products_table, use the select() function to select the product_id and product_title, then drop duplicates with the drop_duplicates() function to retrieve only unique product_ids. Refer to the code snippet provided in the Amazon_Reviews_ETL_starter_code.ipynb file for assistance.

The final products_table DataFrame should look like this:

![image](https://user-images.githubusercontent.com/80365882/124342004-78d7d780-db75-11eb-8abd-9816d59c6be0.png)

#### The review_id_table DataFrame

The review_id_table DataFrame To create the review_id_table, use the select() function to select the columns that are in the review_id_table in pgAdmin, and convert the review_date column to a date using the code snippet provided in the Amazon_Reviews_ETL_starter_code.ipynb file.

The final review_id_table DataFrame should look like this:

![image](https://user-images.githubusercontent.com/80365882/124342039-b472a180-db75-11eb-8f57-8db79167a265.png)

#### The vine_table DataFrame

The vine_table DataFrame To create the vine_table, use the select() function to select only the columns that are in the vine_table in pgAdmin.

The final vine_table DataFrame should look like this:

![image](https://user-images.githubusercontent.com/80365882/124342052-d10ed980-db75-11eb-8c6d-4a7d1cc2fdb5.png)


## Deliverable 2: Determine Bias of Vine Reviews

### Results

##### Summary Table1

![image](https://user-images.githubusercontent.com/80365882/124343314-69f62280-db7f-11eb-95c2-e79b5f48e93a.png)

##### Summary Table2

![image](https://user-images.githubusercontent.com/80365882/124343386-d5d88b00-db7f-11eb-9877-65462c4c2cec.png)


## SUMMARY 

. The Furniture product have lower reviews results than Vine participants becouse 99.7% of all 5-star reviews are non-Vine.

. overall of all 5 Star reviews are also the same as the Furnitu becouse all are form vine participants.

## RECOMMENDATIONS:

. The Amazon Vine Analysis provide a favorable dataset on the 5-star rating

.Most of data isn't Vine reviews over specific products, that we could minimize the resluts and create a different dataset on just Vine products.


 

 
 
