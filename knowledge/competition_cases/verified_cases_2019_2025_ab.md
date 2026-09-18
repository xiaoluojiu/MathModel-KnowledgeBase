# CUMCM A/B 深度案例：2019–2025

> 本文件只记录当前已经找到公开证据支持的案例知识。它不是“标准答案库”。同一题可能存在多条合理建模路线。

## 2019 A — 高压油管的压力控制

**Problem Pattern**

`dynamic_system × physical_mechanism × control × parameter_estimation`

**公开证据提取**

公开一等奖/优秀论文项目指出：论文建立高压油管内燃油压力变化模型，使用多项式拟合、分段线性插值、微分方程/差分方程，并研究压力控制策略；公开 GitHub 项目同时提供论文、代码和数据。

**Model tags**

- `ordinary_differential_equation`
- `finite_difference`
- `curve_fitting`
- `piecewise_interpolation`
- `control_strategy`
- `numerical_solution`
- `optimization`

**Transferable pattern**

```text
实验/工程数据
→ 参数拟合/插值
→ 机理方程
→ 数值离散
→ 控制变量设计
→ 策略优化
→ 仿真验证
```

**来源**：公开 GitHub 项目与论文评价页。

---

## 2022 A — 波浪能最大输出功率设计

**Problem Pattern**

`mechanistic_physics × dynamic_system × simulation × optimization`

公开资料显示该题核心包括浮子/振子垂荡模型、PTO 阻尼优化，以及加入纵摇自由度后的联合优化。该类题的知识重点不是“调用某个优化算法”，而是先保证动力学方程、附加质量、稳态功率定义和数值稳定性正确。

**Model tags**

- `ordinary_differential_equation`
- `mechanics`
- `dynamic_system`
- `steady_state`
- `numerical_simulation`
- `parameter_optimization`
- `sensitivity_analysis`

**高价值检索条件**

`physical_mechanism=true` + `continuous_dynamics=true` + `objective=power/efficiency` + `parameters_to_optimize`

**来源**：公开赛题资料、专家讲评体系及公开复盘资料。

---

## 2022 B — 无人机遂行编队飞行中的纯方位无源定位

**Problem Pattern**

`localization × geometry × trajectory_estimation × nonlinear_optimization`

公开国家二等奖项目提供原题、论文、MATLAB 源码、仿真结果和讲解 PPT，说明这是可作为高可信案例的数据源。

**Model tags**

- `bearing_only_localization`
- `geometry`
- `trajectory`
- `parameter_estimation`
- `nonlinear_optimization`
- `simulation`
- `error_analysis`

**检索价值**

适用于：

```text
已知运动平台
+ 只有方向/角度观测
+ 目标位置未知
→ 逆问题 / 几何定位 / 参数估计
```

**来源**：公开国家二等奖 GitHub 项目。

---

## 2023 A — 定日镜场的优化设计

**Problem Pattern**

`geometry × optics × simulation × continuous_optimization × metaheuristic`

公开一等奖项目包含论文、答辩 PPT、代码和数据；另有公开代码仓库明确使用 PSO 进行优化。

**Model tags**

- `geometry`
- `optics`
- `simulation`
- `objective_function`
- `continuous_optimization`
- `particle_swarm_optimization`
- `metaheuristic`
- `sensitivity_analysis`

**重要关系**

```text
physical/optical model
        ↓
objective evaluation
        ↓
optimization
        ↓
configuration update
        ↓
simulation validation
```

**注意**：知识库不能把“PSO”当成唯一正确模型。公开项目只是证明一种实际可行路线。

---

## 2023 B — 多波束测线问题

**Problem Pattern**

`geometry × coverage × route_planning × constrained_optimization`

**初始模型标签**

- `geometric_coverage`
- `swath_model`
- `path_planning`
- `overlap_control`
- `constraint_optimization`
- `numerical_optimization`

该案例应与“路径规划、覆盖优化、几何约束”模型簇建立关系，而不是简单归类成“遗传算法题”。

---

## 2024 A — “板凳龙”闹元宵

**Problem Pattern**

`parametric_curve × kinematics × recursive_constraint × collision_detection × path_optimization`

官方/专家公开解析明确提到：建立龙头运动常微分方程模型、龙身和龙尾运动递推模型、调头曲线模型，并建立碰撞判别模型，在不碰撞条件下确定最小螺距和龙头最大速度。

**Model tags**

- `ordinary_differential_equation`
- `parametric_curve`
- `spiral`
- `arc_length`
- `recursive_model`
- `collision_detection`
- `line_segment_intersection`
- `trajectory_simulation`
- `path_optimization`

**典型 Pipeline**

```text
螺线参数化
→ 弧长/位置关系
→ 龙头 ODE
→ 龙身递推
→ 几何碰撞检测
→ 调头曲线
→ 最小螺距/最大速度优化
```

**来源**：命题人/专家公开讲解、公开论文和代码项目。

---

## 2024 B — 生产过程中的决策问题

**Problem Pattern**

`quality_control × sequential_decision × probability × hypothesis_testing × dynamic_optimization`

公开专家解析的关键词包括：序贯概率比检验、声称质量水平、操作特性曲线、区间估计、假设检验。高校教学活动的公开资料还指出，该题可用抽样概率、机理分析和动态规划研究多阶段检测与拆解策略。

**Model tags**

- `sampling`
- `hypergeometric_distribution`
- `binomial_model`
- `hypothesis_testing`
- `sequential_probability_ratio_test`
- `confidence_interval`
- `quality_control`
- `expected_cost`
- `dynamic_programming`
- `decision_model`

**关键检索模式**

```text
批次质量未知
+ 抽样检测
+ 检测成本
+ 不合格处理
+ 多阶段决策
→ statistical_decision + sequential_decision + optimization
```

**来源**：数学建模及其应用公开解析、北京工业大学机构库及高校专题讲座资料。

---

## 2025 A — 烟幕干扰弹的投放策略

**Problem Pattern**

`3D_kinematics × projectile_motion × geometry × occlusion × constrained_optimization`

公开建模资料可以核验导弹、无人机、烟幕弹和云团的运动状态及五个子问题结构。

**Model tags**

- `three_dimensional_geometry`
- `kinematics`
- `projectile_motion`
- `trajectory`
- `visibility/occlusion`
- `time_window`
- `constraint_optimization`
- `multi_agent_coordination`
- `simulation`

**核心抽象**

```text
运动体状态方程
→ 遮蔽几何判定
→ 有效时间区间
→ 单机策略优化
→ 多弹协同
→ 多无人机/多目标协同优化
```

**重要提醒**：公开方案可以使用不同优化器。知识库应优先记录“优化问题结构”和“约束”，算法只作为候选求解器。

---

## 2025 B — 碳化硅外延层厚度的确定

**Problem Pattern**

`optical_interference × inverse_problem × parameter_estimation × nonlinear_fitting`

公开作品给出了双光束干涉、折射率色散、FFT 频谱分析、多光束干涉、Airy/Fabry–Pérot 模型和非线性最小二乘等路线。

**Model tags**

- `thin_film_interference`
- `fresnel_equations`
- `snell_law`
- `dispersion_model`
- `inverse_problem`
- `fft`
- `peak_detection`
- `nonlinear_least_squares`
- `airy_model`
- `fabry_perot`
- `uncertainty_analysis`

**典型 Pipeline**

```text
反射光谱
→ 数据预处理
→ 干涉条纹分析
→ 物理模型
→ FFT / 峰值初值
→ 非线性参数拟合
→ 多光束效应判定
→ 修正模型
→ 厚度反演 + 不确定度
```

**知识库价值**

这是典型的“不要直接机器学习”的案例：如果题目给出了明确物理机制，优先检索 `mechanistic + inverse_problem` 模型族，再考虑数据驱动方法作为辅助。

**来源**：公开国赛 B 题论文/解题资料及公开算法资料。
