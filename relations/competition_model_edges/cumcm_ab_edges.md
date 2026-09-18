# CUMCM A/B → Model Knowledge Graph Edges

> 这是竞赛案例与模型知识库之间的关系层。边必须区分“题目结构适配”和“论文证据采用”。

## Edge types

- `problem_requires`：题目结构天然要求某类模型。
- `paper_uses`：公开论文明确使用该模型。
- `paper_alternates`：论文使用的替代模型。
- `supports`：模型作为另一个模型的辅助。
- `validates`：用于验证/诊断。
- `optimizes`：模型负责求解优化问题。
- `parameterizes`：用于参数估计。
- `similar_pattern_to`：两个历史题共享 Problem Pattern。

## Current high-confidence / evidence-backed edges

### 2019A

```text
2019A
 ├─ paper_uses → ordinary_differential_equation
 ├─ paper_uses → finite_difference
 ├─ paper_uses → curve_fitting
 ├─ paper_uses → piecewise_interpolation
 ├─ paper_uses → numerical_solution
 └─ paper_uses → control_strategy
```

### 2022B

```text
2022B
 ├─ paper_uses → bearing_only_localization
 ├─ paper_uses → geometry
 ├─ paper_uses → trajectory_estimation
 ├─ paper_uses → nonlinear_optimization
 └─ validates → simulation
```

### 2023A

```text
2023A
 ├─ problem_requires → geometric_optical_model
 ├─ paper_uses → particle_swarm_optimization
 ├─ supports → numerical_simulation
 └─ validates → sensitivity_analysis
```

### 2024A

```text
2024A
 ├─ problem_requires → parametric_curve
 ├─ paper_uses → ordinary_differential_equation
 ├─ paper_uses → recursive_model
 ├─ paper_uses → collision_detection
 ├─ paper_uses → line_segment_intersection
 └─ optimizes → path_parameters
```

### 2024B

```text
2024B
 ├─ paper_uses → hypothesis_testing
 ├─ paper_uses → confidence_interval
 ├─ paper_uses → sequential_probability_ratio_test
 ├─ paper_uses → quality_control
 └─ optimizes → dynamic_decision
```

### 2025B

```text
2025B
 ├─ problem_requires → thin_film_interference
 ├─ paper_uses → dispersion_model
 ├─ paper_uses → fft
 ├─ paper_uses → nonlinear_least_squares
 ├─ paper_uses → airy_model
 └─ parameterizes → layer_thickness
```

### 2025A

```text
2025A
 ├─ problem_requires → three_dimensional_kinematics
 ├─ problem_requires → projectile_motion
 ├─ problem_requires → occlusion_geometry
 ├─ optimizes → release_strategy
 └─ validates → time_domain_simulation
```

## Pattern clusters discovered

### Cluster P1 — Mechanistic inverse problem

```text
2010A
2015A
2017A
2019A
2021A
2022A
2025B
```

Common structure:

`physical mechanism → observation → unknown parameter/state → inverse estimation → validation`

Candidate model family:

`ODE/PDE | geometry | parameter estimation | nonlinear least squares | Bayesian inference | numerical optimization`

### Cluster P2 — Geometry + optimization

```text
2014A
2016A
2023A
2024A
2025A
```

Common structure:

`geometric constraints → objective → feasible region → numerical optimization → simulation`

### Cluster P3 — Resource / decision optimization

```text
2011B
2015B
2018B
2020B
2021B
2024B
```

Common structure:

`resources / demand / uncertainty → decision variables → objective → constraints → optimization / dynamic programming`

### Cluster P4 — Evaluation / decision

```text
2010B
2012A
2017B
2024B
```

Common structure:

`indicator/data → uncertainty/weighting → decision rule → ranking / policy`

## Negative knowledge

历史案例不应被编码成“题目名称 → 固定模型”。例如：

- 2023A 不是“PSO题”；PSO只是公开方案中的一个优化器。
- 2025B 不是“FFT题”；FFT可以用于频域初值/分析，核心仍是光学干涉物理模型和厚度反演。
- 2024B 不是“动态规划题”；其前端包含质量抽样、假设检验等统计决策问题。
- 2024A 不是“碰撞检测题”；碰撞只是完整运动建模与路径优化链中的一个子任务。

这种负知识将用于 AI 的 Negative Match 与 Model Collision。
