# Floyd–Warshall Algorithm

```yaml
id: floyd_warshall
name: Floyd–Warshall Algorithm
family: graph_algorithm
aliases: [Floyd, Floyd-Warshall, 弗洛伊德算法]
tags:
  problem: [path_planning, routing, network_analysis]
  task: [all_pairs_shortest_path]
  data: [graph, network, weighted_edges]
  pattern: [additive_edge_weights]
  structure: [graph, directed_or_undirected]
  scale: [small, medium]
  objective: [minimize_distance, minimize_time, minimize_cost]
  constraints: [edge_weight_semantics]
  mathematics: [graph_theory, dynamic_programming, deterministic]
  philosophy: [algorithmic, exact]
  output: [distance_matrix, shortest_paths]
  prerequisites: [weighted_graph]
  competition: [very_common, graph_problem, formula_friendly]
  limitations: [cubic_time_complexity, negative_cycle_issue]
  risks: [large_dense_graph_runtime, incorrect_infinite_value_handling]
  interpretability: [very_high, formula_interpretability]
applicability:
  hard_match: [all_pairs_shortest_path]
  soft_match: [small_or_medium_dense_graph]
  negative_match: [huge_sparse_graph_where_single_source_is_enough]
parameters:
  - name: distance_matrix
    description: Initial direct-edge matrix with infinity for absent edges.
    selection: Ensure diagonal and unreachable values are encoded correctly.
validation: [triangle_like_path_checks, symmetry_check_when_graph_is_undirected, comparison_with_dijkstra]
strengths: [simple, all_pairs_result, handles_negative_edges_without_negative_cycles]
limitations: [O(n^3), not suitable for negative cycles]
risks: [integer_overflow_in_low_level_implementations, incorrect_missing_edge_encoding]
interpretation:
  overall: very_high
  formula: high
  parameter: high
  feature: high
relations:
  alternative_to: [dijkstra]
  special_case_of: [shortest_path]
references: []
```

## Modeling note

Floyd–Warshall is appropriate when the problem asks for shortest paths between many pairs and the graph size makes its cubic dynamic-programming structure practical.