# HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving

> 论文卡片 · `hirs-agent` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving |
| 作者 | Boyang Mu; Zhiwei Wei; Mugen Peng; Wenjia Xu |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2608.30672）；会址待确认。arXiv 注释写 ACM MM 2026，未与正式论文集交叉核对，不升格 |
| arXiv | [arXiv:2608.30672](https://arxiv.org/abs/2608.30672) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2608.30672) |
| Bib key | `hirs-agent`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-arXiv-HiRS-Agent-Mu.pdf`](../../pdfs/2026-arXiv-HiRS-Agent-Mu.pdf) |
| 代码 / 项目 | https://github.com/IntelliSensing/HiRS-Agent |
| 数据集 | 无记录 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | arXiv 注释写 ACM MM 2026，但未与正式论文集交叉核对；按预印本处理，不升格。 |

## 问题与方法

两级多 agent：Manager 负责动态路由、步级验证、重规划与终止，Specialist 按 RS 工作流组织领域工具并执行子任务；训练为两阶段监督微调 + 验证引导的分层 RL。

## 核心结论

- 论文把单体决策的长程失败归因于任务多阶段、工具误用与错误跨阶段传播。 [摘要]
- Manager/Specialist 分层把“下一步做什么”和“具体怎么调工具”拆开，并在步级做验证与重规划。 [摘要]
- 两阶段监督调优 + 验证引导的分层强化学习同时优化协作策略与工具使用策略。 [摘要]
- 在 Earth-Agent Benchmark 与 ThinkGeo 上报告长程工具使用和最终任务正确率提升。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

arXiv 注释提到 ACM MM 2026，但仓库未与正式论文集交叉核对，卡片按预印本处理，不得写成 ACM MM 录用。结果只在两个现有基准上，不能外推为灾害场景通用提升。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks
- [`rs-claw`](rs-claw.md) — RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents
- [`vicot-agent`](vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis

## 何时必须打开全文

需要 Manager 的验证信号、重规划触发条件、分层 RL 的奖励与信用分配、两个基准的逐项结果时。
