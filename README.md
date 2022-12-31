
# Insiders Clustering

<img src= "img/high-value-customers.png" width= "600" height= "350"> 


Project from Data Science Community, mentoring by Meigarom Lopes.

The business problem is selecting customers to create a loyalty program called Insiders.
A UK-based online retail store has captured the sales data for different products for the period of one year (Nov 2016 to Dec 2017). The organization sells gifts primarily on the online platform. The customers who make a purchase consume directly for themselves. There are small businesses that buy in bulk and sell to other customers through the retail outlet channel.



# 1. Business Problem.
Find significant customers for the business who make high purchases of their favorite products. The organization wants to roll out a loyalty program, called Insiders, to the high-value customers after identification of segments.

**Dataset Description** : https://www.kaggle.com/vik2012kvs/high-value-customers-identification

Attribute:     Description

InvoiceNo:      Invoice number (A 6-digit integral number uniquely assigned to each transaction)
 
StockCode :     Product (item) code

Description :   Product (item) name

Quantity :      The quantities of each product (item) per transaction

InvoiceDate:    The day when each transaction was generated

UnitPrice:      Unit price (Product price per unit)

CustomerID:     Customer number (Unique ID assigned to each customer)

Country :       Country name (The name of the country where each customer resides)

# 2. Business Assumptions.

- Indicate customers who will be part of a loyalty program called Insiders.
- What are the main characteristics of these customers?: Ticket, bascket size, high LTV, churn probability,high TVC prevision, purchasing propensity, age, location.
- How many customers will be part os this group?
- RFM model (recency, frequency,, monetary): sorted data to have a RFM Score.

# 3. Solution Strategy

**Data Description:** rename columns, check NA values, change types.

**Feature Engineering:** recency, frequency, monetary, gross revenue.

**Cluster Analysis:** Visualization Inspection, UMAP -t-SNE
<img width="1142" alt="Screen Shot 2022-02-27 at 17 34 27" src="https://user-images.githubusercontent.com/86486485/155898928-fcb23108-9273-4942-a1bc-726c9ba7f34b.png">

**Feature Engineering:** create new attributes based on the original variables using mindmap hypothesis.

**Exploratory Data Analysis (EDA):** univariate and bivariate analysis. Embedding space study with PCA, UMAP, t-SNE, Decision Tree.

**Hyperparameter Fine Tuning:** K-Means, GMM, Hierarchical Clustering.
<img width="1136" alt="Screen Shot 2022-02-27 at 17 31 05" src="https://user-images.githubusercontent.com/86486485/155898897-680b9f7c-4586-4210-b410-1ab0e3859a71.png">

**Deploy** Database Sqlite: insiders_db.sqlite

# 4. Top 3 Data Insights
**H1** Insiders cluster has a volume of product purchases above 10% of total purchases.

**True** Insiders cluster has a product purchase volume of 38%

**H2** Insiders cluster has a volume of gross revenue above 10% of total purchases.

**True** Insiders cluster has GMV colume of 41%.

**H5** The GMV of cluster Insiders is concentrated in the 3rd quartile.

**False** The GMV of cluster Insiders is concentrated in the 1rd quartile.
<img width="1125" alt="Screen Shot 2022-02-27 at 13 15 19" src="https://user-images.githubusercontent.com/86486485/155890296-21473018-6495-4909-a7d3-53f7dc27ddfd.png">

# 5. Machine Learning Model Applied
<img width="600" alt="Screen Shot 2022-02-27 at 13 16 24" src="https://user-images.githubusercontent.com/86486485/155890327-b1896660-3a58-4a3f-affa-f05da054a871.png">

# 6. Machine Learning Modelo Performance
<img width="678" alt="Screen Shot 2022-02-27 at 13 17 19" src="https://user-images.githubusercontent.com/86486485/155890354-7b357853-0954-4a04-994f-9a09a6c7ff16.png">

# 7. Business Results
<img width="918" alt="Screen Shot 2022-02-27 at 13 18 32" src="https://user-images.githubusercontent.com/86486485/155890381-9080fdbf-a728-4e29-88a0-cfcf17f72fa3.png">

# 8. Conclusions
**Cluster Insiders**
- Number of Custmers: 495 (25,26% of customers)
- Average Recency: 77 days
- Average Purchase: 399
- Average Revenue: 8311.14 dollars
- Freuency of Purchase: 0.37 products/day
- Quantity of Returns: 290
