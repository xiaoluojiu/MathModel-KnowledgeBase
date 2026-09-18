# CUMCM 2024 A/B 论文正文提取批次

## 目的

本文件记录 2024 A/B 题优秀论文正文提取的第一批结构化结果。官方论文展示页以逐页图片形式发布；本批次只把能够由正文证据确认的内容标记为 historical_usage，其余保持为 pattern_inferred。

## A题：板凳龙

### Problem Pattern
- parameterized_geometry
- kinematics
- recursive_body_motion
- collision_detection
- trajectory_constraint
- constrained_optimization

### Data Pattern
- geometric_parameters
- time_series_positions
- velocity_constraints
- collision_distance

### Typical model roles
- 螺线/曲线参数化：mechanistic_geometry
- 弧长参数与运动学关系：state_evolution
- 龙头轨迹：ODE / numerical integration
- 龙身位置递推：recursive_geometry
- 板凳间碰撞：geometric_collision_detection
- 最小螺距/最大速度：constrained_optimization

### Retrieval tags
`geometry`, `kinematics`, `trajectory`, `recursive`, `collision`, `constraint`, `optimization`, `simulation`

### Negative match
- 不应仅因为存在时间变量就直接判定为 time_series_forecasting。
- 不应把遗传算法/PSO等求解器本身当作问题模型。
- 若碰撞约束可解析表达，应优先识别几何约束，再选择优化器。

## B题：生产过程决策

### Problem Pattern
- quality_control
- sequential_decision
- sampling
- hypothesis_testing
- expected_cost
- dynamic_decision

### Data Pattern
- defect_rate
- sample_observations
- inspection_cost
- replacement_loss
- decision_cost

### Typical model roles
- 抽样统计：statistical_inference
- 假设检验：decision_rule
- 检测/拆解/调换策略：decision_optimization
- 期望成本：objective_function
- 多阶段决策：sequential/dynamic_decision

### Retrieval tags
`sampling`, `hypothesis_testing`, `quality_control`, `decision`, `expected_cost`, `sequential`, `dynamic`

### Negative match
- 不应看到“质量”就直接检索回归模型。
- 不应把蒙特卡洛作为默认主模型；只有存在复杂随机过程且解析计算困难时才进入候选。
- 若决策空间有限，应优先枚举/动态决策/整数优化，再考虑启发式算法。

## 官方证据入口
- 2024 A题论文展示：A053、A016、A163、A178、A242等官方页面。
- 2024 B题论文展示：B159、B195、B196等官方页面。

## 质量规则
1. historical_usage 必须有论文正文或可靠全文镜像证据。
2. pattern_inferred 不得升级为 historical_usage。
3. 模型、算法、求解器、验证方法必须分离。
4. 同一问题的不同论文路线保留为 alternatives，不强行合并。

## Sources
- 中国大学生在线 2024 A题论文展示：官方竞赛论文页面。
- 中国大学生在线 2024 B题论文展示：官方竞赛论文页面。
