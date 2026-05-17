# Credit Card Customer Segmentation

This notebook groups credit card customers into different segments using K-Means clustering.

## Project idea

The goal is to understand customer behavior based on their credit card usage, such as balance, purchases, payments, cash advance, and credit limit.

## Steps

- Loaded the dataset
- Removed unnecessary columns
- Handled missing values
- Scaled the data
- Applied K-Means clustering
- Used the elbow method and silhouette score
- Chose the best number of clusters
- Analyzed the customer segments

## Result

The final model divided the customers into 3 groups.

## Questions and Answers

### 1. Why is this an unsupervised learning problem?

This is an unsupervised learning problem because there is no target column or predefined customer label. The model tries to find hidden groups in the data.

### 2. Why did we remove the `CUST_ID` column?

We removed `CUST_ID` because it is only a customer identification number. It does not help describe customer behavior.

### 3. Which columns had missing values?

The columns with missing values were:

- `CREDIT_LIMIT`
- `MINIMUM_PAYMENTS`

### 4. How did you handle the missing values?

The missing values were filled using the mean value of each column.

### 5. Why is scaling important before applying K-Means?

Scaling is important because K-Means uses distance to form clusters. If the data is not scaled, columns with large values may affect the result more than other columns.

### 6. Which K value did you choose?

I chose `K = 3`.

The elbow method showed that the improvement became smaller after 3 clusters. Also, the silhouette score was best for 3 clusters, so it was selected as the final value.

### 7. Describe each customer segment

- **Cluster 0:** Customers with high balances and high cash advance usage. They do not make many purchases.
- **Cluster 1:** Active customers with high purchases, high credit limits, and high payments.
- **Cluster 2:** Less active customers with lower balances, lower credit limits, and fewer transactions.

### 8. Which cluster may represent high-value customers?

Cluster 1 may represent high-value customers because they have high purchases, high payments, and high credit limits.

### 9. Which cluster may represent customers who rely more on cash advance?

Cluster 0 may represent customers who rely more on cash advance because they have the highest cash advance usage.

### 10. How can a company use these clusters for marketing strategy?

A company can use these clusters to create different marketing strategies. High-value customers can receive rewards and premium offers. Cash advance customers can receive financial support or payment plans. Less active customers can receive promotions to encourage more card usage.

## Tools used

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn