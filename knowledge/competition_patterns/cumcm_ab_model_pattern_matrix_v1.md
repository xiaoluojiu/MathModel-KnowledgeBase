# CUMCM A/B → Problem Pattern → Model Family Matrix V1

> 这是检索矩阵，不是“标准答案表”。它描述结构匹配空间；历史论文证据与当前新题适配性必须分开。

| Pattern | Typical signals | Candidate model families | Key negative checks |
|---|---|---|---|
| inverse_problem + parameter_estimation | 观测量已知、物理/几何关系已知、未知参数 | nonlinear least squares, maximum likelihood, Bayesian estimation, optimization | 模型不可辨识、参数高度相关、数据不足 |
| multi_criteria_evaluation | 多指标、综合评分、排序 | AHP, entropy weight, CRITIC, TOPSIS, VIKOR, fuzzy evaluation | 指标方向/量纲错误、权重主观性、强相关指标重复计权 |
| spatial_analysis + pollution | 经纬度/空间采样/污染指标 | interpolation, spatial statistics, clustering, regression, GIS/network models | 空间自相关忽略、采样偏差、插值外推过远 |
| location_allocation + network | 节点/道路/需求点、设施设置 | facility location, shortest path, p-median, integer programming, max flow | 网络拓扑错误、容量约束遗漏 |
| traffic_flow + capacity | 速度、流量、密度、道路占用 | traffic-flow models, queueing, simulation, regression | 稳态假设不成立、拥堵状态切换 |
| reconstruction + image | 图像/碎片/投影数据 | image processing, graph matching, dynamic programming, optimization | 噪声、旋转/尺度不变性、匹配唯一性 |
| dynamical_system + control | 状态随时间变化、控制量、边界条件 | ODE/PDE, numerical integration, optimal control, MPC | 稳定性、刚性、边界条件、数值误差 |
| scheduling + discrete_optimization | 任务、机器、时间窗、资源限制 | LP/MILP, DP, branch-and-bound, GA/PSO/SA, heuristics | 可行域为空、状态爆炸、启发式无可行解保证 |
| resource_allocation | 有限资源、多对象需求、成本/收益 | LP/MILP, transportation, assignment, multi-objective optimization | 线性假设、整数性、供需平衡 |
| heat_transfer + PDE | 温度场、空间位置、时间 | heat equation, finite difference, finite element, inverse heat transfer | 网格稳定性、边界条件、材料参数 |
| physical_measurement + signal_processing | 光谱/时序信号、频率峰值、干涉 | FFT, filtering, peak detection, spectral models, nonlinear fitting | 采样频率不足、混叠、峰值误判 |
| coverage + path_planning | 覆盖宽度、路线、区域 | geometric optimization, routing, set cover, MILP, heuristic optimization | 覆盖断裂、转弯约束、路径自交 |
| sampling + statistical_decision | 抽样、合格率、成本、接受/拒绝 | hypothesis testing, confidence intervals, SPRT, Bayesian decision, expected cost | 独立同分布假设、错误概率约束、抽样成本 |
| physical_model + optimization | 有明确机理 + 设计变量 + 目标 | mechanistic model + nonlinear optimization, global optimization | 机理模型误差不能被优化器“修好” |
| time_series + forecasting | 时间顺序、趋势、季节、自相关 | ARIMA/SARIMA/SARIMAX, ETS, state-space, VAR, ML | 数据泄漏、非平稳性、外生变量未来不可得 |
| game_theory + resource_competition | 多参与方、策略、收益互相影响 | Nash equilibrium, Stackelberg, evolutionary game | 理性假设、信息结构、均衡存在性 |
| inventory + transportation | 库存、需求、补货、运输成本 | inventory models, transportation, MILP, stochastic optimization | 需求不确定性、缺货成本、期末库存 |

## Historical anchor examples

- 2010A → inverse_problem + parameter_estimation + geometry
- 2011B → location_allocation + network + scheduling
- 2014A → dynamical_system + trajectory_optimization + control
- 2015B → resource_allocation + demand_model + optimization
- 2017B → clustering + regression + multi_objective_optimization
- 2018A → heat_transfer + PDE + optimization
- 2018B → scheduling + discrete_optimization
- 2019A → ODE + dynamic_system + optimization
- 2020A → heat_transfer + numerical_method
- 2020B → dynamic_programming + combinatorial_optimization + game_theory
- 2024A → geometry + kinematics + collision_detection + constrained_optimization
- 2024B → sampling + hypothesis_testing + sequential_decision
- 2025A → kinematics + geometry + constrained_optimization
- 2025B → signal_processing + interference + inverse_problem + nonlinear_least_squares

## Retrieval use

1. 从题目和数据报告抽取 signals。
2. 映射到 1–3 个 Problem Pattern。
3. 通过 candidate families 召回模型，而不是直接选模型。
4. 用 hard/soft/negative match 二次过滤。
5. 查询历史案例，查看相同 pattern 下真实使用路线。
6. 最终最多保留两个高质量候选进入 model collision。

## Important limitation

本矩阵不能替代逐篇论文证据。它用于召回候选知识空间；`historical_usage`、`paper_evidence`、`recommended_model` 必须保持不同字段。