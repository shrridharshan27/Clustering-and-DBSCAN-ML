# Unsupervised Clustering & DBSCAN Density Profiling

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E.svg?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-013243.svg?logo=numpy&logoColor=white)](https://numpy.org/)
[![Git LFS](https://img.shields.io/badge/Git%20LFS-Tracked-informational.svg)](https://git-lfs.github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Author
- **Shrri Dharshan D R** — [@shrridharshan27](https://github.com/shrridharshan27)

---

## Overview
This repository contains implementations and comparative studies of **Unsupervised Clustering Algorithms** and **Density-Based Spatial Clustering of Applications with Noise (DBSCAN)** across high-dimensional time-series benchmark datasets from the UCI Machine Learning Repository.

The project evaluates centroid clustering (K-Means with inertia elbow analysis), hierarchical clustering (Agglomerative bottom-up and Divisive top-down with dendrogram visualization), exemplar clustering (K-Medoids / Partitioning Around Medoids), and non-linear density clustering (DBSCAN with core, border, and noise point isolation).

---

## Project Modules & Datasets

### 1. Unsupervised Clustering — Electricity Load Diagrams (2011–2014)
- **Dataset:** ElectricityLoadDiagrams 2011–2014 Dataset ([UCI ID: 321](https://archive.ics.uci.edu/dataset/321))
- **Objective:** Segment 370 client electricity load profiles based on high-frequency consumption patterns.
- **Notebook:** [`23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb`](./23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb)
- **Methodology:** K-Means (Elbow method with PCA 2D projections), Agglomerative Hierarchical (Ward linkage, dendrograms), Divisive Hierarchical, and K-Medoids.

### 2. Unsupervised Clustering — Weekly Sales Transactions
- **Dataset:** Sales Transactions Dataset Weekly ([UCI ID: 396](https://archive.ics.uci.edu/dataset/396))
- **Objective:** Discover natural product groupings based on 52-week normalized sales trajectories across 811 products.
- **Notebook:** [`23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb`](./23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb)
- **Methodology:** Centroid, hierarchical, and exemplar clustering across 52-week normalized sales curves.

### 3. DBSCAN Density Clustering — Electricity Load Diagrams
- **Dataset:** ElectricityLoadDiagrams 2011–2014 ([UCI ID: 321](https://archive.ics.uci.edu/dataset/321))
- **Objective:** Identify non-spherical consumption patterns and isolate anomalous demand clients.
- **Notebook:** [`23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb`](./23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb)
- **Results:** [`DBSCAN_ElectricityLoad_Results.csv`](./DBSCAN_ElectricityLoad_Results.csv)
- **Methodology:** Epsilon ($\epsilon$) and $min\_samples$ parameter sweep, core vs. border vs. noise classification, Silhouette analysis.

### 4. DBSCAN Density Clustering — Weekly Sales Transactions
- **Dataset:** Sales Transactions Dataset Weekly ([UCI ID: 396](https://archive.ics.uci.edu/dataset/396))
- **Objective:** Segment products according to demand stability and isolate irregular sales profiles.
- **Notebook:** [`23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb`](./23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb)
- **Results:** [`DBSCAN_SalesTransactions_Results.csv`](./DBSCAN_SalesTransactions_Results.csv)
- **Methodology:** Pairwise distance matrices, outlier noise detection, and cluster silhouette scoring.

---

## Evaluation Metrics
- **Silhouette Coefficient:** Intra-cluster cohesion vs. nearest-cluster separation.
- **Inertia / WCSS (Within-Cluster Sum-of-Squares):** Elbow curves for optimal $k$.
- **Cophenetic Correlation & Dendrogram Analysis:** Validating hierarchical linkage structures.
- **Noise Ratio:** Percentage of unassigned noise points detected by DBSCAN.

---

## Project Structure
```text
Clustering-and-DBSCAN-ML/
├── 23BPS1090_ShrriDharshan_ML_Lab_Clustering_ElectricityLoad.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_Clustering_SalesWeekly.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_ElectricityLoad.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_DBSCAN_SalesTransactions.ipynb
├── DBSCAN_ElectricityLoad_Results.csv
├── DBSCAN_SalesTransactions_Results.csv
├── electricity_data/
├── sales_transactions_data/
├── .gitattributes
├── .gitignore
└── README.md
```

---

## Quickstart & Setup
1. **Clone the repository (with Git LFS):**
   ```bash
   git clone https://github.com/shrridharshan27/Clustering-and-DBSCAN-ML.git
   cd Clustering-and-DBSCAN-ML
   ```
2. **Install requirements:**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn scipy ucimlrepo jupyter
   ```
3. **Run the notebooks:**
   ```bash
   jupyter notebook
   ```

---

## License
Distributed under the [MIT License](https://opensource.org/licenses/MIT).
