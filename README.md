# MathModel Knowledge Base

> Problem × Data × Model — 面向 AI Agent 的数学建模竞赛知识库。

本项目不是一个全自动数学建模求解器，也不是简单的“数学模型大全”。它的目标是建立一套**结构化、可检索、可组合、AI-first**的数学建模领域知识基础设施，让 AI 在阅读竞赛题目与数据分析报告后，可以从知识库中快速定位候选模型、比较模型适用条件，并生成可交给任意 AI 的详细解题 Prompt。

## 核心工作流

```text
数学建模题目
     ↓
AI：题目结构分析
     ↓
数据分析报告（由外部数据分析平台产生）
     ↓
AI：数据特征二次分析
     ↓
本知识库：Problem × Data × Model 检索
     ↓
候选模型（通常 1~2 个核心候选）
     ↓
模型碰撞：适用条件 / 优势 / 局限 / 风险 / 竞赛适配
     ↓
AI：形成建模方案
     ↓
生成详细 Solution Prompt
     ↓
用户交给 ChatGPT / Claude / Gemini / 其他 AI 完成建模与代码
```

## 设计原则

1. **AI-first**：知识首先服务于 AI 检索与推理，而不是只服务于人工阅读。
2. **Evidence-first**：模型推荐必须有适用条件、数据依据、限制与证据，而不是孤立的模型名称。
3. **Problem × Data × Model**：模型选择同时考虑题目目标和数据结构。
4. **No blind ranking**：知识库不把模型简单做成固定分数排行榜；它提供匹配证据，由 AI 结合具体题目进行最终判断。
5. **Competition-aware**：考虑数学建模竞赛中的可解释性、公式表达、验证、可视化、论文呈现与复现性。
6. **Composable**：支持替代模型、扩展模型、互补模型和混合建模流程。
7. **可验证**：每个模型逐步补充来源、公式、适用边界、案例和实现。
8. **Case-grounded**：使用历届竞赛题目、官方结果和可合法引用的获奖/优秀论文作为案例证据，但不把获奖模型机械视为普适最优模型。

## 目录

- `schema/`：机器可读的知识结构定义
- `knowledge/`：问题类型、数据模式、建模原则、竞赛题型知识
- `models/`：标准化 Model Cards
- `relations/`：Problem–Model、Data–Model、Model–Model、Pipeline 关系
- `retrieval/`：检索与匹配组件
- `prompt_templates/`：AI 分析与 Prompt 生成规范
- `examples/`：完整检索与建模示例
- `docs/`：架构、标签体系、贡献规范

## 竞赛案例知识

`knowledge/competition_patterns/` 专门保存数学建模竞赛案例的**结构化建模模式**。案例来源包括 COMAP MCM/ICM、全国大学生数学建模竞赛等公开竞赛资源。

案例知识优先保存：题目类型、数据模式、子问题结构、模型角色、候选模型族、选择证据、验证方式、替代方案以及可迁移的建模经验；完整论文仅在明确允许再分发时进入仓库。

## AI 接入

AI 接入本仓库后，应优先阅读 [`AI_QUICK_START.md`](AI_QUICK_START.md)，再按照 `schema/` 和 `retrieval/` 的规范工作。

## 当前阶段

当前版本优先建设**知识底座与标签体系**，随后以高频数学建模模型建立第一批高质量 Model Cards，再实现本地 CLI / Python 检索器以及 MCP / API 接口。

## License

License 将在项目知识体系与贡献规范稳定后确定。
