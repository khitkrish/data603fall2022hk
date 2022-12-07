## Big Data Final Project :  
<h1 align=center>
  ASSOCIATION ANALYSIS BETWEEN VARIOUS PRODUCTS IN THE INSTACART DATA USING SPARK </h1>
  
## Introduction 
Supermarkets all over the world are utilizing data mining techniques to analyze customer purchasing behavior in an effort to increase business and simultaneously satisfy customer needs. One such software is identifying the products that customers frequently purchase together and analyzing 'if-then' trends to know which products to suggest to customers if they purchase A. This aids them in positioning the appropriate goods in the appropriate aisle, aiding customers in remembering their needs. This shortens the shopping process while also assisting clients in stocking their homes and freezers in accordance with their demands.
## Data Source 
Instacart's real dataset from Kaggle, which contains information from 3 million grocery orders made by 200,000 users, will be used in this research. Depending on how frequently a user has ordered from Instacart, there are typically 4–100 different arrangements for each user. The dataset's URL is provided below:
> https://www.kaggle.com/c/instacart-market-basket-analysis/data

## Dataset Discription 
The dataset for this competition is a relational set of files describing customers' orders over time. The goal of the competition is to predict which products will be in a user's next order. The dataset is anonymized and contains a sample of over 3 million grocery orders from more than 200,000 Instacart users. For each user, we provide between 4 and 100 of their orders, with the sequence of products purchased in each order. We also provide the week and hour of day the order was placed, and a relative measure of time between orders. For more information, see the blog post accompanying its public release.
![Screen Shot 2022-12-06 at 12 56 59 AM](https://user-images.githubusercontent.com/60707196/205831753-5808d862-1dbb-4de6-8bee-c682aa432cd7.png)
## File descriptions
Each entity (customer, product, order, aisle, etc.) has an associated unique id. Most of the files and variable names should be self-explanatory.
