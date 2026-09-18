# AI Retrieval Strategy v1

## 1. Purpose

The knowledge base does not replace the reasoning model. It supplies structured evidence so an AI can move from **problem + data profile** to a small, defensible candidate set.

## 2. Input contract

The AI should extract a normalized problem/data profile before searching:

```yaml
problem:
  primary: []
  secondary: []
task: []
data:
  type: []
  scale: []
  target: []
pattern: []
structure: []
objective: []
constraints: []
competition_context: []
known_limitations: []
```

The data profile can come from a separate data-analysis report; the raw dataset does not need to be uploaded to the knowledge base.

## 3. Retrieval stages

### Stage A — Hard filtering

Remove models whose required structure is contradicted by the problem/data profile.

Examples:
- a shortest-path algorithm requires a graph representation;
- Dijkstra requires nonnegative edge weights;
- a time-series model requires an ordered temporal target;
- a binary classifier requires a classification target.

### Stage B — Soft matching

Retrieve models matching:
- problem type;
- task;
- data type;
- statistical/data pattern;
- mathematical structure;
- competition context.

### Stage C — Prerequisite check

For each candidate, inspect its `prerequisites`. If the required evidence is absent, the AI should say **unknown / needs verification**, not silently assume it.

### Stage D — Negative evidence

Apply `negative_match`, limitations and risks. A model can be a mathematically valid candidate while still being a poor practical candidate because of small sample size, extrapolation, computational cost, interpretability requirements, or incompatible constraints.

### Stage E — Candidate collision

Prefer a small candidate set, normally 2 models. Candidates should be structurally different enough to make the comparison informative. Typical pairings include:

- interpretable statistical model vs nonlinear machine-learning model;
- exact optimization vs metaheuristic;
- expert-weighted decision method vs objective weighting method;
- mechanistic model vs empirical model.

Do not select two nearly identical variants unless the distinction matters for the problem.

## 4. Collision report

The AI should produce:

```yaml
candidate_a:
  model: ...
  matching_evidence: []
  negative_evidence: []
  prerequisites_to_verify: []

candidate_b:
  model: ...
  matching_evidence: []
  negative_evidence: []
  prerequisites_to_verify: []

comparison:
  structural_difference: ...
  data_fit_difference: ...
  interpretability_difference: ...
  validation_difference: ...
  competition_difference: ...

recommendation:
  primary_role: ...
  secondary_role: ...
  uncertainty: ...
```

The final recommendation must remain an AI judgment based on the retrieved evidence; the knowledge base itself should not encode a universal winner.

## 5. Evidence hierarchy

1. Problem statement facts supplied by the user.
2. Data-analysis report supplied by the user.
3. Model-card prerequisites and limitations.
4. Official mathematical/software documentation.
5. Peer-reviewed or authoritative references.
6. Competition examples and community practice.

The AI should distinguish evidence from inference.

## 6. Validation guidance

A model recommendation is incomplete without a validation plan. The AI should retrieve or infer suitable validation methods, such as holdout/time-series backtesting, residual diagnostics, feasibility checks, sensitivity analysis, repeated random seeds, or robustness checks.

For supervised machine learning, model selection and evaluation should use task-appropriate metrics and validation rather than training-set fit alone. scikit-learn explicitly separates cross-validation, hyperparameter tuning and scoring in its model-selection guidance. For ARIMA-family models, statsmodels documents ARIMA/SARIMAX as time-series models with exogenous and seasonal extensions and provides residual/forecasting workflows.

## 7. No fabricated evidence

If a model card does not contain a fact, the AI must not invent it and present it as knowledge-base evidence. It should mark the item as requiring external verification.
