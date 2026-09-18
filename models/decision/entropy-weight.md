# Entropy Weight Method

```yaml
id: entropy_weight
name: Entropy Weight Method
family: objective_weighting
aliases: [Entropy Weight, 熵权法]
tags:
  problem: [evaluation, decision, ranking]
  task: [weighting, indicator_evaluation]
  data: [tabular, multi_criteria]
  pattern: [dispersion_across_alternatives]
  structure: [cross_sectional]
  scale: [small, medium, large]
  mathematics: [information_entropy, normalization]
  philosophy: [data_driven]
  output: [criteria_weights]
  prerequisites: [comparable_indicators, indicator_direction]
  competition: [very_common, evaluation_problem, formula_friendly]
  limitations: [not_semantic_importance, sensitive_to_normalization]
  risks: [near_constant_indicator, redundant_information]
  interpretability: [high, formula_interpretability]
applicability:
  hard_match: [objective_weighting_from_observed_data]
  soft_match: [multiple_alternatives, measurable_indicator_variation]
  negative_match: [expert_preference_is_the_primary_information_source]
parameters:
  - name: normalization
    description: Indicator normalization before entropy calculation.
    selection: Preserve benefit/cost semantics and document zero handling.
validation: [weight_sensitivity, redundancy_check, normalization_sensitivity]
strengths: [objective_data_driven_weighting, easy_to_combine_with_ranking_methods]
limitations: [dispersion_is_not_the_same_as_real_world_importance]
risks: [unstable_weights_when_indicators_have_extreme_values]
interpretation:
  overall: high
  formula: high
  parameter: high
  feature: high
relations:
  complementary_to: [topsis, ahp, critic]
  alternative_to: [ahp, critic]
references: []
```

## Modeling note

Entropy weighting estimates weights from the information/dispersion structure of the observed alternatives. It should not be described as universally "objective"; the result is objective relative to the chosen data transformation and entropy construction.