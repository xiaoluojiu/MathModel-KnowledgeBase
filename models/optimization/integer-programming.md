# Integer Programming (IP)

```yaml
id: integer_programming
name: Integer Programming
family: mathematical_optimization
aliases: [IP, Integer Linear Programming, 整数规划]
tags:
  problem: [optimization, scheduling, assignment, selection, allocation]
  task: [discrete_optimization, combinatorial_selection]
  data: [structured, tabular]
  pattern: [discrete_decisions]
  structure: [decision_variables, constraints]
  scale: [small, medium, large]
  objective: [minimize_cost, maximize_profit, maximize_coverage]
  constraints: [linear_constraints, integer_constraints, binary_constraints, capacity_constraints, logical_constraints]
  mathematics: [discrete_optimization, combinatorial, exact_optimization]
  philosophy: [optimization_based]
  output: [optimal_solution, decision_variable]
  prerequisites: [integer_or_binary_variables, objective_definition, feasible_constraints]
  competition: [very_common, optimization_problem, formula_friendly]
  limitations: [computational_complexity, formulation_complexity]
  risks: [large_search_space, infeasibility, solver_time]
  interpretability: [high, formula_interpretability]
applicability:
  hard_match: [discrete_or_binary_decisions]
  soft_match: [selection, scheduling, assignment]
  negative_match: [truly_continuous_decisions_with_no_discrete_logic]
parameters:
  - name: integrality_constraints
    description: Variables constrained to integer or binary values.
    selection: Use binary variables for yes/no decisions and integer variables for counts.
  - name: big_m
    description: Optional constant used to encode conditional logic.
    selection: Use the tightest valid bound; avoid unnecessarily huge values.
validation: [feasibility_check, integrality_check, constraint_slack_analysis, optimality_gap]
strengths: [models_discrete_logic, exact_or_bounded_optima, expressive_formulations]
limitations: [harder_than_LP, formulation_sensitive]
risks: [weak_big_m_formulation, long_solver_time, combinatorial_explosion]
interpretation:
  overall: high
  formula: high
  parameter: high
  feature: high
relations:
  extension_of: [linear_programming]
  alternative_to: [mixed_integer_programming, genetic_algorithm]
  special_case_of: [mixed_integer_programming]
references: []
```

## Modeling note

Integer programming is the natural bridge from a continuous allocation model to discrete competition decisions such as facility opening, worker assignment, route selection and yes/no choices.