# CUMCM A/B 题研究归档与 AI 检索流水线

> Scope: 全国大学生数学建模竞赛（CUMCM）2010–2025，优先 A/B 题。

## 1. Evidence hierarchy

1. 官方竞赛网站的赛题、数据、赛题讲评、评奖及后续研究资料
2. 官方/期刊公开的优秀论文
3. 高校或作者公开论文、代码、补充材料
4. 可靠的公开整理站点，仅作为索引入口
5. 搜索摘要、博客、论坛：只能用于发现线索，不能单独证明“论文使用了某模型”

## 2. Case extraction fields

每道 A/B 题建立 Case Card，并抽取：

- year / problem / title
- source_urls
- subproblems
- domain
- background_mechanism
- data_type / data_pattern / scale
- decision_variables
- objectives
- constraints
- assumptions
- mathematical_structure
- historical_models
- model_role（core / auxiliary / preprocessing / validation / optimization / visualization）
- parameter_estimation
- solver / algorithm
- validation
- sensitivity / robustness
- uncertainty
- model_alternatives
- limitations
- transferable_patterns
- evidence_level

## 3. Critical distinction

`historical_usage` 不等于 `recommended_model`。

某篇优秀论文使用某模型，只能证明该模型曾用于该案例；新题的模型推荐必须重新结合 Problem + Data + Pattern + Objective + Constraints + Prerequisites。

## 4. A/B priority

A/B 题优先级高于 C/D/E，原因是本知识库当前目标是形成可迁移的竞赛建模模式，而非完整复刻所有赛题。

## 5. Pattern extraction

从案例中提取可迁移模式，例如：

- inverse_problem + parameter_estimation
- time_series + forecasting
- multi_criteria_evaluation + weighting
- resource_allocation + constrained_optimization
- spatial_geometry + nonlinear_optimization
- dynamic_system + simulation/control
- sampling + statistical_decision
- physical_measurement + signal_processing + inverse_modeling

## 6. Model collision

候选模型至少保留 2 条独立路线时，比较：

- hard constraints
- soft evidence
- negative evidence
- data compatibility
- interpretability
- computational burden
- validation feasibility
- competition time constraint

最终输出 `primary_candidate` 与 `alternative_candidate`，但不把历史获奖频率直接当作模型优先级。

## 7. Current official source map

- CUMCM 官方历年赛题入口：2010–2026 可追溯。
- 官方说明显示，赛题通常来自科学工程、人文社科、经济管理等实际问题的简化，并要求提供主要问题与数据来源等信息。
- 官方资料说明，2022 年起优秀论文集转由《数学建模及其应用》出版，近年来命题人/评阅人点评文章也发表在该刊。
- 官方后续研究机制要求对优秀论文进行综述、分析现有方案不足，并提出新的模型或算法方案；这一机制可作为“模型局限/替代模型”知识的重要来源。

## 8. Do not overfit to award papers

获奖论文是历史证据，不是 ground truth。相同赛题可以存在多个合理建模路线；知识库的目标是学习“问题结构→可行模型空间”，而不是复制某一篇论文。
