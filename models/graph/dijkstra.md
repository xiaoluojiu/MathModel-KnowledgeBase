# Dijkstra Shortest Path

```yaml
id: dijkstra
name: Dijkstra's Shortest Path Algorithm
family: graph_algorithm
aliases: [Dijkstra, Dijkstra Algorithm, 迪杰斯特拉算法]
tags:
  problem: [path_planning, routing, network_optimization]
  task: [shortest_path, route_selection]
  data: [graph, network, weighted_edges]
  pattern: [nonnegative_edge_weights]
  structure: [graph, network, directed_or_undirected]
  scale: [small, medium, large]
  objective: [minimize_distance, minimize_time, minimize_cost]
  constraints: [nonnegative_edge_weights]
  mathematics: [graph_theory, greedy_algorithm, deterministic]
  philosophy: [algorithmic, exact]
  output: [shortest_path, shortest_distance]
  prerequisites: [source_node, edge_weights, nonnegative_weights]
  competition: [very_common, graph_problem, formula_friendly]
  limitations: [nonnegative_edge_requirement]
  risks: [wrong_edge_weight_definition, disconnected_graph]
  interpretability: [very_high, formula_interpretability]
applicability:
  hard_match: [single_source_shortest_path, nonnegative_edge_weights]
  soft_match: [route_network, transportation_network]
  negative_match: [negative_edge_weights, all_pairs_shortest_path_as_the_only_requirement]
parameters:
  - name: source
    description: Starting node.
    selection: Defined by the problem's origin.
  - name: edge_weight
    description: Cost, time, distance or other additive edge quantity.
    selection: Confirm additivity and nonnegativity.
validation: [path_cost_recalculation, reachability_check, comparison_with_floyd_for_small_graph]
strengths: [exact, efficient, easy_to_explain]
limitations: [negative_edges_not_supported]
risks: [nonadditive_costs, incorrect_network_construction]
interpretation:
  overall: very_high
  formula: high
  parameter: high
  feature: high
relations:
  alternative_to: [floyd_warshall, a_star]
  special_case_of: [shortest_path]
references: []
```

## Modeling note

Dijkstra is a graph algorithm, not a statistical model. Its model-selection signal is the **network representation and edge-cost semantics**. Do not convert a problem to a graph merely to use Dijkstra.