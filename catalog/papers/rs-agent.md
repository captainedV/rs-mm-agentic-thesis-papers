# RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent

> 论文卡片 · `rs-agent` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent |
| 作者 | Wenjia Xu; Zijian Yu; Boyang Mu; Jiuniu Wang; Zhiwei Wei; Mugen Peng |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2406.07089）；正文有 Science China Information Sciences 2025 卷线索，期刊页待交叉确认 |
| arXiv | [arXiv:2406.07089](https://arxiv.org/abs/2406.07089) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2406.07089) |
| Bib key | `rs-agent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-arXiv-RS-Agent-Xu.pdf`](../../pdfs/2024-arXiv-RS-Agent-Xu.pdf) |
| 代码 / 项目 | https://github.com/IntelliSensing/RS-Agent |
| 数据集 | RSSDIVCS, RSVQA, DOTA |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 正文提到 Science China Information Sciences 2025 卷线索，但期刊页未交叉确认；按预印本处理。 |

## 问题与方法

以 LLM 中央控制器理解意图并规划，配合动态工具包、任务级专家方案空间与领域知识空间；用 Task-Aware Retrieval 和 DualRAG 改善工具链与知识检索。

## 核心结论

- RS-Agent 把 RS 工作流拆成中央控制器、动态工具包、Solution Space 与 Knowledge Space 四部分，是早期“规划 + 工具编排”的代表。 [摘要]
- Task-Aware Retrieval 先推断任务类型再检索专家流程，避免只按查询相似度拼工具链。 [摘要]
- DualRAG 用双路径加权检索补足领域知识的相关性与完整性。 [摘要]
- 系统原生支持光学与 SAR 影像，这一点使其比纯 RGB agent 更接近 thesis 的多源设定。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

会址按预印本处理（正文虽提到期刊线索，未核正式页）；没有独立复现或灾害端到端评测。不能把“支持 SAR”写成“已解决 SAR 工具规划”。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`change-agent`](change-agent.md) — Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis
- [`rs-chatgpt`](rs-chatgpt.md) — Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models
- [`geoagent-chen`](geoagent-chen.md) — An LLM Agent for Automatic Geospatial Data Analysis

## 何时必须打开全文

需要工具包清单、任务类型体系、检索语料、光学/SAR 子集结果时。
