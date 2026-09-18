# AI Quick Start

本文件是给接入本仓库的 AI Agent 阅读的第一入口。

## 你的任务

本知识库用于辅助数学建模竞赛中的**模型识别与模型选择**。你不是被要求机械地从库中挑一个模型，而是要把：

```text
题目 Problem
数据 Data
模型 Model
```

连接起来。

## 标准流程

### Step 1：分析题目

从题目中提取：

- 研究对象
- 子问题
- 目标变量
- 决策变量
- 预测/优化/评价/分类等任务
- 目标函数
- 约束条件
- 是否存在时间、空间、网络、层级结构
- 题目要求的输出

### Step 2：读取数据分析报告

不要要求用户把大型原始数据全部发送给你。优先使用数据分析报告提取：

- 样本量与维度
- 变量类型
- 缺失值与异常值
- 分布特征
- 相关性与共线性
- 时间序列特征
- 空间/网络结构
- 非线性与交互
- 类别不平衡
- 数据规模
- 已完成的预处理

### Step 3：形成 Problem × Data Profile

将题目需求和数据事实分别结构化，不要把题目中的假设误当成数据事实。

### Step 4：检索知识库

按照 `schema/` 中定义的字段检索候选模型。优先使用：

- problem
- task
- data
- pattern
- structure
- scale
- objective
- constraints
- prerequisites
- competition

### Step 5：筛选 1~2 个核心候选

知识库可以返回多个候选，但最终建模分析通常聚焦 1~2 个核心模型，避免把候选列表变成“模型大杂烩”。

### Step 6：模型碰撞

对候选模型逐项比较：

- Problem Match
- Data Match
- Pattern Match
- Prerequisite Match
- Competition Fit
- Interpretability
- Strengths
- Limitations
- Risks
- Computational Considerations

不得仅依据固定分数得出结论。

### Step 7：形成建模建议

明确：

- Primary Model
- Secondary / Alternative Model（如确有必要）
- 为什么适合
- 哪些条件仍需验证
- 哪些结果可以作为对照
- 是否存在合理的混合模型方案

### Step 8：生成 Solution Prompt

输出一个可以直接复制给其他 AI 的详细 Prompt。Prompt 至少应包含：

1. 题目背景
2. 子问题拆解
3. 数据事实
4. 推荐模型及标签
5. 模型选择依据
6. 数学假设
7. 建模要求
8. 参数确定方法
9. 验证与误差分析
10. 敏感性 / 稳健性分析
11. 可视化要求
12. Python 实现要求
13. 数学建模论文写作要求
14. 禁止未经依据随意换模型的约束

## 重要规则

- **不要把知识库标签当成绝对真理。** 标签用于检索和提供证据。
- **不要因为模型常见就认为它适合。** 必须结合题目与数据。
- **不要为了“先进”而优先深度学习。** 竞赛中模型选择需要考虑数据、解释性和可复现性。
- **不要把 SHAP、交叉验证、ADF 等诊断/解释工具误认为预测模型。** 它们应通过 `task` / `prerequisites` / `diagnostic` 等字段表达。
- **不要输出没有依据的唯一正确模型。** 在存在明显不确定性时说明验证步骤。

## 推荐读取顺序

```text
AI_QUICK_START.md
        ↓
schema/model.schema.json
schema/problem.schema.json
schema/data.schema.json
schema/relation.schema.json
        ↓
docs/tagging_system.md
        ↓
models/ + relations/
```
