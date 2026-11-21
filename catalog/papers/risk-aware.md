# Risk-Aware LLM Agents for Geospatial Data Retrieval

> 论文卡片 · `risk-aware` · 主题簇 [综述、系统与基础设施](../clusters/survey-infra.md) · 关系 **背景文献**

| 字段 | 值 |
| --- | --- |
| 标题 | Risk-Aware LLM Agents for Geospatial Data Retrieval |
| 作者 | Kyle Gao; Joel Cumming; Jonathan Li; Linlin Xu; David Clausi |
| 年份 | 2026 |
| 会址 / 状态 | ISPRS Archives XLIX-B3-2026 |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · 仓库未记录 |
| Bib key | `risk-aware`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-ISPRS-RiskAware-Gao.pdf`](../../pdfs/2026-ISPRS-RiskAware-Gao.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | catalog retrieval / API generation |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向云地理空间目录的 LLM 数据检索框架：把自然语言意图转成结构化 API 调用，含 Guardrail（安全/策略）、General-QA（意图解释）、Recommender-Analyst（schema 感知的 API 生成）三个 agent。

## 核心结论

- 系统目标是让用户用自然语言从云目录检索卫星/环境数据，而不是直接写 API。 [摘要]
- 三角色分工把安全护栏、意图解释与 schema 感知的调用生成拆开，模块可通过 API schema 替换迁移。 [摘要]
- 论文报告了对抗性多轮场景下的初步评测，强调安全与政策约束。 [摘要]
- 它属于数据检索/基础设施，不是灾害影像的工具规划或后训练。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2 的核心增益；初步对抗评测不能当作生产级安全证明。没有灾害端到端任务或轨迹监督。

## 与主张的关系

**背景文献**。这篇提供背景、系统或评测基础设施，不能作为核心方法增益的直接证据。

## 相关论文

- [`space-air-ground`](space-air-ground.md) — Integration and Intelligent Monitoring Technology System of Space-Air-Ground Remote Sensing
- [`talemi-survey`](talemi-survey.md) — Agentic AI in Remote Sensing: Foundations, Taxonomy, and Emerging Systems
- [`geoagent-chen`](geoagent-chen.md) — An LLM Agent for Automatic Geospatial Data Analysis

## 何时必须打开全文

需要 API schema 替换机制、Guardrail 规则、对抗评测设置时。
