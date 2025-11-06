# 🛍️ Customer Segmentation using K-Means Clustering

## 📘 Project Overview
This project applies **K-Means clustering** to group mall customers into meaningful segments based on their **Annual Income** and **Spending Score**.  
The objective is to identify distinct customer types that can help businesses design **targeted marketing strategies** and improve customer engagement.

---

## 🧠 Objectives
- Explore and understand customer data.  
- Perform **data preprocessing** and **feature scaling**.  
- Use the **Elbow Method** to determine the optimal number of clusters.  
- Apply **K-Means clustering** to identify customer segments.  
- Visualize the clusters and interpret the results.

---

## 🧹 Dataset Description
The dataset contains **200 mall customers**, each with demographic and spending information.

| Feature | Description |
|----------|-------------|
| `CustomerID` | Unique identifier for each customer |
| `Genre` | Gender (Male/Female) |
| `Age` | Customer’s age |
| `Annual Income (k$)` | Annual income in thousand dollars |
| `Spending Score (1-100)` | Mall-assigned score based on customer behavior and spending nature |

**Source:** [Mall Customer Segmentation Data (Kaggle)](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

---

## 🔍 Exploratory Data Analysis (EDA)
EDA revealed key patterns about customer demographics and spending behavior:

- **Age Distribution:** Most customers are between **25–40 years old**.  
- **Income Distribution:** Centered around **$60k–70k**, with few high earners.  
- **Spending Score Distribution:** Shows a **bimodal pattern**, suggesting distinct spending habits.  
- **Gender Distribution:** Slightly more females than males, balanced overall.

These findings indicated the potential for clear customer segmentation.

---

## ⚙️ Model Building

### **1. Feature Selection & Scaling**
Selected the most relevant features:
- `Annual Income (k$)`  
- `Spending Score (1-100)`

Features were standardized using **StandardScaler** to ensure proper distance-based clustering.

---

### **2. Determining Optimal Clusters (Elbow Method)**
The **Elbow Method** was used to identify the best number of clusters by plotting **WCSS (Within-Cluster Sum of Squares)** for different k values.

📈 The elbow point appeared at **k = 5**, indicating **five optimal clusters**.

---

### **3. Applying K-Means Clustering**
The model grouped customers into five distinct clusters based on income and spending score.

| Cluster | Annual Income (k$) | Spending Score | Segment Description |
|----------|--------------------|----------------|----------------------|
| **0** | 55.3 | 49.5 | Average customers |
| **1** | 86.5 | 82.1 | High-income, high-spending (Premium Customers) |
| **2** | 25.7 | 79.4 | Low-income, high-spending (Impulsive Shoppers) |
| **3** | 88.2 | 17.1 | High-income, low-spending (Cautious Buyers) |
| **4** | 26.3 | 20.9 | Low-income, low-spending (Budget Customers) |

---

## 📊 Cluster Visualization

The scatter plot below displays the five clusters and their **centroids** (black “X” markers):

- X-axis → Annual Income  
- Y-axis → Spending Score  
- Each color → Distinct customer segment  
- Black X → Cluster centroid (mean income and spending)

The clusters are **well-separated**, confirming that income and spending behavior naturally define customer types.

---

## 💡 Key Insights
- The customer base divides into **five unique behavioral segments**.  
- The **most profitable groups** are:
  - High-income, high-spending customers (Cluster 1)  
  - Low-income, high-spending customers (Cluster 2)  
- The **least active segments** (Clusters 3 and 4) represent customers who spend less, even with higher income.  
- Cluster 0 represents **average customers** with balanced habits.

---

## 🚀 Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)  
- **Jupyter Notebook** for analysis and visualization  
- **K-Means Clustering** from Scikit-learn  

---

## ✅ Conclusion
This project demonstrates how **unsupervised learning** can be used to uncover actionable insights from customer data.  
By segmenting customers into five groups, businesses can tailor their marketing strategies, offer personalized promotions, and enhance customer retention.  

K-Means proved to be an effective and interpretable method for identifying distinct customer behaviors within a simple dataset.

---
