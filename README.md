## Data603 - Platforms for Big Data Analysis
## Market Basket Analysis

## Introduction
<p align="center">
<img width="760" height="450" src="https://cdn-images-1.medium.com/max/717/1*ulB2MwvLLxnqC2vNIbA9Rg.png">
</p>
The future of supermarkets and online grocery stores depends on a term called product placement, which basically means identifying and analyzing users buying pattern and placing the right suggestion of commodities or groceries. To do the same, big data and machine learning have joined hands and invented various data mining techniques to analyse the customer buying pattern and using algorithms to recommend right product to the buyer. This however increases the business efficiency and customer engagement along with increasing the customer satisfaction which is pretty much the foundation of every business. One such algorithm in the world of logistic regression of machine learning is association rule mining. in this project we will be using FP Growth Algorithm under association rule mining to analyse the cart wise pattern and build different metrics like lift, confidence and support to study the association of the itemsets. This helps the modern supermarket industry to engage their customers while the buyer saves time spent on shopping. This would also help the customers remember their needs and assists clients in stocking their homes and freezers in accordance with their demands.

## Project Abstract
In our project we use a ~3.4 Million dataset from kaggle that has original dataset from Instacart website. It also has supporting dictionary datasets and evaluation sets to form the merge between the tables and analyse the association. After the dataset is complete, data is converted into carts by combining the order and products dataset. Following the process, FPGrowth Algorithm is applied on the carts datatable as its builds a Frequency pattern tree based on a If-Then criteria by analysing the association between the itemsets. This algorithm does so using the metrics like support, lift and confidence. The the antecedent(If) and consequent(Then) table is formed where consequent are the resulting recommendation.

## Data Description

Data link - https://www.kaggle.com/competitions/instacart-market-basket-analysis/data?select=orders.csv.zip
1. orders(~3.4 M)
   This dataset contains all the historical details of 3 million orders as per the below fields,

      orderid - Identifier for the orders.

      user_id - Identifier for the users.

      eval_set - Identifies the eval set the order belongs to.

      order_number - The order sequence of the user.

      order_dow - the day of the week the order was placed on.

      order_hour_of_day - the hour of the day the order was placed on.

      days_since_prior - days since the last order placed by the user(users with one orders have been given a value N/A).

2. products(~50 K)
This dataset contains the details of a product w.r.t the aisle and the department it belongs to.

      product_id - Identifier for the products.

      product_name - Name assigned to a product.

      aisle_id - Aisle associated with the product.

      department_id - Department associated with the product.

3. aisles(134)
Acts like a dictionary dataset that contains aisles data.

      aisle_id - Identifier for the aisles.

      aisle - Name assigned to the aisle.

4. departments(21)
Acts like a dictionary dataset that contains department data.

      department_id - Identifier for departments.

      department - Name associated with the departments.

5. order_products_SET(~3 M +)
Contains evaluation set for the prior, test and training orders.

      order_id - Foreign key containing identifier for the orders.

      product_id - Foreign key containing identifier for the products.

      add_to_cart_order - order in which the product was added to cart.

      reordered - depicts if the product was ordered in the part, if no product ordered previously then 0.

      eval_Set in the orders dataset can be one among the below three datasets,

      prior(~3.2 M) - orders prior to the users most recent order.

      train(~131 K) - training data to aid the ML model.

      test(~75 K) - test data for ML model.
 
## How to Find and Run Code
      
### The latest publish link is as below,

https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/2369395306214346/4499639871704699/3174366705860897/latest.html

### How to get access to the file in Databricks community edition workspace,

Step 1 – To get access to the file, reach out to any team members to any of the email IDs below,
      1.	Poojaa1@umbc.edu
      2.	purushj1@umbc.edu
      3.	sgande1@umbc.edu
      4.	so73977@umbc.edu
      
Step 2 – Once you are assigned as a user of the workspace by any of the team members, you should be able to see the tables in the DBFS and run the notebook.

Step 3 – To check the tables click on “DATA”  “Create Table” side navigation, this will land you to the below page.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206330996-cf716f23-4590-4072-9df1-105cea52d88b.png">

Step 4 – Click on the “DBFS” top navigation to get the folder structure of Databricks File system in community edition. All the dataset related to this project are stored here.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331093-c2d32065-456d-42cf-8c22-d0c29316d627.png">

### How to Run the notebook,

Step 1 - Once the access to the workspace is given, the workspace can be accessed by clicking on the “Workspace” side navigation and access the “Shared” notebook named “DATA603_FinalProject”.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331284-8615f76e-08a2-473f-a385-eb17e06ade16.png">

Step 2 – After opening the notebook “DATA603_FinalProject”, make sure to have a cluster up and running at the top right corner of the notebook.

Step 3 – In case the old cluster has been terminated, create a cluster resource by clicking on “My Cluster”  “More” ”Create new resource”.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331405-4837fc38-cfff-4122-8f6d-4c24e7f9fab8.png">

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331412-604666e7-e1e8-4243-b279-e096c9ed35c0.png">

Step 4 – Click on “Create, Attach, & Run” to create a cluster and start it.

Step 5 – Click on “Run all” to run the code.

### To access the file and import to native Databricks,

Step 1 – The Databricks notebook has been published publicly via the link attached above, click on the link to reach to the notebook.

Step 2 – In the Databricks notebook page, the introduction and data dictionary has been mentioned before the code. To run the code, the user must import the notebook using import button at the right corner of the page.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331547-8aafcbfc-4b13-4de9-b65c-0e600ab3672c.png">

Step 3 – Once the import is clicked, an instruction window will pop-up that says the below,

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98848906/206331576-ce018928-0b2a-4dcd-ad3f-cb514ec4114d.png">

Step 3 - after downloading the notebook, the next step is to upload it into users native Databricks and run it.

NOTE: As the free version allows the creation of standard cluster only, new clusters must be created as the old one terminates. The old one detached and new resource is created.


