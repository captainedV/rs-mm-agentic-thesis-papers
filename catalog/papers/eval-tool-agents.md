# Evaluating Tool-Augmented Agents in Remote Sensing Platforms

> 论文卡片 · `eval-tool-agents` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **背景文献**

| 字段 | 值 |
| --- | --- |
| 标题 | Evaluating Tool-Augmented Agents in Remote Sensing Platforms |
| 作者 | Simranjit Singh; Michael Fore; Dimitrios Stamoulis |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2405.00709）；会址按预印本 |
| arXiv | [arXiv:2405.00709](https://arxiv.org/abs/2405.00709) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2405.00709) |
| Bib key | `eval-tool-agents`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-arXiv-EvaluatingToolAgents-Singh.pdf`](../../pdfs/2024-arXiv-EvaluatingToolAgents-Singh.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RS platform tool evaluation |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

GeoLLM-QA 基准：在真实 UI 平台上记录长序列的语言、视觉与点击动作，评测工具增强 LLM 对“这里”这种由系统状态隐含指代的真实任务。

## 核心结论

- 论文指出既有 benchmark 假设图文模板已硬编码“这里”，忽略了地图缩放/框选等系统状态。 [摘要]
- GeoLLM-QA 记录语言、视觉与点击组成的长动作序列，更接近分析师真实操作。 [摘要]
- 它评测 SOTA LLM 在真实 UI 平台上的工具使用，暴露状态接地问题。 [摘要]
- 这是早期评测基础设施，不是灾害或轨迹后训练方法。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

workshop 论文；不能支撑 P1/P2 的增益结论。任务范围与规模有限，不能外推为通用 RS agent 评测。

## 与主张的关系

**背景文献**。这篇提供背景、系统或评测基础设施，不能作为核心方法增益的直接证据。

## 相关论文

- [`geollm-engine`](geollm-engine.md) — GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots
- [`geollm-squad`](geollm-squad.md) — Multi-Agent Geospatial Copilots for Remote Sensing Workflows
- [`risk-aware`](risk-aware.md) — Risk-Aware LLM Agents for Geospatial Data Retrieval
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要动作空间、UI 状态编码、任务评分与模型结果时。
