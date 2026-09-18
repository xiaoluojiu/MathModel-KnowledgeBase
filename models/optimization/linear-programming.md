# Linear Programming (LP)

```yaml
id: linear_programming
name: Linear Programming
family: mathematical_optimization
aliases: [LP, Linear Programming, 线性规划]
tags:
  problem: [optimization, resource_allocation, production_planning, transportation]
  task: [optimal_allocation, cost_minimization, profit_maximization]
  data: [structured, tabular]
  pattern: [linear_relationships]
  structure: [decision_variables, constraints]
  scale: [small, medium, large]
  objective: [minimize_cost, maximize_profit, maximize_efficiency]
  constraints: [linear_constraints, equality_constraints, inequality_constraints, capacity_constraints, budget_constraints]
  mathematics: [convex_optimization, continuous, deterministic]
  philosophy: [optimization_based]
  output: [optimal_solution, decision_variable]
  prerequisites: [linear_objective, linear_constraints, variable_domains]
  competition: [very_common, optimization_problem, formula_friendly]
  limitations: [linear_assumption, deterministic_formulation]
  risks: [bad_parameter_estimation, infeasibility, unbounded_solution]
  interpretability: [high, formula_interpretability, parameter_interpretability]
applicability:
  hard_match: [linear_objective_and_constraints]
  soft_match: [continuous_decision_variables, known_coefficients]
  negative_match: [essential_nonlinearity, discrete_decisions_without_relaxation]
parameters:
  - name: objective_coefficients
    description: Coefficients of the linear objective.
    selection: Derive directly from the problem statement or calibrated data.
  - name: constraint_coefficients
    description: Coefficients and bounds defining feasible decisions.
    selection: Verify units and feasibility before solving.
  - name: variable_bounds
    description: Lower/upper bounds for decision variables.
    selection: Encode physical and logical limits explicitly.
validation: [feasibility_check, constraint_slack_analysis, sensitivity_analysis, objective_recalculation]
strengths: [globally_solvable_convex_structure, interpretable, mature_solvers]
limitations: [requires_linear_structure, coefficient_uncertainty_not_automatic]
risks: [infeasible_model, unbounded_model, unit_inconsistency]
interpretation:
  overall: very_high
  formula: very_high
  parameter: high
  feature: high
relations:
  extension_of: [convex_optimization]
  alternative_to: [nonlinear_programming, integer_programming]
  special_case_of: [mathematical_optimization]
references: []
```

## Modeling note

LP is often the first model to test when a competition problem describes resource allocation with linear costs, capacities and conservation relations. Do not force linearity when the underlying mechanism is materially nonlinear.