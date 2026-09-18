# Monte Carlo Simulation

```yaml
id: monte_carlo
name: Monte Carlo Simulation
family: stochastic_simulation
aliases: [Monte Carlo, 蒙特卡洛模拟]
tags:
  problem: [simulation, uncertainty, risk, probability, optimization]
  task: [uncertainty_quantification, probability_estimation, risk_analysis, numerical_integration]
  data: [structured, stochastic_inputs]
  pattern: [randomness, uncertainty, nonlinear_response]
  structure: [independent_or_dependent_samples]
  scale: [medium, large]
  objective: [estimate_expectation, estimate_probability, quantify_risk]
  constraints: [distribution_assumptions]
  mathematics: [probabilistic, stochastic, sampling_based]
  philosophy: [simulation_based, data_driven]
  output: [probability, expectation, confidence_interval, risk_measure]
  prerequisites: [random_variable_definition, sampling_scheme, input_distributions]
  competition: [very_common, simulation_problem, uncertainty_analysis]
  limitations: [sampling_error, computational_cost]
  risks: [wrong_distribution_assumption, insufficient_samples, correlated_sampling]
  interpretability: [high, mechanism_interpretability]
applicability:
  hard_match: [uncertainty_propagation, probability_estimation_by_sampling]
  soft_match: [complex_black_box_system, no_closed_form_solution]
  negative_match: [deterministic_closed_form_solution_is_available_and_preferred]
parameters:
  - name: sample_size
    description: Number of simulated realizations.
    selection: Increase until estimates and uncertainty intervals stabilize.
  - name: random_seed
    description: Reproducibility seed for pseudo-random generators.
    selection: Fix for reproducible reporting and repeat across seeds for robustness.
validation: [convergence_curve, confidence_interval, repeated_seed_analysis, variance_reduction_check]
strengths: [flexible, handles_complex_systems, natural_uncertainty_propagation]
limitations: [slow_convergence, requires_input_distributions_or_sampling_models]
risks: [distribution_misspecification, monte_carlo_noise]
interpretation:
  overall: high
  formula: medium
  parameter: high
  feature: medium
relations:
  complementary_to: [sensitivity_analysis, optimization, queueing]
  alternative_to: [analytical_probability]
references: []
```

## Modeling note

Monte Carlo is a **simulation framework**, not a single predictive estimator. The knowledge base should retrieve it when uncertainty or stochastic system behavior is central to the question, and should expose sampling error rather than treating one simulation run as a deterministic answer.