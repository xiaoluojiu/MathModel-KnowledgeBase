# CUMCM 2025 A/B Evidence Cards

> Scope: 2025 A/B only. This file separates verified public evidence from later pattern inference.

## Source registry

- Official competition site: https://www.mcm.edu.cn/
- Official paper-display index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/qkt_sxjm_lw_lwzs.shtml
- 2025 paper display index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2025qgdxssxjmjslwzs/
- 2025 A paper page: https://dxs.moe.gov.cn/zx/a/hd_sxjm_sxjmlw_2025qgdxssxjmjslwzs_2025atlw/251101/2022729.shtml
- 2025 B paper index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2025qgdxssxjmjslwzs/2025btlw/
- 2025 B paper B060: https://dxs.moe.gov.cn/zx/a/hd_sxjm_sxjmlw_2025qgdxssxjmjslwzs_2025btlw/251101/2022733.shtml
- 2025 B paper B157: https://dxs.moe.gov.cn/zx/a/hd_sxjm_sxjmlw_2025qgdxssxjmjslwzs_2025btlw/251107/2023197.shtml

## 2025A — 烟幕干扰弹的投放策略

### Verified competition metadata

- Problem: A
- Year: 2025
- Officially described by the competition organization as “烟幕干扰弹的投放策略”.
- Domain: defense / trajectory planning / optimization.
- The official 2025 award announcement identifies A as one of the undergraduate problems.

### Evidence status

- `official_problem`: verified
- `paper_display`: verified; official public display includes paper A196.
- `full_paper_text`: not treated as machine-extracted here because the official page exposes page images rather than a text PDF in the retrieved result.

### High-confidence problem-pattern hypotheses

These are structural hypotheses, NOT claims about A196's exact method:

- projectile/trajectory modeling
- spatial geometry
- kinematics
- line-of-sight / occlusion geometry
- constrained optimization
- deployment timing / position decision
- numerical simulation

### Candidate model families for retrieval

- mechanistic kinematics model
- geometric visibility / coverage model
- nonlinear constrained optimization
- numerical search / simulation
- global heuristic optimization as an alternative when the objective is nonconvex

### Negative checks

Do not select a generic regression model merely because the input is tabular. First determine whether the problem is primarily mechanism-based and decision/optimization based.

Do not treat “genetic algorithm” as the problem itself. It is a possible solver for an optimization formulation.

## 2025B — 碳化硅外延层厚度的确定

### Verified competition metadata

- Problem: B
- Year: 2025
- Officially described by the competition organization as “碳化硅外延层厚度的确定”.
- Domain: semiconductor measurement / optics / inverse problem.
- The official 2025 award announcement identifies B as one of the undergraduate problems.

### Evidence status

- `official_problem`: verified
- `paper_display`: verified; official public display includes at least B060 and B157.
- `full_paper_text`: not treated as machine-extracted here because the official display pages expose paper pages as images.

### High-confidence problem-pattern hypotheses

- physical measurement
- signal processing
- inverse modeling
- parameter estimation
- interference / spectral structure
- nonlinear fitting
- model validation

### Candidate model families for retrieval

- mechanistic optical/interference model
- Fourier/spectral analysis for signal feature extraction
- nonlinear least squares / constrained parameter estimation
- robust fitting / uncertainty analysis as supporting methods

### Negative checks

Do not classify the task as ordinary supervised regression unless the problem formulation actually supplies an appropriate labeled training set.

Do not treat FFT as the final physical model. It can be a feature/initialization tool inside a larger inverse-modeling pipeline.

## AI retrieval rules derived from these cases

1. `historical_usage` must be supported by the actual paper text or another high-quality source.
2. `pattern_inference` must be stored separately from `historical_usage`.
3. Solver and model must be separate entities: e.g. nonlinear least squares is a solver/estimation procedure, while the physical interference equation is the mechanism model.
4. A model used by one displayed paper is not automatically a recommendation for a new problem.
5. When paper text is image-only, record the evidence state instead of hallucinating extracted equations.

## Next extraction target

The next pass should retrieve and OCR/inspect the individual 2025 A/B paper page images where permitted, then populate:

- exact subproblem-to-model mapping
- exact equations/model names
- parameter estimation method
- objective function
- constraints
- validation metrics
- sensitivity/robustness
- paper-specific alternatives

Only after that should the extracted methods be promoted to `historical_usage` edges in the model graph.
