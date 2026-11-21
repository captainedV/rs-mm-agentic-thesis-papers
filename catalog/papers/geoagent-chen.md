# An LLM Agent for Automatic Geospatial Data Analysis

> 论文卡片 · `geoagent-chen` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | An LLM Agent for Automatic Geospatial Data Analysis |
| 作者 | Yuxing Chen; Weijie Wang; Sylvain Lobry; Camille Kurtz |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2410.18792）；会址待确认 |
| arXiv | [arXiv:2410.18792](https://arxiv.org/abs/2410.18792) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2410.18792) |
| Bib key | `geoagent-chen`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2024-arXiv-GeoAgent-Chen.pdf`](../../pdfs/2024-arXiv-GeoAgent-Chen.pdf) |
| 代码 / 项目 | https://github.com/Yusin2Chen/GeoAgent |
| 数据集 | GeoCode |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

GeoAgent 把代码解释器、静态分析、RAG 与 Monte Carlo Tree Search 组合起来，帮助 LLM 处理带空间约束和多函数调用的地理空间数据分析，并配套 GeoCode 基准。

## 核心结论

- 论文指出 LLM 直接写地理空间代码会在复杂顺序任务、空间约束和冷门库上产生逻辑错误与幻觉。 [摘要]
- GeoAgent 用代码解释器执行、静态分析纠错、RAG 补库知识，并用 MCTS 搜索多步代码方案。 [摘要]
- 配套基准覆盖数据获取、分析与可视化，含单轮和多轮任务，强调真实 Python 库与函数调用。 [摘要]
- 结论是仅靠 LLM 内置知识不足以完成准确的地理空间编程，必须把执行反馈纳入循环。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

这是地理空间数据分析代码 agent，不是卫星影像工具规划；没有灾害、SAR 或检测/分割工具链。不能把 GeoCode 结果当作 RS agent 的通用分数。会址按预印本处理。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`univearth`](univearth.md) — Towards LLM Agents for Earth Observation
- [`rs-agent`](rs-agent.md) — RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows

## 何时必须打开全文

需要 MCTS 的节点定义、静态分析规则、GeoCode 的库/函数分布与多轮任务评分时。
