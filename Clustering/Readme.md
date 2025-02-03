# Clustering Analysis: K-Means, DBSCAN, and Agglomerative Clustering

## Overview
This project involves two clustering tasks:
1. **Synthetic Data Clustering with K-Means**
2. **Comparative Analysis of K-Means, DBSCAN, and Agglomerative Clustering**

## Task 1: Clustering Synthetic Data using K-Means

### Data Generation
- Created synthetic data using `sklearn.datasets.make_blobs`
- Generated **500 samples** with **4 centers**

### Clustering Approach
- Applied **K-Means clustering**
- Evaluated clustering performance using:
  - **Silhouette Score**: `0.76`
  - **Adjusted Rand Index (ARI)`**
- Used the **Elbow Method** by plotting `k_means.inertia_` to determine the optimal number of clusters

### Results
- Achieved a well-separated clustering structure with high silhouette score
- The elbow plot suggested the optimal cluster number

---

## Task 2: Comparison of K-Means, DBSCAN, and Agglomerative Clustering

### Data Generation
Generated a custom dataset with circular patterns and noise using the following function:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

def PointsInCircum(r, n=100):
    return [(np.cos(2*np.pi/n*x)*r+np.random.normal(-30,30),
             np.sin(2*np.pi/n*x)*r+np.random.normal(-30,30)) for x in range(1,n+1)]

# Creating data points in the form of a circle
df = pd.DataFrame(PointsInCircum(500,1000))
df = df.append(PointsInCircum(300,700))
df = df.append(PointsInCircum(100,300))

# Adding noise to the dataset
df = df.append([(np.random.randint(-600,600),
               np.random.randint(-600,600)) for i in range(300)])

plt.figure(figsize=(7,7))
plt.scatter(df[0], df[1], s=2, color='grey')
plt.title('Dataset',fontsize=12)
plt.xlabel('Feature 1',fontsize=10)
```

### Clustering Methods Compared
1. **K-Means**
   - Assumes clusters are spherical
   - Struggles with non-linearly separable data
2. **DBSCAN**
   - Density-based clustering algorithm
   - Good for non-linear and noisy data
3. **Agglomerative Hierarchical Clustering**
   - Builds a hierarchy of clusters
   - Suitable for different cluster shapes
