# 综述、系统与基础设施

> 主题簇 · `survey-infra` · 3 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

领域地图、系统集成、数据检索与安全护栏；用于定位与背景，不提供核心方法证据。

## 代表论文

### [`talemi-survey`](../papers/talemi-survey.md) — Agentic AI in Remote Sensing: Foundations, Taxonomy, and Emerging Systems

综述给出 agentic RS 的统一 taxonomy：单 agent copilot vs 多 agent 系统；它把规划机制、检索增强生成与记忆结构作为架构分析主轴。

[打开卡片](../papers/talemi-survey.md) · 2026 · WACV 2026 Workshop (GeoCV)

### [`space-air-ground`](../papers/space-air-ground.md) — Integration and Intelligent Monitoring Technology System of Space-Air-Ground Remote Sensing

论文把空天地遥感的挑战归为多模态数据治理不足、解译泛化不足与应用协同不足；体系含三条主线：标准化数据处理与跨源检索、组件化多任务解译、基于多模态大模型的应用 agent。

[打开卡片](../papers/space-air-ground.md) · 2026 · ISPRS Archives XLIX-B1-2026

### [`risk-aware`](../papers/risk-aware.md) — Risk-Aware LLM Agents for Geospatial Data Retrieval

系统目标是让用户用自然语言从云目录检索卫星/环境数据，而不是直接写 API；三角色分工把安全护栏、意图解释与 schema 感知的调用生成拆开，模块可通过 API schema 替换迁移。

[打开卡片](../papers/risk-aware.md) · 2026 · ISPRS Archives XLIX-B3-2026

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |

## 共同能力边界

- 综述/系统/基础设施不提供核心方法增益的实验证据。
- workshop 或系统论文必须标清会址，不得升格为主会方法论文。
- 系统愿景与初步对抗评测不能写成生产级可靠性。
- 检索/安全/数据治理是重要约束，但不等于灾害工具规划。

## 写作时何时进入

写引言、related work、领域地图、系统架构、数据检索/安全背景时进入。具体方法与数字回到原论文卡片。
