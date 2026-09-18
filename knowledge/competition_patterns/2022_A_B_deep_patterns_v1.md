# CUMCM 2022 A/B — Deep Problem Patterns v1

## 2022 A — 波浪能最大输出功率设计

### Problem pattern
A mechanical vibration / energy-conversion problem. The floating body and oscillator respond to wave excitation; the PTO damper converts relative motion into output power. The design objective is to choose damping parameters to maximize average power.

### Mathematical structure
- Coupled vibration equations
- Wave excitation
- Linear and nonlinear damping
- Spring/restoring terms
- Added inertia / radiation damping
- Steady-state or long-window average power
- Parameter optimization

### Model families
- ODE / coupled dynamical system
- Harmonic/steady-state analysis when linear assumptions permit
- Numerical ODE integration for nonlinear cases
- Stability analysis
- Constrained parameter optimization
- Sensitivity analysis

### Tags
`mechanistic_dynamics`, `vibration`, `energy_conversion`, `ode`, `steady_state`, `parameter_optimization`, `sensitivity`

### Negative checks
- Pure regression does not replace the governing dynamics when physical equations are available.
- A metaheuristic is only a solver choice.
- Time-series forecasting models such as ARIMA are not the natural primary model for a known mechanical excitation system.

## 2022 B — 无人机遂行编队飞行中的纯方位无源定位

### Problem pattern
A geometric localization and correction problem. UAVs maintain a known relative formation; some transmit and others infer angular information. The task is to select transmitting/reference UAVs and determine correction strategies while minimizing the number of transmitting UAVs.

### Mathematical structure
- Circle/formation geometry
- Bearing-angle constraints
- Coordinate reconstruction / localization
- Deviation estimation
- Sequential correction
- Discrete selection / minimum transmitter set

### Model families
- Analytic geometry / trigonometric geometry
- Circle fitting / geometric estimation
- Bearing-only localization
- Graph representation of correction relationships
- Set-cover / minimum dominating-style formulations where the exact relation permits
- Combinatorial optimization / dynamic programming / search

### Tags
`geometry`, `localization`, `bearing_only`, `formation_control`, `discrete_optimization`, `coverage_relation`, `graph_model`

### Negative checks
- Do not force a regression model onto a deterministic geometric relation.
- Do not call every transmitter-selection problem “set cover” without verifying the coverage relation.
- Do not confuse formation correction with continuous trajectory optimization unless the task explicitly introduces motion over time.

## Historical evidence
The official China University Student Online 2022 A/B commentary index explicitly identifies A as “波浪能最大输出功率设计” and B as “无人机遂行编队飞行中的纯方位无源定位”. The official paper-display index lists multiple A and B papers. Public reproductions provide secondary technical analyses; specific paper-level historical usage remains subject to body evidence.

## Cross-case relations
- `2022A -> mechanistic_dynamics -> ODE -> parameter_optimization`
- `2022B -> geometric_localization -> discrete_selection`
- Both illustrate the rule: **identify governing structure before selecting an algorithm**.
