# RAVEN: A Rapid Agentic Vision Framework for Emergency Response in Vulnerable Settlements

> 论文卡片 · `raven` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **背景文献**

| 字段 | 值 |
| --- | --- |
| 标题 | RAVEN: A Rapid Agentic Vision Framework for Emergency Response in Vulnerable Settlements |
| 作者 | Arkadip Maitra; Suvajit Patra; Sumantro Mukherjee |
| 年份 | 2026 |
| 会址 / 状态 | WACV 2026 Workshop (GeoCV) |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · 仓库未记录 |
| Bib key | `raven`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-WACVW-RAVEN-Maitra.pdf`](../../pdfs/2026-WACVW-RAVEN-Maitra.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | 无记录 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向脆弱定居点/难民营应急评估的 agentic 视觉框架：LLM 编排器协调屋顶分割等专用 CV 工具，从航空/卫星影像自动评估定居点状况。

## 核心结论

- RAVEN 针对难民营规模大、人工评估慢的问题，用 LLM 编排分割等视觉工具。 [摘要]
- 单个难民营可超过 20 km²、含数万栋建筑，说明任务规模与自动化需求。 [摘要]
- 它是应急应用案例，展示工具编排在真实人道场景的潜力。 [摘要]
- 但它是 WACV 2026 Workshop 论文，范围窄，未提供通用工具规划基准。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 20 km²+ | 单个难民营规模示例 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能写成主会录用或通用 agent 方法；不能支撑 P1/P2 的机制性结论。没有多传感器切换或轨迹后训练。

## 与主张的关系

**背景文献**。这篇提供背景、系统或评测基础设施，不能作为核心方法增益的直接证据。

## 相关论文

- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`rescueadi`](rescueadi.md) — RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents
- [`risk-aware`](risk-aware.md) — Risk-Aware LLM Agents for Geospatial Data Retrieval
- [`eo-gym`](eo-gym.md) — EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents

## 何时必须打开全文

需要工具清单、编排逻辑、评估指标与定居点数据时。
