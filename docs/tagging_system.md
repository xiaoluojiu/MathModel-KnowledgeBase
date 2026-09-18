# Model Tagging System V1.0

标签系统是本知识库的核心索引基础。标签不是简单关键词集合，而是描述模型与**问题、任务、数据、规律、数学性质、竞赛场景及其他模型之间关系**的结构化元数据。

## 一级标签维度

| 字段 | 含义 |
|---|---|
| `problem` | 模型能够解决的问题类型 |
| `task` | 模型在完整建模流程中承担的任务 |
| `data` | 输入数据类型 |
| `pattern` | 数据中需要或能够利用的规律 |
| `structure` | 数据的统计/时间/空间/网络结构 |
| `scale` | 样本与变量规模 |
| `objective` | 优化或决策目标 |
| `constraints` | 约束条件类型 |
| `mathematics` | 数学/统计计算性质 |
| `philosophy` | 建模思想 |
| `output` | 模型输出类型 |
| `prerequisites` | 使用模型前需要满足或检查的条件 |
| `limitations` | 方法边界 |
| `risks` | 常见失效风险 |
| `competition` | 数学建模竞赛适配信息 |
| `interpretation` | 可解释性画像 |
| `relations` | 模型之间的结构关系 |

## 推荐标签词表

### Problem

`forecasting`, `prediction`, `regression`, `classification`, `risk_prediction`, `optimization`, `single_objective_optimization`, `multi_objective_optimization`, `decision`, `multi_criteria_decision`, `ranking`, `selection`, `evaluation`, `clustering`, `dimensionality_reduction`, `anomaly_detection`, `feature_selection`, `resource_allocation`, `scheduling`, `routing`, `path_planning`, `facility_location`, `transportation`, `assignment`, `inventory`, `queueing`, `dynamic_system`, `simulation`, `state_estimation`, `network_analysis`

### Task

`baseline`, `prediction`, `forecasting`, `feature_analysis`, `relationship_analysis`, `parameter_estimation`, `model_fitting`, `optimization`, `evaluation`, `ranking`, `classification`, `clustering`, `simulation`, `sensitivity_analysis`, `uncertainty_analysis`, `validation`, `diagnosis`, `interpretation`

### Data

`tabular`, `structured`, `cross_sectional`, `time_series`, `longitudinal`, `panel_data`, `event_data`, `irregular_time_series`, `spatial`, `geospatial`, `spatiotemporal`, `network`, `graph`, `text`, `image`, `signal`, `sequence`, `categorical`, `continuous`, `mixed_type`

### Pattern

`trend`, `seasonality`, `periodicity`, `autocorrelation`, `stationarity`, `nonstationarity`, `linear`, `nonlinear`, `monotonic`, `non_monotonic`, `interaction`, `high_order_interaction`, `normal`, `non_normal`, `heavy_tailed`, `skewed`, `heteroscedastic`, `multimodal`, `multicollinearity`, `sparsity`, `high_dimensionality`, `imbalance`, `dependency`

### Structure

`independent_observations`, `dependent_observations`, `hierarchical`, `nested`, `sequential`, `temporal`, `spatial_dependency`, `network_dependency`, `repeated_measurements`, `grouped_data`

### Scale

`tiny_sample`, `small_sample`, `medium_sample`, `large_sample`, `very_large_sample`, `low_dimensional`, `medium_dimensional`, `high_dimensional`, `ultra_high_dimensional`, `few_features`, `many_features`, `n_greater_than_p`, `p_greater_than_n`

> 样本规模标签只表达相对适用性，不把统一数值阈值硬编码为所有模型的绝对规则。

### Objective

`minimize_cost`, `maximize_profit`, `maximize_efficiency`, `minimize_time`, `minimize_distance`, `maximize_coverage`, `minimize_risk`, `maximize_accuracy`, `maximize_utility`, `balance_objectives`, `economic`, `environmental`, `social`, `technical`

### Constraints

`linear_constraints`, `nonlinear_constraints`, `equality_constraints`, `inequality_constraints`, `integer_constraints`, `binary_constraints`, `capacity_constraints`, `budget_constraints`, `time_constraints`, `resource_constraints`, `logical_constraints`, `spatial_constraints`, `hard_constraint`, `soft_constraint`

### Mathematics

`deterministic`, `stochastic`, `probabilistic`, `statistical`, `optimization_based`, `distance_based`, `tree_based`, `kernel_based`, `gradient_based`, `bayesian`, `frequentist`, `linear`, `nonlinear`, `convex`, `nonconvex`, `smooth`, `nonsmooth`, `continuous`, `discrete`, `global_optimization`, `local_optimization`

### Philosophy

`mechanistic`, `statistical`, `empirical`, `data_driven`, `optimization`, `simulation`, `probabilistic`, `geometric`, `graph_based`, `rule_based`, `heuristic`

### Output

`continuous_prediction`, `probability`, `class_label`, `ranking`, `score`, `optimal_solution`, `decision_variable`, `cluster_label`, `latent_representation`, `time_series_forecast`, `pareto_front`, `network_structure`

### Competition

`very_common`, `common`, `occasionally_used`, `advanced`, `rare`, `formula_friendly`, `interpretation_friendly`, `visualization_friendly`, `easy_to_explain`, `easy_to_implement`, `easy_to_validate`, `CUMCM`, `MCM`, `ICM`, `APMCM`

### Relations

`is_a`, `variant_of`, `extension_of`, `generalization_of`, `special_case_of`, `alternative_to`, `complementary_to`, `hybrid_with`, `preprocessing_for`, `diagnostic_for`, `ensemble_with`

## 标签匹配原则

知识检索至少区分三种关系：

### Hard Match

模型必须满足的必要条件。明显违反时可以淘汰候选。

### Soft Match

提高候选相关性的条件，但不是绝对要求。

### Negative Match

模型已知的适用风险、前置条件冲突或明显不匹配特征，用于降低相关性或要求额外验证。

**不要把上述机制简单实现为固定总分排行榜。** 匹配结果应保留证据，使 AI 能解释候选模型为何进入下一轮。

## 标签质量要求

每个标签必须满足至少一项实际用途：

1. 能帮助从题目识别模型；
2. 能帮助从数据报告识别模型；
3. 能区分两个容易混淆的模型；
4. 能发现模型的使用前提或风险；
5. 能建立模型之间的可解释关系。

如果一个标签不能帮助检索、筛选、比较或解释，应考虑删除，而不是为了“看起来全面”继续堆积标签。