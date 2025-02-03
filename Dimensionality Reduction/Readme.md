# Dimensionality Reduction and Classification on MNIST Dataset

## Overview
This project applies various dimensionality reduction techniques to the MNIST dataset and evaluates their impact on classification performance using a Random Forest classifier. The goal is to compare results on the original high-dimensional data and the reduced representations obtained via PCA, UMAP, t-SNE, and LDA.

## Key Features
- Load and visualize the MNIST dataset.
- Apply Principal Component Analysis (PCA) to reduce dimensionality.
- Train a Random Forest classifier on both the original and PCA-reduced data.
- Use additional dimensionality reduction techniques: UMAP, t-SNE, and LDA.
- Compare the classification results before and after dimensionality reduction.

## Implementation Steps

### 1. Load and Preprocess MNIST Data
- Fetch the MNIST dataset from OpenML.
- Convert the data into NumPy arrays and ensure labels are integers.

### 2. Visualize Sample Images
- Display sample images from the dataset to understand their structure.
- Use Matplotlib to plot grayscale images with corresponding labels.

### 3. Dimensionality Reduction Methods
- **PCA (Principal Component Analysis)**
  - Reduce the dimensionality of the MNIST dataset.
  - Retain significant variance while reducing the feature space.
  
- **UMAP (Uniform Manifold Approximation and Projection)**
  - Capture the global and local structure of the data efficiently.
  
- **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
  - Useful for visualizing high-dimensional data in 2D or 3D.
  
- **LDA (Linear Discriminant Analysis)**
  - A supervised dimensionality reduction technique that maximizes class separability.

### 4. Classification using Random Forest
- Train a Random Forest model on both the original and reduced feature sets.
- Evaluate and compare the classification performance on different feature spaces.

## Expected Output
- **Visualization of MNIST samples** before applying dimensionality reduction.
- **Plots of reduced data representations** (PCA, UMAP, t-SNE, LDA).
- **Classification results** comparing accuracy before and after dimensionality reduction.

## Libraries Used
- **Scikit-learn**: For dataset loading, PCA, LDA, and classification.
- **UMAP-learn**: For non-linear dimensionality reduction.
- **Matplotlib & Seaborn**: For data visualization.
- **NumPy & Pandas**: For numerical and data processing.

## Conclusion
This project demonstrates the effectiveness of different dimensionality reduction techniques in reducing computation while maintaining classification accuracy. The results highlight the trade-offs between feature space reduction and predictive performance.
