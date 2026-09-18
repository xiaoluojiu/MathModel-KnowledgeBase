# 优秀论文深度抽取协议 V1.0

## 目标

将“优秀/获奖论文”从参考资料转换为可被 AI 检索的结构化建模知识，而不是建立一个 PDF 收藏夹。

## 单篇论文最小抽取单元

```yaml
case_id:
year:
contest: CUMCM
problem: A|B
paper_id:
award_level:
source:
source_type: official|award-paper|code-backed|secondary

problem_profile:
  domain:
  task_types: []
  subproblems: []

data_profile:
  data_types: []
  scale:
  temporal:
  spatial:
  noise:
  missingness:
  nonlinear:

models:
  - subproblem:
    model_id:
    role: primary|secondary|diagnostic|optimization|validation|comparison
    evidence:
    confidence:

parameters:
  - parameter:
    method:
    evidence:

validation:
  methods: []

sensitivity:
  methods: []

assumptions:
  - text:
    risk:

limitations:
  - text:

relations:
  problem_patterns: []
  data_patterns: []
  model_relations: []
  pipelines: []

transferable_knowledge:
  - pattern:
    conditions: []
    transferable_to: []

citation:
```

## 抽取顺序

### Step 1：题目层

先读取原题，确定：

- 目标变量/目标函数
- 决策变量
- 约束
- 时间/空间结构
- 子问题之间的依赖关系

### Step 2：论文层

逐题扫描：

- 模型假设
- 数学公式
- 算法名称
- 参数求解
- 数据处理
- 结果评价
- 模型检验
- 敏感性分析

### Step 3：证据层

所有“论文采用了 X 模型”的断言必须能回溯到：

- 论文正文
- 论文附录
- 官方赛题讲评
- 作者公开代码

不能仅因为 X 是该题常见解法就标成论文采用 X。

### Step 4：关系层

建立：

```text
Paper
 ↓
Subproblem
 ↓
Model
 ↓
Model Card
 ↓
Problem Pattern
 ↓
Data Pattern
```

同时记录模型在论文中的角色：

- `primary`
- `secondary`
- `optimization`
- `preprocessing`
- `diagnostic`
- `validation`
- `comparison`

### Step 5：反向知识抽取

从论文中反向发现新的标签，而不是强迫所有论文适配已有标签。

例如发现大量论文使用：

`expected_cost`、`piecewise_model`、`inverse_problem`、`trajectory_constraint`

则进入标签候选池，经审核后才进入正式 schema。

## 论文与模型的关系不能简化

错误：

```text
2023A → PSO
```

正确：

```text
2023A
 ├─ 子问题1 → optical_efficiency_model
 ├─ 子问题2 → continuous_optimization
 ├─ 子问题3 → PSO / alternative optimization
 └─ validation → simulation / sensitivity
```

## 评价标准

优秀论文不是“正确答案数据库”。它主要提供：

- 建模思路
- 模型组合
- 假设方式
- 参数求解策略
- 验证方式
- 论文表达方式
- 模型边界

知识库必须保留不同优秀论文之间的分歧。若同一题存在 A/B 两种高质量路线，不合并成唯一答案，而建立 `alternative_to` / `complementary_to` / `hybrid_with` 关系。

## 版权与归档原则

知识库优先保存**结构化事实、短摘要、模型关系和来源链接**，不默认重新分发整篇受版权保护的论文。官方公开展示论文可作为外部证据链接；必要时保存用户合法取得的原始资料到本地处理，但 GitHub 默认不提交未经许可的大体积论文原文。

## 当前来源策略

优先级：

1. 官方组委会 / 中国大学生在线。
2. 官方赛题讲评与专家解析。
3. 高校数学建模中心公开资料。
4. 作者本人公开 GitHub / 项目。
5. 可信二次整理。

搜索结果只能帮助发现资料，不能自动升级为高可信证据。
