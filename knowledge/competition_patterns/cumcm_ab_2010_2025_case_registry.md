# CUMCM A/B 题 2010–2025 Case Registry

> Scope: 全国大学生数学建模竞赛（CUMCM）2010–2025，仅 A/B。
> 本文件是**案例注册表**，不是把搜索摘要当作论文结论。`historical_models` 必须在论文/官方讲评核验后再提升证据等级。

## Evidence status

- `official_problem`: 官方赛题可追溯
- `paper_indexed`: 已找到论文展示/论文索引入口
- `method_verified`: 模型已由论文或官方讲评核验
- `pattern_inferred`: 根据题目结构推导出的候选 Pattern，不能冒充历史论文事实

## 2010–2017

| Year | Problem | Title | Problem Pattern (initial) | Data/Structure | Status |
|---|---|---|---|---|---|
| 2010 | A | 储油罐的变位识别与罐容表标定 | geometry + inverse_problem + parameter_estimation | geometric measurement | official_problem; pattern_inferred |
| 2010 | B | 2010年上海世博会影响力的定量评估 | multi_criteria_evaluation + statistical_analysis | socio-economic indicators | official_problem; pattern_inferred |
| 2011 | A | 城市表层土壤重金属污染分析 | spatial_analysis + pollution_assessment + statistical_analysis | spatial/environmental measurements | official_problem; pattern_inferred |
| 2011 | B | 交巡警服务平台的设置与调度 | network + location_allocation + scheduling | road/network + demand | official_problem; pattern_inferred |
| 2012 | A | 葡萄酒的评价 | multi_criteria_evaluation + statistical_analysis | sensory/chemical indicators | official_problem; pattern_inferred |
| 2012 | B | 太阳能小屋的设计 | physical_model + simulation + optimization | energy/environment parameters | official_problem; pattern_inferred |
| 2013 | A | 车道被占用对城市道路通行能力的影响 | traffic_flow + simulation + capacity_analysis | traffic observations | official_problem; pattern_inferred |
| 2013 | B | 碎纸片的拼接复原 | image_processing + combinatorial_optimization + reconstruction | image/fragments | official_problem; pattern_inferred |
| 2014 | A | 嫦娥三号软着陆轨道设计与控制策略 | dynamical_system + trajectory_optimization + control | physical constants/trajectory | official_problem; pattern_inferred |
| 2014 | B | 创意平板折叠桌 | geometry + structural_design + optimization | geometric constraints | official_problem; pattern_inferred |
| 2015 | A | 太阳影子定位 | geometry + inverse_problem + parameter_estimation | shadow observations | official_problem; pattern_inferred |
| 2015 | B | “互联网+”时代的出租车资源配置 | resource_allocation + demand_model + optimization | spatial-temporal demand | official_problem; pattern_inferred |
| 2016 | A | 系泊系统的设计 | physical_model + simulation + constrained_optimization | wind/wave/current + structure | official_problem; pattern_inferred |
| 2016 | B | 小区开放对道路通行的影响 | traffic_flow + network + simulation | road network + traffic | official_problem; pattern_inferred |
| 2017 | A | CT系统参数标定及成像 | inverse_problem + image_reconstruction + parameter_estimation | projection/image data | official_problem; pattern_inferred |
| 2017 | B | “拍照赚钱”的任务定价 | clustering + regression + multi_objective_optimization | task/location/user data | official_problem; pattern_inferred |

## 2018–2025

| Year | Problem | Title | Problem Pattern (initial) | Data/Structure | Status |
|---|---|---|---|---|---|
| 2018 | A | 高温作业专用服装设计 | heat_transfer + PDE + multi_objective_optimization | thermal/material parameters | official_problem; pattern_inferred |
| 2018 | B | 智能RGV的动态调度策略 | scheduling + discrete_optimization + simulation | job/queue/state data | official_problem; pattern_inferred |
| 2019 | A | 高压油管的压力控制 | ODE + dynamic_system + parameter_estimation + optimization | pressure/time measurements | official_problem; pattern_inferred |
| 2019 | B | “同心协力”策略研究 | rigid_body_dynamics + collision + simulation + optimization | physical geometry/motion | official_problem; pattern_inferred |
| 2020 | A | 炉温曲线 | heat_transfer + numerical_method + inverse_problem | temperature/time measurements | official_problem; pattern_inferred |
| 2020 | B | 穿越沙漠 | dynamic_programming + combinatorial_optimization + game_theory | route/resources | official_problem; pattern_inferred |
| 2021 | A | 生产设备的数字化管理 | time_series + anomaly_detection + maintenance_decision | equipment sensor data | official_problem; pattern_inferred |
| 2021 | B | 生产企业原材料的订购与运输 | inventory + transportation + optimization | demand/cost/logistics | official_problem; pattern_inferred |
| 2022 | A | 波浪能最大输出功率设计 | physical_model + numerical_simulation + optimization | wave/device parameters | official_problem; pattern_inferred |
| 2022 | B | 无人机辅助通信 | geometry + coverage + optimization + simulation | spatial/trajectory/network data | official_problem; pattern_inferred |
| 2023 | A | 定日镜场的优化设计 | geometry + physical_model + nonlinear_optimization | heliostat geometry/solar data | official_problem; pattern_inferred |
| 2023 | B | 多波束测线问题 | geometry + coverage + path_planning + optimization | bathymetry/coverage data | official_problem; pattern_inferred |
| 2024 | A | 板凳龙 | geometry + kinematics + collision_detection + constrained_optimization | spiral/trajectory geometry | official_problem; pattern_inferred |
| 2024 | B | 生产过程中的决策问题 | sampling + hypothesis_testing + sequential_decision + expected_cost | quality sampling | official_problem; pattern_inferred |
| 2025 | A | 烟幕干扰弹的投放策略 | kinematics + geometry + constrained_optimization | trajectories/constraints | official_problem; pattern_inferred |
| 2025 | B | 碳化硅外延层厚度的确定 | signal_processing + interference + inverse_problem + nonlinear_least_squares | spectral/interference measurements | official_problem; pattern_inferred |

## Immediate verified model anchors

以下只登记当前检索中已有较强公开证据的锚点；其余案例必须逐篇论文/讲评核验后再提升：

- 2017B：聚类分析、回归分析、多目标规划可作为公开资料中的方法线索。
- 2018A：热传导方程、有限差分、多目标/单目标优化可作为方法线索。
- 2018B：0-1 规划、启发式/非线性优化是公开资料中常见路线。
- 2019A：数据预处理、常微分方程、优化/数值方法有公开解析线索。
- 2019B：动力学方程、碰撞、模拟退火等有公开解析线索。
- 2020A：热传导、有限差分、遍历/搜索是公开解析线索。
- 2020B：组合优化、数学规划、动态规划、启发式算法、博弈/Nash 均有公开解析线索。
- 2025A/B：公开资料中分别出现几何/运动学/约束优化，以及干涉、FFT、非线性拟合等路线；需以论文或官方讲评逐项核验。

## Sources

- 官方历年赛题入口：https://www.mcm.edu.cn/html_cn/block/8579f5fce999cdc896f78bca5d4f8237.html
- CMathC 2010–2025 优秀论文索引：https://www.cmathc.org.cn/mcm/lw/530.html
- CMathC 2010–2025 赛题汇总：https://www.cmathc.org.cn/mcm/st/607.html
- 中国大学生在线数学建模论文/讲评入口：https://dxs.moe.gov.cn/zx/hd/sxjm/dwdxxsxjm/dwdxxsxjm-qgdxssxjmjsAt.shtml
- 公开真题 GitHub 镜像（仅作为资料索引/下载入口）：https://github.com/CosmicLinks/cumcm-problems

## Next extraction rule

本注册表中的 `pattern_inferred` 不能直接进入 AI 的 `recommended_model` 结论。下一步必须建立逐题 Case Card，并把论文证据、官方讲评、模型角色和模型标签分别记录，再生成 `problem_model_edges`。