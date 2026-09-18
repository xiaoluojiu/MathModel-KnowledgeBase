# Principal Component Analysis

**ID:** `pca`

## Summary
Linear dimensionality reduction that projects data onto orthogonal directions of maximal variance. It is useful for compression, visualization, denoising, and as preprocessing for downstream models.

## Tags
- problem: `dimensionality_reduction`, `visualization`, `feature_engineering`
- task: `dimensionality_reduction`, `feature_extraction`, `preprocessing`
- data: `tabular`, `structured`, `continuous`
- pattern: `correlation`, `redundancy`, `high_dimensionality`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`
- mathematics: `linear`, `matrix_factorization`, `variance_based`
- philosophy: `geometric`, `data_driven`
- output: `latent_representation`, `principal_components`, `explained_variance`
- competition: `very_common`, `visualization_friendly`, `preprocessing`

## Applicability
**Hard match:** numeric feature matrix.

**Soft match:** correlated features, high dimensionality, need for low-dimensional visualization or compact representations.

**Negative match:** categorical-only data without suitable encoding; situations where maximum variance is not aligned with the task objective.

## Parameters
- `n_components`: number of retained components.
- scaling/centering policy.

## Validation
Explained variance ratio, reconstruction error, downstream validation, component stability and domain interpretability.

## Strengths
- removes linear redundancy
- useful visualization and preprocessing tool
- computationally well understood

## Limitations / Risks
- components may be difficult to interpret
- unsupervised variance does not necessarily maximize predictive information
- scaling choices materially affect components

## Relations
- `preprocessing_for`: `linear-regression`, `svm`, `kmeans`
- `alternative_to`: `feature-selection`
- `complementary_to`: `lasso`

## References
- scikit-learn decomposition documentation: https://scikit-learn.org/stable/modules/decomposition.html
