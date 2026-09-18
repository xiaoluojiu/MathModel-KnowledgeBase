# CUMCM 2010–2025 A/B 题知识索引

> 本文件是竞赛案例知识层的总索引。目标不是保存整篇论文，而是把题目、问题结构、数据结构、候选模型、模型组合和可迁移建模模式连接到 Model Cards。
>
> **范围：仅全国大学生数学建模竞赛（CUMCM）本科组 A/B 题。**
>
> **重要：**“题目层标签”与“论文实际采用模型”必须区分。仅凭题名推断的标签标记为 `inferred`；只有从公开论文、官方赛题讲评、论文展示或可核验代码中提取的模型才标记为 `evidence-backed`。

## 1. 数据源

- CMathC 汇总页：2010–2025 优秀论文资源索引（包含百度网盘资源入口）。
- 中国大学生在线：2012–2025 年公开论文展示页面；部分年份提供 A/B 题获奖论文页面和论文图像。
- CMathC / shumo.com：历年题目索引。
- 高校数学建模中心：历年题目附件、题目原文和论文资料。
- 公开 GitHub：仅用于补充可公开核验的论文、代码、数据与模型实现。

## 2. 2010–2025 A/B 题目录与初始 Problem Pattern

| 年份 | 题号 | 题目 | 初始问题模式 | 初始模型族标签 | 状态 |
|---|---|---|---|---|---|
| 2010 | A | 储油罐的变位识别与罐容表标定 | 几何反演、参数识别、标定 | geometry, parameter_estimation, numerical_solution | inferred |
| 2010 | B | 上海世博会影响力的定量评估 | 综合评价、指标构建 | evaluation, multi_criteria_decision, statistics | inferred |
| 2011 | A | 城市表层土壤重金属污染分析 | 空间数据、污染评价、统计分析 | spatial, statistics, interpolation, evaluation | inferred |
| 2011 | B | 交巡警服务平台的设置与调度 | 网络选址、覆盖、路径、调度 | graph, facility_location, routing, optimization | inferred |
| 2012 | A | 葡萄酒的评价 | 多指标评价、主客观赋权 | evaluation, statistics, ranking | evidence-backed title + topic |
| 2012 | B | 太阳能小屋的设计 | 工程设计、能量/经济约束优化 | optimization, engineering, energy | evidence-backed title + topic |
| 2013 | A | 车道被占用对城市道路通行能力的影响 | 交通流、容量、动态系统 | traffic_flow, simulation, regression | inferred |
| 2013 | B | 碎纸片的拼接复原 | 图像/边缘匹配、组合优化 | image, matching, combinatorial_optimization | inferred |
| 2014 | A | 嫦娥三号软着陆轨道设计与控制策略 | 动力学、轨迹优化、最优控制 | differential_equation, optimal_control, optimization | inferred |
| 2014 | B | 创意平板折叠桌 | 几何设计、结构约束、优化 | geometry, design_optimization, constraints | inferred |
| 2015 | A | 太阳影子定位 | 几何反演、时空定位、参数估计 | geometry, inverse_problem, parameter_estimation | inferred |
| 2015 | B | “互联网+”时代的出租车资源配置 | 需求预测、空间/时间配置、优化 | forecasting, allocation, optimization, spatiotemporal | inferred |
| 2016 | A | 系泊系统的设计 | 力学、几何约束、工程优化 | mechanics, geometry, constrained_optimization | evidence-backed topic |
| 2016 | B | 小区开放对道路通行的影响 | 交通网络、仿真、容量/路径分析 | graph, traffic, simulation, optimization | inferred |
| 2017 | A | CT系统参数标定及成像 | 逆问题、参数估计、成像重建 | inverse_problem, parameter_estimation, imaging | inferred |
| 2017 | B | “拍照赚钱”的任务定价 | 定价、激励、空间分配、预测 | pricing, optimization, regression, spatial | inferred |
| 2018 | A | 高温作业专用服装设计 | 热传递、动态系统、设计优化 | differential_equation, simulation, optimization | inferred |
| 2018 | B | 智能RGV的动态调度策略 | 动态调度、排队/任务分配 | scheduling, dynamic_optimization, simulation | inferred |
| 2019 | A | 高压油管的压力控制 | 动力学、微分方程、控制、数值计算 | ode, control, numerical_method, optimization | evidence-backed from public paper/code |
| 2019 | B | “同心协力”策略研究 | 博弈/策略、概率、组合决策 | game_theory, probability, strategy | inferred |
| 2020 | A | 炉温曲线 | 动态系统、热过程、参数拟合/控制 | ode, curve_fitting, simulation, optimization | inferred |
| 2020 | B | 穿越沙漠 | 路径规划、资源约束、动态决策 | routing, dynamic_programming, optimization | inferred |
| 2021 | A | “FAST”主动反射面的形状调节 | 几何/结构、非线性优化、参数控制 | geometry, nonlinear_optimization, parameter_estimation | inferred |
| 2021 | B | 乙醇偶合制备 C4 烯烃 | 化学反应动力学、回归、优化 | kinetics, regression, optimization | inferred |
| 2022 | A | 波浪能最大输出功率设计 | 物理动力学、功率优化、数值求解 | mechanics, simulation, optimization | evidence-backed topic |
| 2022 | B | 无人机遂行编队飞行中的纯方位无源定位 | 几何定位、轨迹估计、非线性优化 | localization, geometry, trajectory, optimization | evidence-backed topic |
| 2023 | A | 定日镜场的优化设计 | 几何/光学、目标函数、组合/连续优化 | geometry, optics, optimization, metaheuristic | evidence-backed from public GitHub papers |
| 2023 | B | 多波束测线问题 | 几何覆盖、测线规划、优化 | geometry, coverage, routing, optimization | inferred + public solution ecosystem |
| 2024 | A | “板凳龙”闹元宵 | 螺线运动、动力学、碰撞检测、路径优化 | kinematics, geometry, simulation, optimization | evidence-backed topic |
| 2024 | B | 生产过程中的决策问题 | 抽样检测、贝叶斯/概率决策、生产策略 | decision, probability, quality_control, optimization | evidence-backed topic |
| 2025 | A | 烟幕干扰弹的投放策略 | 三维运动学、遮蔽几何、约束优化 | kinematics, geometry, simulation, constrained_optimization | evidence-backed topic |
| 2025 | B | 碳化硅外延层厚度的确定 | 干涉光学、参数反演、非线性拟合 | inverse_problem, optics, nonlinear_regression, parameter_estimation | evidence-backed topic |

## 3. 历史题型的可迁移 Pattern

### A 类工程/物理/几何问题

常见链条：

```text
物理背景
→ 合理假设
→ 几何/微分方程/守恒关系
→ 参数识别
→ 数值求解
→ 约束优化
→ 敏感性/误差分析
```

高频标签：

`mechanistic` `geometry` `differential_equation` `parameter_estimation` `simulation` `constrained_optimization` `numerical_method`

### B 类管理/资源/决策问题

常见链条：

```text
数据清洗
→ 需求/概率/指标建模
→ 决策变量
→ 目标函数
→ 约束
→ 优化/评价
→ 情景分析
```

高频标签：

`decision` `allocation` `scheduling` `evaluation` `forecasting` `optimization` `probability` `simulation`

## 4. 重点历史案例关系

### 2019 A：高压油管的压力控制

公开一等奖论文/代码资料显示，该题使用了高压油管压力变化的微分方程/差分模型，并结合拟合、插值、数值计算和控制策略；公开 GitHub 项目还提供论文、代码和数据。该案例应连接到：

- `ordinary_differential_equation`
- `curve_fitting`
- `piecewise_interpolation`
- `finite_difference`
- `control_strategy`
- `numerical_solution`
- `optimization`

### 2023 A：定日镜场的优化设计

公开一等奖项目提供论文、答辩 PPT、代码和数据；其公开代码使用 PSO 等优化程序。该案例应连接：

- `geometry`
- `optics`
- `simulation`
- `objective_function`
- `particle_swarm_optimization`
- `continuous_optimization`
- `multi_stage_optimization`

### 2024 A：板凳龙

官方赛题讲评体系明确将其作为复杂运动/优化问题进行讲解；题目核心包括节点位置、速度、运动轨迹、碰撞/路径等。应连接：

- `kinematics`
- `parametric_curve`
- `spiral`
- `collision_detection`
- `simulation`
- `trajectory_optimization`

### 2024 B：生产过程中的决策问题

官方赛题讲评体系将其作为生产过程中的决策问题；公开资料显示涉及零配件/成品检测与退回等多阶段决策。应连接：

- `decision_tree`
- `probabilistic_decision`
- `quality_control`
- `expected_cost`
- `dynamic_decision`
- `optimization`

### 2025 A：烟幕干扰弹的投放策略

公开赛题资料显示该题涉及三维运动与投放策略优化；知识库中应作为 `kinematics × geometry × constrained_optimization` 的高价值案例，而不是简单标记为“遗传算法题”。

### 2025 B：碳化硅外延层厚度

该题应作为 `interference_model × inverse_problem × nonlinear_parameter_estimation` 的典型案例。核心知识价值在于：**先建立物理观测模型，再反演参数，而不是直接套用回归算法。**

## 5. 证据等级

- `official`: 竞赛组委会/中国大学生在线/官方赛题讲评直接证据。
- `award-paper`: 可核验优秀/获奖论文正文证据。
- `code-backed`: 公开代码仓库可复现模型证据。
- `secondary`: 高校、教学中心、公开资料整理。
- `inferred`: 仅由题目结构推断，不能作为“获奖论文实际使用模型”的证据。

## 6. 下一步提取要求

对每一篇可获取的 A/B 优秀论文，必须抽取：

1. 题目与子问题映射。
2. 每个子问题的实际模型。
3. 模型前置假设。
4. 输入数据与数据特征。
5. 参数估计方法。
6. 优化算法及其角色。
7. 验证方法。
8. 敏感性/稳健性分析。
9. 模型替代路线。
10. 论文中明确指出的优点/不足。
11. 可迁移 Problem Pattern。
12. 对应 Model Card ID。
13. 原始来源和证据等级。

**禁止把“网上常见解法”写成“获奖论文实际采用方法”。**
