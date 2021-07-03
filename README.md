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
 1. pick a dataset to analyze from the following Amazon Review datasets:
 
 ![image](https://user-images.githubusercontent.com/80365882/124341672-cdc61e80-db72-11eb-97de-d8e9e77c1304.png)

 2. Create a new database with Amazon RDS
 3.In pgAdmin, create a new database inAmazon RDS server
 4. Download the challenge_schema.sql file
 5. In pgAdmin, run a new query to create the tables 
 6. Download the Amazon_Reviews_ETL_starter_code.ipynb file, then upload the file as a Google Colab Notebook, and rename it Amazon_Reviews_ETL.
 
 
