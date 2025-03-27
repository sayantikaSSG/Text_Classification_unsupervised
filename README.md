# 📌 K-Means Clustering on Bag-of-Words Dataset

## 📖 Overview
This project implements **K-Means clustering** on three different text datasets:
- **KOS**
- **NIPS**
- **ENRON**

The goal is to analyze document similarities based on word occurrences and determine optimal clusters using the **elbow method**.

---
## ⚙️ Methodology & Steps

### 1️⃣ Data Preprocessing
- Read the dataset and extract **Doc_ID, Word_ID, and Word_Count**.
- Created a **sparse matrix** with **Word_IDs as rows** and **Doc_IDs as columns**, marking word occurrences.

### 2️⃣ Jaccard Similarity Calculation
- Computed the **Jaccard Index** between documents to create a **symmetric similarity matrix**.

### 3️⃣ K-Means Clustering
- Applied **K-Means clustering** with different cluster sizes.
- Used the **elbow method** (inertia vs. clusters plot) to determine the optimal number of clusters.
- **Optimal Clusters Identified:**
  - **KOS:** 2 clusters
  - **NIPS:** 4 clusters
  - **ENRON:** Required **stratified sampling (1%)**, but a clear elbow point was not observed.

### 4️⃣ Dimensionality Reduction & Visualization
- Applied **dimension reduction** techniques for **3D visualization** of clusters.
- Assigned **Doc_IDs to respective clusters** and stored them in a dictionary format.

---
## 📊 Performance Metrics (1% Sample of ENRON Dataset)

| **Performance Measure** | **KOS** | **NIPS** | **ENRON** (1%) |
|------------------------|--------|--------|-------------|
| **Time Taken (s)**      | 128.02  | 51.86   | 3962.09      |
| **Space Required (MiB)** | 726.61  | 582.61  | 5115.92      |

---
## 🎯 Key Takeaways
✅ **KOS & NIPS datasets** showed clear cluster formations, making K-Means effective.  
✅ **ENRON dataset** required **stratified sampling**, but clustering was inconclusive due to an unclear elbow point.  
✅ **Dimensionality reduction** helped visualize document similarities in 3D space.  

---
