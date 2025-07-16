# 🧠 Customer Segmentation using Clustering

This project performs customer segmentation using clustering algorithms. The goal is to group customers based on their characteristics and behaviors, providing insights for targeted marketing, service personalization, and relationship management.

## 📌 Objectives

1. Segment customers into distinct groups using clustering techniques.
2. Derive actionable insights from each segment for business strategy.
3. Identify the best clustering model for this dataset.

---

## 📥 Dataset

- **Source**: [Kaggle - Automobile Customer Data](https://www.kaggle.com/datasets/akashdeepkuila/automobile-customer/data)
- **Size**: 10,695 records, 10 columns
- **Features**:  
  - `CustomerID`, `Age`, `Gender`, `Profession`, `SpendingScore`, `Family_Size`, `WorkExperience`, `Married`, `Graduated`, `Category`

---

## 🛠️ Data Preparation

- **Missing Values**: 2,108
- **Duplicates**: 136
- **Steps**:
  - Drop `CustomerID` and `Category` columns
  - Fill nulls: median for numeric, mode for categorical
  - Remove duplicates and outliers
  - Encode categorical values numerically

---

## 📊 Exploratory Data Analysis (EDA)

Performed EDA to understand the distribution and relationships between features. Outlier detection and normalization were also conducted.

---

## 🤖 Clustering Models

Used three clustering algorithms:
1. **K-Means Clustering**
2. **Agglomerative Clustering** ✅ *(Best Silhouette Score)*
3. **DBSCAN Clustering**

### 🔍 Cluster Evaluation

- **Elbow Method** suggested **k = 3**
- **Silhouette Score** suggested **k = 2**, but **k = 3** was chosen for better interpretability.

---

## 🧬 Cluster Insights (Agglomerative Clustering)

### Cluster 1:
- **Gender**: 51% Male / 49% Female
- **Age**: Mean 32 yrs (mostly 37)
- **Married**: 57% Yes
- **Graduated**: 56% Yes
- **Profession**: Mostly Artist
- **Spending Score**: Mostly Low
- **Family Size**: Mostly 2

### Cluster 2:
- **Gender**: 56% Male
- **Age**: Mean 47–54 yrs
- **Married**: 86% Yes
- **Graduated**: 74% Yes
- **Profession**: Mostly Artist
- **Spending Score**: Low to Average
- **Family Size**: Mostly 2

### Cluster 3:
- **Gender**: 60% Male
- **Age**: Mean 73–80 yrs
- **Married**: 94% Yes
- **Graduated**: 63% Yes
- **Profession**: Mostly Lawyer
- **Spending Score**: Mostly Low, Mean High
- **Family Size**: Mostly 2

---

## 📈 Conclusion

Agglomerative Clustering with **3 clusters** provides the best segmentation and interpretability. Each cluster presents a unique customer profile, enabling strategic marketing and service personalization.

---

## 📂 Project Structure

📦 customer-segmentation/n
├── 📁 data/n
├── 📁 notebooks/n
├── 📁 models/n
├── 📄 README.md/n
├── 📄 requirements.txt/n
└── 📄 clustering.ipynb/n

---
