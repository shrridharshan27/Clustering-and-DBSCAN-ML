# ML Lab 06: Unsupervised Clustering & DBSCAN

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E.svg?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-013243.svg?logo=numpy&logoColor=white)](https://numpy.org/)

---

## Academic Details
- **Student Name:** Shrri Dharshan D R
- **Register Number:** 23BPS1090
- **Course Code:** BCSE209P
- **Course Title:** Machine Learning Laboratory
- **Faculty:** Dr. S. Shridevi
- **Institution:** School of Computer Science and Engineering (SCOPE), VIT Chennai

---

## Overview
This repository contains laboratory implementations and empirical comparative studies of **Unsupervised Clustering Algorithms** and **Density-Based Spatial Clustering (DBSCAN)** across high-dimensional real-world time-series datasets from the UCI Machine Learning Repository.

The laboratory explores centroid-based clustering (K-Means), hierarchical clustering paradigms (Agglomerative bottom-up and Divisive top-down), exemplar-based clustering (K-Medoids / PAM), and density-based non-linear cluster discovery (DBSCAN with noise point detection).

---

## Experiments & Datasets

### 1. Clustering — Electricity Load Diagrams (2011–2014)
- **Dataset:** ElectricityLoadDiagrams 2011–2014 Dataset ([UCI ID: 321](https://archive.ics.uci.edu/dataset/321))
- **Objective:** Group 370 electricity clients based on consumption patterns and daily/hourly demand profiles.
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb)
- **Algorithms:** K-Means (Elbow method with inertia, PCA 2D projections), Agglomerative Hierarchical Clustering (Ward linkage, dendrograms), Divisive Hierarchical Clustering, K-Medoids (Partitioning Around Medoids), and DBSCAN.

### 2. Clustering — Weekly Sales Transactions
- **Dataset:** Sales Transactions Dataset Weekly ([UCI ID: 396](https://archive.ics.uci.edu/dataset/396))
- **Objective:** Discover natural product groupings based on normalized weekly sales trajectories across 811 products over 52 weeks.
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb)
- **Algorithms:** K-Means, Agglomerative Clustering, Divisive Clustering, K-Medoids, and DBSCAN.

### 3. DBSCAN — Electricity Load Diagrams
- **Dataset:** ElectricityLoadDiagrams 2011–2014 ([UCI ID: 321](https://archive.ics.uci.edu/dataset/321))
- **Objective:** Identify arbitrarily shaped load density profiles and detect anomalous/outlier clients.
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb)
- **Output Results:** [DBSCAN_ElectricityLoad_Results.csv](./DBSCAN_ElectricityLoad_Results.csv)
- **Techniques:** Epsilon ($\epsilon$) and $min\_samples$ parameter sweep, core vs. border vs. noise point classification, and Silhouette coefficient evaluation.

### 4. DBSCAN — Weekly Sales Transactions
- **Dataset:** Sales Transactions Dataset Weekly ([UCI ID: 396](https://archive.ics.uci.edu/dataset/396))
- **Objective:** Segment products according to demand stability and isolate irregular/sporadic sales behaviors.
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb)
- **Output Results:** [DBSCAN_SalesTransactions_Results.csv](./DBSCAN_SalesTransactions_Results.csv)
- **Techniques:** High-dimensional distance matrices, noise point filtering, and cluster silhouette scoring.

---

## Evaluation Metrics
Unsupervised clustering performance is evaluated using:
- **Silhouette Coefficient:** Measures cohesion within clusters vs. separation between clusters (range: $[-1, 1]$).
- **Elbow Method & Inertia:** Within-cluster sum-of-squares (WCSS) to determine optimal cluster counts ($k$).
- **Dendrogram Visualization:** Visualizing hierarchical tree structures and distance cophenetic thresholds.
- **Noise Ratio:** Proportion of unassigned outlier/noise points identified by DBSCAN.

---

## Repository Structure
```text
ML-Lab-06-Clustering-and-DBSCAN/
├── 23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb
├── DBSCAN_ElectricityLoad_Results.csv
├── DBSCAN_SalesTransactions_Results.csv
├── electricity_data/
├── sales_transactions_data/
├── .gitignore
└── README.md
```

---

## How to Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com/shrridharshan27/ML-Lab-06-Clustering-and-DBSCAN.git
   cd ML-Lab-06-Clustering-and-DBSCAN
   ```
2. **Install dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn scipy ucimlrepo jupyter
   ```
3. **Dataset Setup:**
   - The notebooks automatically fetch and extract datasets from the official UCI Machine Learning Repository at runtime using `ucimlrepo` or fallback direct download.
4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
