# TOPSIS

```yaml
id: topsis
name: Technique for Order Preference by Similarity to Ideal Solution
family: multi_criteria_decision
aliases: [TOPSIS, 理想解法]
tags:
  problem: [evaluation, ranking, decision, selection]
  task: [ranking, scoring, multi_criteria_decision]
  data: [tabular, multi_criteria]
  pattern: [competing_criteria, positive_and_negative_indicators]
  structure: [cross_sectional]
  scale: [small, medium, large]
  objective: [maximize_benefit, minimize_cost]
  constraints: [criterion_direction]
  mathematics: [distance_based, normalization, ideal_solution]
  philosophy: [decision_analysis]
  output: [score, ranking, closeness_coefficient]
  prerequisites: [indicator_direction, normalization_rule, weights]
  competition: [very_common, evaluation_problem, ranking_problem, formula_friendly]
  limitations: [normalization_sensitivity, weight_sensitivity]
  risks: [rank_reversal, correlated_indicators]
  interpretability: [high, formula_interpretability]
applicability:
  hard_match: [multi_criteria_evaluation, alternatives_and_indicators]
  soft_match: [known_or_estimable_weights, benefit_and_cost_indicators]
  negative_match: [pure_time_series_forecasting, problems_without_comparable_alternatives]
parameters:
  - name: weights
    description: Importance weights for indicators.
    selection: Obtain from justified methods such as AHP, entropy weight or CRITIC.
  - name: normalization
    description: Transformation that makes indicators comparable.
    selection: Match the normalization to indicator semantics and document it.
validation: [weight_sensitivity, normalization_sensitivity, rank_stability]
strengths: [simple, transparent, naturally handles benefit_and_cost indicators]
limitations: [depends_on_weights, normalization_choice_matters]
risks: [rank_instability, redundant_indicators]
interpretation:
  overall: high
  formula: high
  parameter: high
  feature: high
relations:
  complementary_to: [ahp, entropy_weight, critic]
  alternative_to: [vikor, promethee]
references:
  - https://doi.org/10.1016/0377-2217(94)00032-7
```

## Modeling note

TOPSIS ranks alternatives by relative closeness to an ideal best and ideal worst solution. The knowledge base should treat **weight generation and indicator preprocessing as separate modeling decisions**, not hide them inside TOPSIS.