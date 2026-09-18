# Dynamic Programming (DP)

```yaml
id: dynamic_programming
name: Dynamic Programming
family: combinatorial_optimization
aliases: [DP, Dynamic Programming, 动态规划]
tags:
  problem: [optimization, scheduling, resource_allocation, path_planning, sequential_decision]
  task: [optimal_substructure_search, sequential_decision]
  data: [structured, tabular]
  pattern: [optimal_substructure, overlapping_subproblems]
  structure: [sequential, staged_decision]
  scale: [small, medium, large]
  objective: [minimize_cost, maximize_profit, maximize_reward]
  constraints: [state_constraints, transition_constraints, capacity_constraints]
  mathematics: [recurrence, discrete_optimization, deterministic]
  philosophy: [optimization_based]
  output: [optimal_solution, policy, decision_sequence]
  prerequisites: [state_definition, transition_definition, boundary_conditions]
  competition: [very_common, optimization_problem, formula_friendly]
  limitations: [state_space_explosion, formulation_specificity]
  risks: [incorrect_state_definition, excessive_memory_or_time]
  interpretability: [high, formula_interpretability]
applicability:
  hard_match: [optimal_substructure, staged_or_sequential_decisions]
  soft_match: [finite_state_space, recurrence_can_be_defined]
  negative_match: [no_state_decomposition, enormous_uncompressed_state_space]
parameters:
  - name: state
    description: Minimal information required to characterize the remaining decision problem.
    selection: Avoid carrying irrelevant history; include all information needed for future transitions.
  - name: transition
    description: Recurrence linking current state to predecessor or successor states.
    selection: Derive directly from the problem's decision process.
validation: [boundary_condition_check, recurrence_check, brute_force_small_instance, solution_reconstruction]
strengths: [exact_for_valid_decomposition, clear_recursion, strong_for_sequential_decisions]
limitations: [state_design_is_problem_specific, curse_of_dimensionality]
risks: [hidden_state_information, exponential_state_growth]
interpretation:
  overall: high
  formula: very_high
  parameter: high
  feature: medium
relations:
  alternative_to: [integer_programming, shortest_path]
  special_case_of: [combinatorial_optimization]
references: []
```

## Modeling note

DP is a **problem decomposition strategy** rather than one fixed statistical estimator. The decisive knowledge-base tags are `optimal_substructure`, `overlapping_subproblems`, and the structure of the state space.