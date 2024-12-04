# Unsupervised Learning

**Unsupervised learning** refers to a class of machine learning problems where the model is tasked with finding patterns or relationships in data without explicit guidance or labeled examples. Unlike in supervised learning problems, there are no targets $y_i$, and datasets consist of just feature vectors: $\mathcal D = \{\boldsymbol x_i\}_{i=1}^n$.

## Dimensionality Reduction

```{figure} https://buffml.com/wp-content/uploads/2022/12/Dimensionality_Reduction.png
---
align: center
height: 500px
---
```

Dimensionality reduction techniques transform high-dimensional data into a lower-dimensional representation while preserving important information. This is useful for:

- Visualization of high-dimensional data
- Reducing computational complexity
- Removing noise and redundant features
- Addressing the curse of dimensionality

Common techniques include:

- Principal Component Analysis (PCA)
- t-SNE (t-Distributed Stochastic Neighbor Embedding)
- UMAP (Uniform Manifold Approximation and Projection)

## Clustering

```{figure} https://media.licdn.com/dms/image/D4D12AQFdOCmVd8QVow/article-cover_image-shrink_720_1280/0/1680696595611?e=2147483647&v=beta&t=_BnRUyAeG4dxyHALQ0E48cL8pfvmGh7sUDxETG6LRoQ
---
align: center
height: 500px
---
```

Clustering algorithms group similar data points together based on their features or characteristics. Points within the same cluster should be similar to each other and different from points in other clusters.

Popular clustering algorithms:

- K-means clustering
- Hierarchical clustering
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- Gaussian Mixture Models

## Anomaly Detection

```{figure} https://www.quest.com/images/og/OGImage-AnomalyDetection_170064.jpg
---
align: center
---
```

Anomaly detection (also known as outlier detection) identifies data points that deviate significantly from the expected pattern or behavior. These anomalies might indicate:

- Fraud in financial transactions
- Manufacturing defects
- Network intrusions
- Sensor malfunctions

Common approaches:

- Statistical methods (z-score, IQR)
- Isolation Forest
- One-class SVM
- Autoencoders

## Association Rule Learning

```{figure} https://i0.wp.com/analyticsarora.com/wp-content/uploads/2022/06/association-rule-learning-visual-example-ml-interview.png?resize=800%2C600&ssl=1
---
align: center
---
```

Association rule learning discovers interesting relationships between variables in large datasets. It's particularly useful in:

- Market basket analysis
- Product recommendations
- Web usage mining
- Cross-selling strategies

**Popular algorithms:**

- Apriori algorithm
- FP-Growth
- ECLAT

## Topic Modeling

```{figure} https://d3lkc3n5th01x7.cloudfront.net/wp-content/uploads/2023/11/03043855/topic-modeling-in-NLP.svg
---
align: center
---
```

Topic modeling algorithms uncover abstract "topics" that occur in a collection of documents. Each topic is represented as a distribution over words, and each document as a mixture of topics.

Common techniques:

- Latent Dirichlet Allocation (LDA)
- Non-negative Matrix Factorization (NMF)
- Latent Semantic Analysis (LSA)

Applications:

- Content recommendation
- Document summarization
- Trend analysis
- Content organization
