# CUMCM 2023 A/B — Deep Problem Patterns v1

## 2023 A — 定日镜场的优化设计

### Problem pattern
A physically governed solar-optics layout problem: calculate optical efficiency/output and redesign tower position, mirror dimensions, height, number and placement under power and field constraints.

### Data pattern
- Mirror coordinates / layout
- Solar position by time/date
- Geometric dimensions
- Tower/receiver geometry
- Optical parameters
- Annual-average aggregation over specified representative times

### Model families
- Vector geometry / coordinate transformation
- Solar-position calculation
- Reflection-law / optical mechanism model
- Shadowing / blocking geometry
- Numerical integration / discrete quadrature for annual aggregation
- Constrained nonlinear optimization
- Global/metaheuristic search as a solver where the feasible design space is difficult

### Tags
`physical_mechanism`, `optics`, `geometry`, `layout_optimization`, `multi_constraint`, `annual_aggregation`, `nonlinear_optimization`

### Negative checks
- Regression is not the primary mechanism when optical equations are given.
- PSO/GA is a solver, not the problem definition.
- “Annual average” should not automatically be treated as a time-series forecasting problem.

## 2023 B — 多波束测线问题

### Problem pattern
A bathymetric survey-line design problem: use multibeam coverage geometry and water-depth information to design routes/line spacing while balancing coverage, overlap, efficiency and possibly turning/length constraints.

### Data pattern
- Spatial coordinates
- Bathymetry / depth
- Swath width / coverage angle
- Survey vessel motion assumptions
- Overlap and coverage requirements

### Model families
- Spatial geometry / coordinate transformation
- Swath-footprint geometry
- Coverage / set-cover style formulation
- Route/path planning
- Line-spacing optimization
- Numerical geometry and grid-based computation

### Tags
`spatial_coverage`, `geometric_optimization`, `path_planning`, `survey_design`, `coverage_constraint`, `spatial_data`

### Negative checks
- Generic clustering does not solve route coverage by itself.
- Pure shortest-path algorithms are insufficient when coverage and overlap are constraints.
- ML should be auxiliary unless the task explicitly becomes prediction from bathymetric observations.

## Cross-case relations
- `2023A -> physical_geometry -> constrained_optimization`
- `2023B -> spatial_geometry -> coverage_optimization`
- Both are strong examples of `mechanistic_model + numerical_solver`, where the solver may be GA/PSO/etc. but the mathematical structure remains geometry/constraints.

## Evidence status
Official China University Student Online has a 2023 A/B paper-display index and individual paper pages. The official/educational commentary pages identify 2023 A as “定日镜场的优化设计” and 2023 B as “多波束测线问题”. Historical usage of any specific solver must be promoted only after body-level paper evidence is extracted.
