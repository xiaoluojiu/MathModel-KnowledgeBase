# 2025 CUMCM A196 — Evidence Card

> 状态：正文 OCR 已核验；以下方法均来自论文正文/摘要镜像。历史使用不等于当前题目推荐。

## Source

- Official showcase: https://dxs.moe.gov.cn/zx/a/hd_sxjm_sxjmlw_2025qgdxssxjmjslwzs_2025atlw/251101/2022729.shtml
- OCR text mirror: https://github.com/yushugulao/CUMCM-Archive/blob/main/research_index/pdf_text/2025/A/优秀论文/A196--89f5a9e676.md
- Pages: 98

## Problem pattern

`mechanistic_kinematics + geometric_visibility + simulation_based_optimization + high_dimensional_coordination`

## Data / structure pattern

`3D_coordinates + trajectories + time_window + geometric_constraints + discrete_sampling`

## Explicitly evidenced methods

### Physical / geometric model
- Missile and UAV position functions
- Smoke-cloud motion model
- Line-of-sight / target-occlusion geometry
- Boolean occlusion function
- Continuous effective-occlusion interval argument

### Numerical / search methods
- Bisection search for effective-occlusion interval endpoints
- Multi-start variable-step coordinate search
- Particle Swarm Optimization as independent validation
- Differential Evolution for independent validation / optimization
- Local grid search
- Predicted-interception-point based dimensionality reduction
- Hierarchical optimization for multi-UAV/multi-smoke/multi-missile case
- Task allocation before continuous parameter optimization

### Sensitivity / validation
- Polygon discretization of circular boundaries
- Sensitivity analysis over boundary sampling count
- Independent solver comparison
- Relative-error comparison

## Method roles

| Method | Role | Tags |
|---|---|---|
| Kinematics | mechanistic forward model | `mechanistic`, `kinematics`, `trajectory` |
| Occlusion geometry | constraint/objective evaluator | `computational_geometry`, `visibility`, `boolean_condition` |
| Bisection | interval boundary solver | `root_finding`, `bracketing`, `numerical_method` |
| Multi-start coordinate search | primary low-dimensional optimizer | `derivative_free`, `multi_start`, `local_search` |
| PSO | validation / alternative optimizer | `metaheuristic`, `global_search`, `validation` |
| Differential Evolution | optimizer / validation | `evolutionary`, `global_search`, `validation` |
| Local grid search | refinement | `local_refinement`, `derivative_free` |
| Predicted interception point | structural dimensionality reduction | `problem_reduction`, `geometry`, `coordination` |
| Hierarchical optimization | high-dimensional decomposition | `decomposition`, `task_allocation`, `large_search_space` |

## Key modeling insight

The important transferable pattern is not "use PSO/DE". It is:

`mechanistic simulation -> non-smooth/black-box objective -> exploit geometry/physics to reduce search space -> derivative-free optimization -> independent solver validation`.

For the multi-agent case the paper further uses:

`task allocation -> independent subproblem optimization -> temporal interval intersection`.

## Historical route graph

```text
3D kinematics
      ↓
line-of-sight / occlusion evaluator
      ↓
black-box effective-time objective
      ↓
physics/geometry-based reduction
      ↓
┌───────────────┬────────────────────┐
↓               ↓                    ↓
multi-start     local grid            DE / PSO
coordinate      refinement            validation
search
      ↓
optimal deployment

high-dimensional case:
task allocation
      ↓
subproblem optimization
      ↓
interval intersection
      ↓
coordinated objective
```

## Negative / caution knowledge

- PSO and Differential Evolution are not automatically preferred simply because the objective is nonlinear.
- The paper's strongest transferable contribution is exploiting problem geometry before optimization; this can reduce dimensionality and computational cost.
- Discrete sampling of a geometric boundary introduces approximation error; sampling density must be sensitivity-tested.
- A derivative-free optimizer is appropriate when the objective is obtained through simulation and lacks a reliable analytic gradient; this is a condition, not a universal rule.
- Multi-UAV problems can benefit from decomposition/task allocation before continuous optimization rather than blindly optimizing the full decision vector.

## Retrieval tags

`cumcm_2025` `A` `mechanistic_model` `kinematics` `3D_geometry` `visibility` `occlusion` `simulation` `black_box_objective` `derivative_free` `multi_start` `coordinate_search` `bisection` `particle_swarm` `differential_evolution` `grid_search` `dimensionality_reduction` `task_allocation` `hierarchical_optimization` `sensitivity_analysis` `model_validation`
