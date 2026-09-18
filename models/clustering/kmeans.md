# K-Means Clustering

**ID:** `kmeans`

## Summary
Centroid-based unsupervised clustering that partitions observations into K groups by minimizing within-cluster squared distances.

## Tags
- problem: `clustering`, `pattern_discovery`
- task: `clustering`, `segmentation`
- data: `tabular`, `structured`, `continuous`
- pattern: `cluster_structure`, `approximately_spherical_clusters`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`
- mathematics: `distance_based`, `optimization_based`, `nonparametric`
- philosophy: `geometric`, `data_driven`
- output: `cluster_label`, `cluster_centroid`
- competition: `very_common`, `visualization_friendly`, `easy_to_explain`

## Applicability
**Hard match:** unlabeled observations represented in a numeric feature space.

**Soft match:** roughly compact, convex/isotropic clusters under a meaningful distance; K can be estimated with diagnostics.

**Negative match:** strongly non-convex clusters, severe scale mismatch, or categorical-only variables without an appropriate distance representation.

## Parameters
- `n_clusters`: number of clusters.
- initialization strategy and number of restarts.
- maximum iterations and convergence tolerance.

## Validation
Silhouette score, Calinski-Harabasz, Davies-Bouldin, stability across initializations, and domain interpretation. The choice of K should not rely on one metric alone.

## Strengths
- simple and fast
- easy to visualize and explain
- scalable to large sample sizes in suitable settings

## Limitations / Risks
- requires K
- sensitive to scaling and initialization
- assumes a particular geometry; inertia can favor compact spherical clusters

## Relations
- `alternative_to`: `dbscan`, `hierarchical-clustering`, `spectral-clustering`

## References
- scikit-learn clustering documentation: https://scikit-learn.org/stable/modules/clustering.html
