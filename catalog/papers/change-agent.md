# Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis

> 论文卡片 · `change-agent` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis |
| 作者 | Chenyang Liu; Keyan Chen; Haotian Zhang; Zipeng Qi; Zhengxia Zou; Zhenwei Shi |
| 年份 | 2024 |
| 会址 / 状态 | IEEE TGRS 2024 |
| arXiv | [arXiv:2403.19646](https://arxiv.org/abs/2403.19646) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2403.19646) |
| Bib key | `change-agent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-TGRS-Change-Agent-Liu.pdf`](../../pdfs/2024-TGRS-Change-Agent-Liu.pdf) |
| 代码 / 项目 | https://github.com/Chen-Yang-Liu/Change-Agent |
| 数据集 | LEVIR-MCI |
| PDF 版本 | arXiv 版本（非 IEEE TGRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

把多级变化解译（MCI）模型当“眼睛”、LLM 当“大脑”：用户指令触发变化检测、变化字幕、目标计数、原因分析与变化预测等 Python 工具调用；配套 LEVIR-MCI 双时相数据。

## 核心结论

- Change-Agent 针对 RS 变化解译中“检测”和“字幕”各自为战的问题，把两者统一进交互式分析。 [摘要]
- MCI 模型含像素级变化检测与语义级变化字幕两支，并用 BI3 层增强双时相交互特征。 [摘要]
- LLM 作为控制器按用户意图调用计数、原因分析、变化预测等 Python 工具，形成早期可执行变化分析流水线。 [摘要]
- 它验证了“感知模型 + LLM 规划 + 工具调用”在变化分析上的可行性，但工具范围限于双时相光学变化。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 SAR–光学切换、灾害多工具流水线或轨迹级后训练；不能把变化分析的工具调用外推为通用 EO 规划。没有与其他 agent 基准的同协议对比。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`rs-agent`](rs-agent.md) — RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent
- [`teochat`](teochat.md) — TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data
- [`rescueadi`](rescueadi.md) — RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents

## 何时必须打开全文

需要 MCI 的两支结构、BI3 层、Python 工具清单、LEVIR-MCI 的规模与评测指标时。
