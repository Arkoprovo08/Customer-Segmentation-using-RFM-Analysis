# Customer Segmentation using RFM Analysis and K-Means Clustering

## Project Overview

This project focuses on **customer segmentation using RFM (Recency, Frequency, Monetary) analysis combined with K-Means clustering and rule-based refinement**.  
The goal is to identify different customer groups to support **targeted marketing strategies, churn reduction, and revenue optimization**.

---

## Objectives

- Understand customer purchasing behavior using RFM metrics
- Segment customers using unsupervised machine learning (K-Means)
- Improve segmentation with business rule-based refinement
- Identify key business segments such as:
  - High Value Customers
  - Regular Customers
  - At Risk Customers
  - Lost High Value Customers
  - Potential High Value Customers

---

## Dataset

The dataset contains transactional retail data with the following features:

- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

---

## Methodology

### 1. Data Preprocessing
- Removed null Customer IDs
- Filtered invalid transactions (zero/negative quantity or price)
- Created `TotalPrice = Quantity × UnitPrice`

---

### 2. RFM Feature Engineering
For each customer:
- **Recency**: Days since last purchase
- **Frequency**: Number of purchases
- **Monetary**: Total spend

---

### 3. Data Transformation
- Applied log transformation to reduce skewness
- Standardized features using StandardScaler

---

### 4. Clustering (K-Means)
- Used Elbow Method to determine optimal K
- Evaluated using Silhouette Score
- Final model: **K = 3**

---

### 5. Business Rule-Based Segmentation
Enhanced clustering results with domain rules to identify:

-  At Risk Customers  
-  High Value Customers  
-  Regular Customers  
-  Lost High Value Customers  
-  Potential High Value Customers  

---

## Key Visualizations

- Customer segment distribution
- Recency, Frequency, Monetary boxplots
- Frequency vs Monetary scatter plot
- Recency vs Monetary churn analysis
- Segment-wise RFM heatmap

---

## Key Insights

- Majority of customers fall under **At Risk and Regular segments**
- Small group of **High Value customers contributes major revenue**
- Identified **Lost High Value customers** (high spend but inactive)
- Found **Potential High Value customers** for upselling opportunities

---

## Business Impact

- Improve customer retention strategies
- Reduce churn using targeted campaigns
- Increase revenue through upselling and cross-selling
- Identify VIP customers for loyalty programs

---

## Tech Stack

- Python 
- Pandas / NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## Future Improvements

- Deploy model using FastAPI / Streamlit
- Add real-time customer scoring system
- Integrate with SQL database for live segmentation
- Build dashboard using Power BI / Tableau

---

## Conclusion

This project demonstrates how **machine learning + business rules** can be combined to build an effective customer segmentation system that is both **data-driven and business-actionable**.

---

## Author
Arkoprovo Ghosh

Data Science & Machine Learning Enthusiast
