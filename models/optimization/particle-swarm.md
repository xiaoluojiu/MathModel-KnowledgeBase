# Particle Swarm Optimization (PSO)

```yaml
id: particle_swarm
name: Particle Swarm Optimization
family: swarm_intelligence
aliases: [PSO, Particle Swarm Optimization, 粒子群优化]
tags:
  problem: [optimization, continuous_optimization, parameter_optimization]
  task: [global_search, approximate_optimization]
  data: [structured, tabular]
  pattern: [nonlinear, nonconvex, multimodal]
  structure: [population_based]
  scale: [small, medium, large]
  objective: [minimize_cost, maximize_profit, multi_objective_optimization]
  constraints: [box_constraints, nonlinear_constraints, penalty_constraints]
  mathematics: [stochastic, derivative_free, nonconvex]
  philosophy: [metaheuristic, swarm_intelligence]
  output: [approximate_optimal_solution, parameter_vector]
  prerequisites: [objective_function, variable_bounds, constraint_handling]
  competition: [very_common, optimization_problem, flexible]
  limitations: [no_general_optimality_guarantee, parameter_sensitive]
  risks: [premature_convergence, boundary_stagnation, stochastic_variance]
  interpretability: [medium]
applicability:
  hard_match: [continuous_nonconvex_search, derivative_free_objective]
  soft_match: [parameter_calibration, expensive_black_box_objective]
  negative_match: [simple_convex_problem_with_exact_solver]
parameters:
  - name: swarm_size
    description: Number of particles.
    selection: Balance diversity against objective evaluations.
  - name: inertia_weight
    description: Controls momentum of particle velocity.
    selection: Tune or schedule based on convergence behavior.
  - name: cognitive_coefficient
    description: Attraction toward each particle's own best position.
    selection: Tune jointly with social coefficient.
  - name: social_coefficient
    description: Attraction toward swarm best position.
    selection: Tune jointly with cognitive coefficient.
validation: [multiple_random_seeds, convergence_curve, bound_check, sensitivity_analysis]
strengths: [simple_continuous_search, derivative_free, easy_to_implement]
limitations: [continuous_representation_is_natural_but_discrete_versions_need_design, approximate]
risks: [premature_convergence, parameter_sensitivity]
interpretation:
  overall: medium
  formula: low
  parameter: medium
  feature: low
relations:
  alternative_to: [genetic_algorithm, simulated_annealing]
  complementary_to: [local_search]
references: []
```

## Modeling note

PSO is a population-based stochastic optimizer. The repository should keep the canonical continuous form separate from discrete or binary variants because their representations and update rules differ.