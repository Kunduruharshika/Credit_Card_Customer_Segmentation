# Customer Segmentation using Unsupervised Learning

## Project Overview

This project focuses on segmenting credit card customers using unsupervised learning techniques, specifically K-Means clustering and Principal Component Analysis (PCA). The aim is to classify customers into meaningful segments based on their spending behavior, credit limits, and payment patterns. The goal is to create distinct customer groups that can help businesses optimize their marketing strategies, improve customer relationship management, and increase profitability.

By clustering the customers, we can gain valuable insights into their financial behaviors, which can be used to offer personalized services and targeted promotions, leading to better customer engagement and retention.

![Customer Segmentation Overview](https://github.com/Kunduruharshika/Credit_Card_Customer_Segmentation/blob/d212597defb2e6b912117ee6b51aea3a3917e84b/Supervised-and-Unsupervised-Learning.png)  
*Customer segmentation process overview.*

## Dataset Details

Training Data: 8,871 customer records  
Test Data: Not used (Unsupervised learning)  
Features: Various customer financial metrics, including:

- **Balance**: Current balance on the customer’s credit card.
- **Purchases**: Total purchases made by the customer.
- **One-off Purchases**: Total one-time purchases.
- **Installments Purchases**: Total installment-based purchases.
- **Cash Advance**: Total amount of cash withdrawn by the customer.
- **Credit Limit**: Customer’s credit limit.
- **Payments**: Payments made by the customer.
- **Minimum Payments**: Minimum required payments on the credit card.
- **Tenure**: Length of time the customer has been with the bank.

**Target Variable**: None (Unsupervised learning)

Key Features:
- **Balance**: The current balance of each customer.
- **Purchases**: The total amount spent by each customer.
- **One-off Purchases**: Amount spent on one-time purchases.
- **Installments Purchases**: Amount spent in installments.
- **Cash Advance**: Cash withdrawn by the customer.
- **Credit Limit**: The customer’s credit limit.
- **Payments**: Amount paid by the customer.
- **Minimum Payments**: Minimum amount that needs to be paid by the customer.
- **Tenure**: Duration of the relationship with the bank.

---

## Approach & Methodology

### 1. **Data Cleaning & Preprocessing**
- **Objective**: Prepare the data for clustering by handling missing values, scaling the features, and transforming categorical variables.
- **Actions Taken**:
  - Filled missing values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT` columns using suitable strategies.
  - Standardized the numerical features to normalize data for better clustering results.

### 2. **Feature Engineering**
- **Objective**: Enhance the data by creating relevant features.
- **Actions Taken**:
  - Engineered additional features related to customer spending patterns.
  - Used **PCA (Principal Component Analysis)** to reduce dimensionality and speed up the clustering process.

### 3. **Clustering with K-Means**
- **Objective**: Identify distinct customer segments using the K-Means algorithm.
- **Actions Taken**:
  - Determined the optimal number of clusters using the **Elbow Method**.
  - Applied **K-Means clustering** to segment customers based on financial behavior.
  - Visualized the clusters using PCA-reduced data to better understand the grouping.

### 4. **Cluster Profiling**
- **Objective**: Provide insights into each customer segment by analyzing their key characteristics.
- **Actions Taken**:
  - Analyzed the average values for each cluster to describe the financial behavior of the segments.
  - Categorized the clusters based on high spenders, low credit users, etc.

---

## Results & Business Impact

By segmenting the customers into distinct groups, businesses can create more personalized experiences and optimize marketing strategies. Below are the key findings:
- **Cluster 0**: High spenders with high credit limits.
- **Cluster 1**: Low spenders with medium credit limits.
- **Cluster 2**: Moderate spenders with low credit limits.
- **Cluster 3**: High balance holders with low credit utilization.

These insights can be used to prioritize high-value customers, tailor offers, and implement retention strategies.

---

## How the Business Problem is Solved

### **Segmentation of Customers**
The core business problem was to understand customer behavior and group customers into similar segments. By using **K-Means clustering**, we grouped customers based on their spending behavior, allowing for personalized customer engagement.

### **Business Benefits**:
- **Targeted Marketing**: Businesses can now create custom marketing strategies for each segment.
- **Customer Retention**: By identifying high-value or high-risk customers, the company can focus on customer retention efforts.
- **Improved Customer Insights**: Provides a deeper understanding of customer spending patterns and financial behavior.

---

## Tools & Technologies Used

- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Development Environment**: Jupyter Notebook

---

## How to Run the Project

To run the notebooks and replicate the analysis, you'll need to set up the environment:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Kunduruharshika/Credit_Card_Customer_Segmentation.git
   cd Credit_Card_Customer_Segmentation
