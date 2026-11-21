# GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots

> 论文卡片 · `geollm-engine` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **背景文献**

| 字段 | 值 |
| --- | --- |
| 标题 | GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots |
| 作者 | Simranjit Singh; Michael Fore; Dimitrios Stamoulis |
| 年份 | 2024 |
| 会址 / 状态 | CVPR 2024 Workshop (EarthVision) |
| arXiv | [arXiv:2404.15500](https://arxiv.org/abs/2404.15500) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2404.15500) |
| Bib key | `geollm-engine`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-CVPRW-GeoLLM-Engine-Singh.pdf`](../../pdfs/2024-CVPRW-GeoLLM-Engine-Singh.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | geospatial copilot workflows |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

真实感地理空间 Copilot 环境：提供地理空间 API 工具、动态地图/UI 与外部多模态知识库，用大规模并行任务生成评估 agent 对真实分析师指令的理解与功能正确性。

## 核心结论

- GeoLLM-Engine 针对既有 agent 评测任务过于简化、提示模板化的问题，构造更真实的分析师工作流。 [摘要]
- 环境含地理空间 API、动态地图/UI 与外部多模态知识库，强调功能正确性而非只匹配答案文本。 [摘要]
- 它通过大规模并行任务生成降低人工构造 benchmark 的开销。 [摘要]
- 它是环境/评测基础设施，不是规划算法；后续 GeoLLM-Squad 以其为底座。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能单独支撑“多 agent 更好”或某个规划策略；workshop 论文，范围有限。不能把环境能力当作模型能力。

## 与主张的关系

**背景文献**。这篇提供背景、系统或评测基础设施，不能作为核心方法增益的直接证据。

## 相关论文

- [`geollm-squad`](geollm-squad.md) — Multi-Agent Geospatial Copilots for Remote Sensing Workflows
- [`eval-tool-agents`](eval-tool-agents.md) — Evaluating Tool-Augmented Agents in Remote Sensing Platforms
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 API 集合、UI 状态表示、任务生成与功能正确性判定时。
