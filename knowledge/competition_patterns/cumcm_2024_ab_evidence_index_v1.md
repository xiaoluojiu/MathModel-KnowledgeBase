# CUMCM 2024 A/B Evidence Index v1

## Official paper corpus

The official China University Student Online corpus provides individual image-page publications for 2024 A and B papers. Verified A examples include A016, A053, A163, A178, and A242. A dedicated 2024 B-paper index is also available.

Official sources:
- 2024 A-paper index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2024qgdxssxjmjslwzs/2024atlw/
- 2024 B-paper index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2024qgdxssxjmjslwzs/2024btlw/

## Evidence handling

The publication pages expose paper pages as images. Therefore a model is not marked `method_verified` merely because a search result, title, or third-party summary mentions it. Verification requires reading the relevant paper page(s), equations, tables, or algorithm descriptions.

## Extraction target

For every selected A/B paper:

- competition year / problem
- paper ID
- source URL
- page count if observable
- subproblem decomposition
- input/output variables
- data pattern
- assumptions
- governing equations
- statistical models
- optimization models
- algorithms/solvers
- parameter estimation
- validation
- sensitivity/robustness
- model limitations
- alternative routes
- reusable problem-pattern tags
- model-card relation IDs

## Relation types

`historical_usage`, `supports`, `alternative_to`, `composed_with`, `requires`, `validates`, `negative_evidence`, `pattern_instance_of`.

## Priority

Continue 2024 A/B in parallel with 2023/2022 extraction. Prefer official displayed papers and official expert commentary; use third-party material only as discovery evidence unless independently verified.
