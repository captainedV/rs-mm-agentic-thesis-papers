# An LLM-based multi-agent system for remote sensing analysis

> 论文卡片 · `expertsrs` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | An LLM-based multi-agent system for remote sensing analysis |
| 作者 | Sun et al.（仓库仅记录短作者，未展开） |
| 年份 | 2026 |
| 会址 / 状态 | Big Earth Data |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178) |
| Bib key | `expertsrs`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | **缺失**（见 [`missing-pdfs.md`](../../missing-pdfs.md)） |
| 代码 / 项目 | 无记录 |
| 数据集 | 遥感分析工作流 |
| 核对状态 | 仅元数据，未核正文 |
| 引用注意 | 缺全文：`missing-pdfs.md` 记录 Taylor & Francis 可能需订阅，未发现开放预印本。 |

## 问题与方法

面向非专家用户的 Data–Tools–Brain 多 agent 系统，把含糊的自然语言查询转成可执行的遥感分析流程；原型使用 AutoGen 与 DeepSeek-V3。

## 核心结论

- 论文提出 Data–Tools–Brain 三角色多 agent，目标用户是不会写遥感处理流程的非专家。 [papers.json 摘要要点；未核正文]
- 系统把含糊查询拆成数据、工具与推理角色，再组装为可执行分析流程。 [papers.json 摘要要点；未核正文]
- 仓库未收录开放全文，也未发现可核的导航仓库；以下判断只能停在元数据与公开摘要层面。 [papers.json 摘要要点；未核正文]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能引用具体实验数字、消融或工具调用协议；不能把这套系统与 Earth-Agent/DORA 的分数比较；不能声称其已复现。

## 与主张的关系

**P1 模态–工具规划**。仅元数据，未核正文；即使主题相关，也不能作为已核证据引用。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows
- [`openearthagent-shabbir`](openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents
- [`openearth-agent-zhao`](openearth-agent-zhao.md) — OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation

## 何时必须打开全文

在获得 Taylor & Francis 正式版或作者预印本之前，不应把任何方法细节写进正文；若必须引用，只能按正式页摘要作背景。
