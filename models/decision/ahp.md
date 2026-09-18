# Analytic Hierarchy Process (AHP)

```yaml
id: ahp
name: Analytic Hierarchy Process
family: multi_criteria_decision
aliases: [AHP, 层次分析法]
tags:
  problem: [decision, evaluation, ranking, selection]
  task: [weighting, ranking, multi_criteria_decision]
  data: [structured, criteria_matrix, pairwise_comparison]
  pattern: [hierarchical_preferences, qualitative_and_quantitative_criteria]
  structure: [hierarchical]
  scale: [small, medium]
  objective: [maximize_utility, ranking]
  constraints: [consistency_constraint]
  mathematics: [matrix_based, eigenvector, pairwise_comparison]
  philosophy: [preference_based, decision_analysis]
  output: [criteria_weights, ranking, priority_vector]
  prerequisites: [criteria_hierarchy, pairwise_comparisons]
  competition: [very_common, evaluation_problem, decision_problem, formula_friendly]
  limitations: [subjective_weights, rank_reversal_risk]
  risks: [inconsistent_judgments, comparison_burden]
  interpretability: [high, formula_interpretability, parameter_interpretability]
applicability:
  hard_match: [multi_criteria_decision, explicit_hierarchy]
  soft_match: [small_number_of_criteria, expert_judgment_available]
  negative_match: [very_large_number_of_criteria, objective_data_only_without_preference_input]
parameters:
  - name: pairwise_scale
    description: Relative importance scale used for pairwise comparisons.
    selection: Usually Saaty-style 1–9 scale; justify any alternative.
  - name: consistency_ratio
    description: Consistency diagnostic for pairwise judgment matrix.
    selection: Check CR before accepting weights.
validation: [consistency_ratio, sensitivity_analysis, rank_stability]
strengths: [transparent, intuitive, combines qualitative and quantitative criteria]
limitations: [subjective_comparisons, hierarchy design affects result]
risks: [inconsistent_matrix, too_many_pairwise_comparisons]
interpretation:
  overall: high
  formula: high
  parameter: high
  feature: high
relations:
  alternative_to: [entropy_weight, critic, topsis]
  complementary_to: [topsis, fuzzy_comprehensive_evaluation]
references:
  - https://doi.org/10.1016/0377-2217(90)90057-I
```

## Modeling note

AHP is primarily a **preference/weight elicitation and ranking framework**, not a generic prediction model. In a competition solution it is often stronger when paired with an explicit evaluation or ranking method rather than used as the entire pipeline.