# 2025 CUMCM B060 — Evidence Card

> 状态：正文 OCR 已核验；模型标签依据论文正文，不把历史使用等同于当前题目推荐。

## Source

- Official showcase: https://dxs.moe.gov.cn/zx/a/hd_sxjm_sxjmlw_2025qgdxssxjmjslwzs_2025btlw/251101/2022733.shtml
- OCR text mirror: https://github.com/yushugulao/CUMCM-Archive/blob/main/research_index/pdf_text/2025/B/优秀论文/B060--4abe934b8f.md
- Pages: 72

## Problem pattern

`physical_measurement + spectroscopy + inverse_problem + parameter_estimation + interference`

## Data pattern

`reflectance_spectrum + wavenumber + multiple_incidence_angles + experimental_measurement`

## Explicitly evidenced methods

### Mechanistic / physical model
- Drude refractive-index model
- Fresnel reflection formulation
- Two-beam interference model
- Multi-beam interference / Airy-type correction

### Parameter estimation / numerical methods
- Newton iteration for inverse parameter estimation
- Grid search for initial value selection
- Nonlinear fitting / residual-square objective
- Cubic spline interpolation for spectral extrema
- Statistical aggregation of multiple thickness estimates

### Validation / uncertainty
- Standard deviation
- Confidence interval
- Coefficient of variation
- Cross-validation of two independent thickness inversion routes
- Multi-beam significance indicator `G`
- Machine-learning-assisted check of multi-beam influence

## Method roles

| Method | Role | Tags |
|---|---|---|
| Drude | physical parameter/refractive-index model | `mechanistic`, `physics`, `material`, `refractive_index` |
| Fresnel | optical forward model | `mechanistic`, `optics`, `reflection` |
| Two-beam interference | forward measurement model | `wave_interference`, `spectroscopy`, `physics` |
| Newton iteration | inverse solver | `root_finding`, `parameter_estimation`, `local_solver` |
| Grid search | initialization | `initialization`, `global_scan` |
| Cubic spline | feature/extrema extraction | `interpolation`, `signal_processing` |
| Multi-beam/Airy | model correction | `model_refinement`, `interference` |
| Statistical aggregation | uncertainty/reliability | `uncertainty`, `confidence_interval` |

## Key modeling insight

This case should not be indexed as merely a "Newton iteration problem". The dominant pattern is:

`physical forward model -> measured spectrum -> inverse parameter estimation -> independent cross-check -> model-error diagnosis -> physical model correction`.

## Historical route graph

```text
Drude refractive index
        ↓
Fresnel + two-beam interference
        ↓
reflectance spectrum
   ┌────┴─────────────┐
   ↓                  ↓
periodic minima       Newton inverse fitting
   ↓                  ↓
spline interpolation  grid initialization
   ↓                  ↓
thickness estimate ←→ thickness estimate
          ↓
 statistical reliability
          ↓
 multi-beam effect diagnosis
          ↓
 Airy / multi-beam correction
```

## Negative / caution knowledge

- Newton iteration is a solver, not the underlying mathematical model.
- Periodic-minimum extraction is a data-derived estimator and depends on reliable extrema detection.
- A physical correction should be introduced when evidence indicates model discrepancy; do not automatically upgrade every case to a multi-beam model.
- Machine learning is reported as a verification/diagnostic component in this paper; it should not be treated as the primary physical model without additional evidence.

## Retrieval tags

`cumcm_2025` `B` `physics` `optics` `spectroscopy` `thin_film` `interference` `refractive_index` `Drude` `Fresnel` `inverse_problem` `parameter_estimation` `Newton_iteration` `grid_search` `spline_interpolation` `uncertainty` `model_correction` `Airy` `multi_beam`
