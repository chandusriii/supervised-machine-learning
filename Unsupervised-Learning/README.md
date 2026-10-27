# Unsupervised Learning: Clustering Guide

This guide accompanies the notebooks in `Unsupervised-Learning/`. It explains core concepts, practical trade-offs, and Scikit-learn APIs used in the examples.

> **Learning goal:** understand how clustering discovers structure in features without using known target labels during fitting. Iris species labels can be used after clustering for comparison, but must not be passed into `KMeans.fit` if the goal is to demonstrate unsupervised learning.

## 1. What is unsupervised learning?

Unsupervised learning works with observations whose target labels are not supplied to the algorithm. Clustering groups observations according to feature-space similarity. A cluster assignment is not automatically a meaningful real-world category.

Official guide: https://scikit-learn.org/stable/unsupervised_learning.html

## 2. K-Means

K-Means partitions observations into a chosen number of clusters, representing each cluster by a centroid. It repeatedly assigns observations to nearby centroids and updates the centroids to reduce within-cluster sum of squares (inertia).

```python
from sklearn.cluster import KMeans
from sklearn.datasets import load_iris
from sklearn.preprocessing import StandardScaler
from sklearn.pipeline import make_pipeline

iris = load_iris()
X = iris.data  # Only features are used to fit the clustering model

model = make_pipeline(
    StandardScaler(),
    KMeans(n_clusters=3, n_init=10, random_state=42),
)
cluster_ids = model.fit_predict(X)
```

Why scale? K-Means uses distances. A feature with a larger numeric range can dominate distance calculations unless features are on comparable scales. A pipeline ensures scaling is fitted and reused consistently.

Official reference: https://scikit-learn.org/stable/modules/clustering.html#k-means

### Inertia and the Elbow Method

`KMeans.inertia_` is the sum of squared distances from samples to their assigned centroid. Inertia cannot increase as K increases, so it should not be treated as a score to maximize. The elbow method plots inertia against candidate K values and looks for a point where additional clusters produce diminishing improvements. The elbow can be ambiguous and is not a guarantee of the best K.

```python
inertias = []
candidate_k = range(1, 11)

for k in candidate_k:
    model = make_pipeline(
        StandardScaler(),
        KMeans(n_clusters=k, n_init=10, random_state=42),
    )
    model.fit(X)
    inertias.append(model.named_steps['kmeans'].inertia_)
```

Official API: https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html

### Silhouette Score

The silhouette score compares within-cluster distance with distance to the nearest other cluster. It ranges from -1 to +1; higher values usually indicate better-separated clusters for the selected metric. It requires at least two clusters and fewer clusters than samples. Use it alongside plots and context.

Official API: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html

## 3. Hierarchical (Agglomerative) Clustering and Dendrograms

Agglomerative clustering begins with each sample as its own cluster and repeatedly merges clusters. The linkage criterion determines how between-cluster distances are computed:
- **Ward:** merges to minimize the increase in within-cluster variance; supports Euclidean distance.
- **Complete:** uses the maximum pairwise distance between clusters.
- **Average:** uses the average pairwise distance between clusters.
- **Single:** uses the minimum pairwise distance between clusters.

A dendrogram visualizes merge order and merge distances. Scikit-learn's `AgglomerativeClustering` estimates cluster labels, but does not itself draw a conventional dendrogram. The notebook uses SciPy's `linkage` and `dendrogram` for visualization.

Official Scikit-learn reference: https://scikit-learn.org/stable/modules/clustering.html#hierarchical-clustering

## 4. K-Means vs. Hierarchical Clustering

| Topic | K-Means | Agglomerative / Hierarchical |
|---|---|---|
| Number of clusters | Choose K before fitting | Choose a cluster count or inspect the hierarchy |
| Core idea | Repeated centroid assignment/update | Repeatedly merge the closest clusters by a linkage rule |
| Output | Flat partition and centroids | Flat labels; hierarchy can be inspected with a dendrogram |
| Scaling | Usually important because distances are used | Often important for distance-based linkage |
| Typical strength | Simple and efficient for compact, roughly convex clusters | Shows nested relationships and offers multiple linkage rules |
| Caveat | Sensitive to initialization and cluster geometry | May be more computationally expensive on large datasets |

Neither method is universally superior. Compare outputs and assumptions against the structure of the data.

## 5. DBSCAN

DBSCAN groups points in dense regions and labels points that do not meet the density criteria as noise (label `-1`). Unlike K-Means, it does not require a cluster count in advance and can identify arbitrarily shaped clusters.

Key parameters:
- `eps`: neighborhood radius.
- `min_samples`: number of nearby samples needed for a core point (including the point itself in Scikit-learn's convention).

Scaling and parameter choices strongly affect the outcome. If `eps` is too small, many points may be marked as noise; if too large, clusters may merge.

Official API: https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html

## 6. Evaluating clusters correctly

- Use inertia and the elbow plot to examine K-Means compactness across K values.
- Use silhouette scores to examine separation, while remembering they favor some cluster shapes over others.
- Visualize results and inspect the feature space.
- Compare clusters with Iris species only as a post-hoc educational check. Cluster IDs are arbitrary and do not directly correspond to species names.
- For DBSCAN, exclude noise points from some internal metrics where appropriate, and ensure at least two non-noise clusters remain before computing silhouette.

## 7. Official references

- Scikit-learn Unsupervised Learning: https://scikit-learn.org/stable/unsupervised_learning.html
- Clustering overview: https://scikit-learn.org/stable/modules/clustering.html
- K-Means API: https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html
- Silhouette score API: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html
- AgglomerativeClustering API: https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html
- DBSCAN API: https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html
- SciPy dendrogram API: https://docs.scipy.org/doc/scipy/reference/generated/scipy.cluster.hierarchy.dendrogram.html