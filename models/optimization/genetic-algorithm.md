# Genetic Algorithm (GA)

```yaml
id: genetic_algorithm
name: Genetic Algorithm
family: evolutionary_optimization
aliases: [GA, Genetic Algorithm, 遗传算法]
tags:
  problem: [optimization, combinatorial_optimization, scheduling, routing]
  task: [global_search, approximate_optimization]
  data: [structured, tabular]
  pattern: [nonlinear, nonconvex, discontinuous, multimodal]
  structure: [population_based]
  scale: [medium, large]
  objective: [minimize_cost, maximize_profit, multi_objective_optimization]
  constraints: [nonlinear_constraints, discrete_constraints, penalty_constraints]
  mathematics: [stochastic, heuristic, derivative_free, nonconvex]
  philosophy: [metaheuristic, evolutionary]
  output: [approximate_optimal_solution, decision_variable]
  prerequisites: [objective_function, encoding_or_solution_representation, constraint_handling]
  competition: [very_common, optimization_problem, flexible]
  limitations: [no_general_optimality_guarantee, parameter_sensitive]
  risks: [premature_convergence, computational_cost, poor_constraint_handling]
  interpretability: [medium, formula_interpretability_low]
applicability:
  hard_match: [black_box_or_nonconvex_objective, derivative_free_search]
  soft_match: [discrete_search, multimodal_landscape, expensive_exact_solver]
  negative_match: [simple_convex_problem_with_available_exact_solver]
parameters:
  - name: population_size
    description: Number of candidate solutions maintained each generation.
    selection: Tune against runtime and diversity; avoid copying a single default.
  - name: crossover_rate
    description: Probability of recombination between parent solutions.
    selection: Tune with representation and diversity in mind.
  - name: mutation_rate
    description: Probability of mutation applied to candidate solutions.
    selection: Increase when diversity collapses; calibrate to encoding.
  - name: generations
    description: Number of evolutionary iterations.
    selection: Use convergence curves and compute budget.
validation: [multiple_random_seeds, convergence_curve, feasibility_check, sensitivity_analysis]
strengths: [derivative_free, flexible, handles_discrete_and_nonconvex_search]
limitations: [approximate, tuning_required, potentially_expensive]
risks: [premature_convergence, stochastic_variance, invalid_solution_generation]
interpretation:
  overall: medium
  formula: low
  parameter: medium
  feature: low
relations:
  alternative_to: [particle_swarm, simulated_annealing, integer_programming]
  complementary_to: [local_search, linear_programming]
references: []
```

## Modeling note

GA should be selected because the **optimization landscape or decision representation** justifies heuristic search, not merely because it is popular in competitions. When an exact polynomial-time or convex solver is available, compare it before choosing a metaheuristic.