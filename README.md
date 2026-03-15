# MSCS 634 Lab 5 – Clustering Techniques
---

Student: *Prakash Tamang*  
Course: **MSCS 634 – Advanced Data Mining**  
Lab: **Lab 5 – Clustering Techniques**

## Overview

This lab explores clustering techniques using the Wine dataset from the sklearn Python library. The goal is to understand how different clustering algorithms group similar observations and how parameter selection influences clustering outcomes.

Two clustering methods were implemented in this lab:

- Hierarchical Clustering (Agglomerative)
- DBSCAN (Density-Based Spatial Clustering)

The dataset features were standardized before applying the clustering algorithms to ensure fair distance comparisons.

---

## Dataset

The Wine dataset contains chemical analysis results of wines grown in the same region in Italy but derived from three different cultivars.

Dataset characteristics:

- 178 observations
- 13 numerical features
- Features include alcohol content, malic acid, magnesium, flavanoids, and other chemical measurements.

The dataset was explored using:

- `.head()`
- `.info()`
- `.describe()`

All features were standardized using **StandardScaler** before clustering.

---

## Hierarchical Clustering

Agglomerative Hierarchical Clustering was applied to the standardized dataset.

Key steps:

- The clustering algorithm grouped samples based on similarity.
- A scatter plot visualization was used to observe cluster formation.
- A **dendrogram** was generated to understand how clusters merge at different distance levels.

The dendrogram helped visualize the hierarchical relationships between observations and suggested reasonable cluster groupings.

---

## DBSCAN Clustering

DBSCAN clustering was applied to detect density-based clusters.

Different parameter values were tested:

- `eps`
- `min_samples`

Initial parameter values labeled most points as noise. Increasing the `eps` value allowed the algorithm to identify cluster regions.

A scatter plot visualization was used to observe cluster assignments and noise points.

---

## Clustering Evaluation Metrics

The following evaluation metrics were computed to assess clustering performance:

- **Silhouette Score**
- **Homogeneity Score**
- **Completeness Score**

These metrics help measure cluster separation and how well clusters align with the actual class labels in the dataset.

The results showed that DBSCAN did not produce highly distinct clusters for this dataset with the tested parameters.

---

## Key Insights

- Feature standardization is important for clustering algorithms that rely on distance measurements.
- Hierarchical clustering provided clearer cluster structures for this dataset.
- DBSCAN was highly sensitive to parameter selection and required tuning to detect clusters.
- Evaluation metrics indicated that DBSCAN clustering did not strongly match the actual dataset classes.

---

## Challenges

- Selecting appropriate DBSCAN parameters required experimentation.
- Visualizing high-dimensional data required selecting only two features for plotting.
- Interpreting clustering results required comparing algorithm behavior and evaluation metrics.

---

## Repository Contents

This repository contains:

- `Lab5_Clustering.ipynb` – Jupyter Notebook with all code, visualizations, and analysis
- `README.md` – Summary and explanation of the lab work