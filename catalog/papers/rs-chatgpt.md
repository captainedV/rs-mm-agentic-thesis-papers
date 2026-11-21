# Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models

> 论文卡片 · `rs-chatgpt` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **背景文献**

| 字段 | 值 |
| --- | --- |
| 标题 | Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models |
| 作者 | Guo, Su, Wu, Du, Zhang, Li（仓库短作者记录） |
| 年份 | 2024 |
| 会址 / 状态 | IGARSS 2024 |
| arXiv | [arXiv:2401.09083](https://arxiv.org/abs/2401.09083) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2401.09083) |
| Bib key | `rs-chatgpt`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-IGARSS-RS-ChatGPT-Guo.pdf`](../../pdfs/2024-IGARSS-RS-ChatGPT-Guo.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | detection / classification / captioning |
| PDF 版本 | arXiv 版本（非 IEEE IGARSS 正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

用 ChatGPT 串联预训练 RS 视觉模型（检测、分类、字幕等）完成解译任务的早期系统，目标是降低非专家使用 RS 工具的门槛。

## 核心结论

- RS-ChatGPT 的贡献是把 LLM 作为调度器，把多种现成视觉模型接成可执行解译流程。 [摘要]
- 它覆盖检测、分类、字幕等任务，展示了“LLM + 视觉工具”的早期可行性。 [摘要]
- 但工具链与规划较浅，缺少参数校验、轨迹评测与多传感器切换。 [摘要]
- 它是后续 RS agent 常引的起点，不是强 agent 方法。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1 的“可靠规划”结论；没有 benchmark 或轨迹监督。不能把早期 demo 写成已解决工具参数接地。

## 与主张的关系

**背景文献**。这篇提供背景、系统或评测基础设施，不能作为核心方法增益的直接证据。

## 相关论文

- [`rs-agent`](rs-agent.md) — RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent
- [`change-agent`](change-agent.md) — Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows

## 何时必须打开全文

需要具体工具清单、调度提示、失败案例分析时。
