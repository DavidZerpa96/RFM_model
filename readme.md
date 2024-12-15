# RFM Model with K-Means for Retail Sales

## Overview
This project demonstrates the application of **RFM analysis** combined with **K-Means clustering** to segment customers based on their purchasing behavior. The project uses a dataset of retail transactions sourced from Kaggle.

**Dataset Source:** [Online Retail Listing - Kaggle](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)

---

## What is RFM Analysis?
RFM analysis is a method used in marketing to analyze and segment customers based on three key dimensions:

- **Recency (R):** How recently a customer made a purchase.
- **Frequency (F):** How often a customer makes purchases.
- **Monetary Value (M):** How much money a customer spends.

By combining these metrics, businesses can classify their customers into meaningful segments to optimize their marketing strategies and improve customer retention.

---

## What is K-Means Clustering?
**K-Means** is an unsupervised machine learning algorithm that partitions a dataset into `K` clusters, where each data point belongs to the cluster with the nearest mean. It is widely used for:

- Segmenting customers.
- Identifying patterns in data.
- Reducing the dimensionality of large datasets.

### Key Steps in K-Means:
1. Randomly initialize `K` cluster centroids.
2. Assign each data point to the nearest centroid.
3. Update the centroids based on the mean of the assigned points.
4. Repeat until the centroids no longer change significantly.

---

## Project Workflow
### 1. Data Preprocessing
- Loaded the dataset and cleaned it to remove duplicates and null values.
- Converted columns like `InvoiceDate` to appropriate formats for calculation.

### 2. RFM Calculation
- Calculated Recency, Frequency, and Monetary values for each customer.

### 3. Clustering with K-Means
- Determined the optimal number of clusters (`K`) using:
  - **Elbow Method**
  - **Silhouette Score**
- Segmented customers into 5 clusters based on their RFM scores.

### 4. Pareto Analysis
- Applied the Pareto Principle (80/20 rule) to identify the top 20% of customers contributing to 80% of revenue.

### 5. Business Recommendations
- Provided actionable insights for retaining high-value customers and improving engagement across segments.

---

## Key Results
### Customer Segments
- **Cluster 2:** High-value customers with high frequency and monetary values.
- **Cluster 3:** Loyal and valuable customers.
- **Cluster 0 & 1:** Average customers with moderate engagement.
- **Cluster 4:** New customers with low engagement.

### Pareto Analysis Highlights
- Top 20% of customers (approximately 1,363 customers) contribute to 80% of the total revenue.

---

## Files in the Repository
- `RFModelK-means.ipynb`: Jupyter Notebook containing the entire analysis.
- `online_retail_listing.csv`: Dataset used in the project.
- `README.md`: Documentation for the project.
- `requirements.txt`: To import the necessary libraries.

---

## How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/DavidZerpa96/RFM_model.git
   ```
2. Navigate to the directory:
   ```bash
   cd RFM_model
   ```
3. Install dependencies (if required):
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook RFModelK-means.ipynb
   ```

---

## Future Improvements
- Integrate real-time customer segmentation with live data.
- Use additional clustering techniques (e.g., DBSCAN) for comparison.
- Visualize more metrics such as lifetime value (CLV).

---

## Acknowledgments
Dataset sourced from Kaggle ([link](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)).
