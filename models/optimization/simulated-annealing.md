# Simulated Annealing (SA)

```yaml
id: simulated_annealing
name: Simulated Annealing
family: metaheuristic_optimization
aliases: [SA, Simulated Annealing, 模拟退火]
tags:
  problem: [optimization, combinatorial_optimization, routing, scheduling]
  task: [global_search, approximate_optimization]
  data: [structured, tabular]
  pattern: [nonconvex, multimodal, rugged_search_space]
  structure: [single_solution_iterative_search]
  scale: [small, medium, large]
  objective: [minimize_cost, maximize_profit]
  constraints: [hard_constraints, penalty_constraints]
  mathematics: [stochastic, derivative_free, nonconvex]
  philosophy: [metaheuristic, probabilistic_search]
  output: [approximate_optimal_solution]
  prerequisites: [objective_function, neighborhood_operator, constraint_handling]
  competition: [common, optimization_problem, flexible]
  limitations: [cooling_schedule_sensitive, stochastic, runtime_sensitive]
  risks: [premature_freezing, excessive_runtime, invalid_neighbors]
  interpretability: [medium]
applicability:
  hard_match: [discrete_or_continuous_nonconvex_search]
  soft_match: [local_minima_risk, meaningful_neighborhood_definition]
  negative_match: [simple_convex_problem_with_exact_solver]
parameters:
  - name: initial_temperature
    description: Starting temperature controlling acceptance of worse moves.
    selection: High enough to explore; validate empirically.
  - name: cooling_schedule
    description: Rule controlling temperature decrease.
    selection: Choose with explicit stopping criteria and convergence checks.
  - name: neighborhood_operator
    description: Generates candidate moves from the current solution.
    selection: Must preserve or explicitly repair feasibility.
validation: [multiple_random_seeds, convergence_curve, feasibility_check, sensitivity_analysis]
strengths: [escapes_local_minima, simple, flexible]
limitations: [parameter_and_schedule_sensitive, approximate]
risks: [freezing_too_early, poor_neighborhood_design]
interpretation:
  overall: medium
  formula: low
  parameter: medium
  feature: low
relations:
  alternative_to: [genetic_algorithm, particle_swarm]
  complementary_to: [local_search, integer_programming]
references: []
```

## Modeling note

SA is especially useful when a meaningful neighborhood move can be defined and local search alone is prone to getting trapped. Its knowledge card should always expose the neighborhood and cooling schedule rather than treating them as implementation trivia.