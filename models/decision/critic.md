# CRITIC Weighting

```yaml
id: critic
name: CRITIC Method
family: objective_weighting
aliases: [CRITIC, Criteria Importance Through Intercriteria Correlation]
tags:
  problem: [evaluation, decision, ranking]
  task: [weighting, indicator_evaluation]
  data: [tabular, multi_criteria]
  pattern: [dispersion, indicator_correlation]
  structure: [cross_sectional]
  scale: [small, medium, large]
  mathematics: [standardization, correlation, information_content]
  philosophy: [data_driven]
  output: [criteria_weights]
  prerequisites: [numeric_indicators, indicator_direction, correlation_estimation]
  competition: [common, evaluation_problem, formula_friendly]
  limitations: [correlation_measure_choice, scale_and_outlier_sensitivity]
  risks: [unstable_weights_with_small_samples, redundant_or_outlier_dominated_features]
  interpretability: [high, formula_interpretability]
applicability:
  hard_match: [objective_weighting, multiple_correlated_indicators]
  soft_match: [indicator_variability_is_informative]
  negative_match: [expert_preference_must_dominate]
parameters:
  - name: correlation_measure
    description: Inter-criteria correlation used to represent conflict/redundancy.
    selection: Pearson is common for continuous indicators; justify alternatives.
  - name: normalization
    description: Transformation before dispersion and correlation calculations.
    selection: Keep indicator direction and scale effects explicit.
validation: [weight_sensitivity, correlation_stability, outlier_sensitivity]
strengths: [uses_variability_and_conflict, captures_redundancy]
limitations: [statistical_relationships_do_not_equal_semantic_importance]
risks: [correlation_instability, outlier_influence]
interpretation:
  overall: high
  formula: high
  parameter: high
  feature: high
relations:
  complementary_to: [topsis, entropy_weight]
  alternative_to: [entropy_weight, ahp]
references: []
```

## Modeling note

CRITIC is useful when both indicator contrast and inter-indicator conflict should influence weights. It is a weighting module, not a complete evaluation model.