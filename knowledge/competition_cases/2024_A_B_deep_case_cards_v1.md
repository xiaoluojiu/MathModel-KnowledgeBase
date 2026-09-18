# CUMCM 2024 A/B — Deep Case Cards v1

> Evidence status: problem titles and official expert-commentary existence verified from official/public sources. Historical-model fields are separated into `verified`, `supported`, and `inferred`; do not promote inferred routes to historical_usage without paper-body evidence.

## 2024 A — “板凳龙”闹元宵

### Problem profile
- Domain: mechanics / geometry / kinematics / path planning / constrained optimization
- Core object: a linked dragon formed by benches moving along planar curves.
- Main structures: Archimedean spiral, arc-length parameterization, fixed handle distances, recursive node positions, velocity propagation, collision detection, turnaround-path design.
- Primary task families: simulation + geometric constraint solving + feasibility search + optimization.

### Data pattern
- Geometric parameters
- Bench/handle dimensions
- Initial spiral/path parameters
- Time-dependent positions and velocities
- Candidate turnaround geometry

### Candidate model families
- Parametric geometry
- Arc-length ODE / numerical integration
- Nonlinear equation solving
- Recursive constraint propagation
- Computational geometry / segment intersection
- Constrained nonlinear optimization
- Binary feasibility search when the objective is a monotone geometric threshold

### Negative checks
- Pure regression is not a first-choice model when the governing geometry is explicitly known.
- Generic black-box ML should not replace the mechanistic geometry model merely because numerical data are available.
- A heuristic optimizer is a solver option, not the mathematical model itself.

### Transferable patterns
`mechanistic_geometry`, `linked_body_kinematics`, `arc_length_parameterization`, `collision_avoidance`, `path_design`, `constraint_satisfaction`, `feasibility_threshold`

### Evidence
Official 2024 A paper-display pages exist on China University Student Online; the official competition commentary identifies A as “板凳龙闹元宵”. Public technical reproductions independently describe spiral trajectory, handle-distance constraints, collision detection and turnaround optimization. Treat those reproductions as secondary evidence, not award-paper evidence.

---

## 2024 B — “生产过程中的决策问题”

### Problem profile
- Domain: quality control / operations research / decision analysis / stochastic cost optimization
- Core structure: components with defective probabilities, inspection decisions, assembly, finished-product inspection, disassembly/rework and cost/revenue trade-offs.
- Main task families: statistical inference + discrete decision optimization + expected-cost analysis.

### Data pattern
- Defect rates / estimated defect rates
- Inspection costs
- Assembly cost
- Finished-product testing cost
- Disassembly / replacement / loss cost
- Sale/recovery value
- Sequential process decisions

### Candidate model families
- Binomial / normal approximation / confidence intervals
- Hypothesis testing / sampling inspection
- Expected-cost enumeration
- Decision tree / state-transition representation
- Dynamic programming for sequential decisions when state dependence exists
- Integer / binary optimization for discrete inspection choices
- Sensitivity and robustness analysis

### Negative checks
- Do not jump directly to AHP/TOPSIS: this is a decision optimization problem with explicit cost and probability structure, not a generic multi-criteria ranking task.
- Do not treat “decision tree” as the underlying optimization model if it is only a visualization of discrete states.
- Do not label a particular heuristic algorithm as historically used without paper-body evidence.

### Transferable patterns
`quality_control`, `sampling_inspection`, `binary_decision`, `expected_cost`, `sequential_decision`, `production_process`, `stochastic_decision`

### Evidence
The official China University Student Online 2024 B collection contains multiple displayed papers, including B195/B159/B196. The official commentary portal lists a dedicated 2024 B expert commentary. Public competition records identify the problem as “生产过程中的决策问题”.

---

## Model-role decomposition for A/B

| Layer | 2024A | 2024B |
|---|---|---|
| Mechanism | geometry/kinematics | probability/production process |
| State | node positions, velocities | component/product states |
| Constraints | distances, non-intersection, path geometry | inspection/process/cost constraints |
| Core solver | numerical root/ODE + search/optimization | enumeration/DP/discrete optimization |
| Validation | geometric consistency + numerical stability | probability/cost consistency + sensitivity |
| Typical anti-pattern | ML-first black box | generic multi-criteria ranking |

### Relation edges
- `2024A -> mechanistic_geometry`
- `2024A -> computational_geometry`
- `2024A -> constrained_optimization`
- `2024B -> stochastic_decision`
- `2024B -> quality_control`
- `2024B -> expected_cost`
- `2024B -> discrete_optimization`
- `mechanistic_geometry --compatible_with--> numerical_solver`
- `expected_cost --compatible_with--> enumeration`
- `expected_cost --compatible_with--> dynamic_programming`
