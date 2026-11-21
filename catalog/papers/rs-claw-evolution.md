# RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks

> 论文卡片 · `rs-claw-evolution` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks |
| 作者 | Kai Ouyang; Dongyang Hou; Liangtian Liu; Zeyuan Wang; Ziyu Li; Chengfu Liu; Zichao Tang; Xuezhi Cui; Shengwu Ouyang; Wentao Yang; Hanwen Yu; Haifeng Li |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2609.22258）；会址待确认 |
| arXiv | [arXiv:2609.22258](https://arxiv.org/abs/2609.22258) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2609.22258) |
| Bib key | `rs-claw-evolution`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-arXiv-RS-Claw-Evolution-Ouyang.pdf`](../../pdfs/2026-arXiv-RS-Claw-Evolution-Ouyang.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | 无记录 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向轻量 RS agent 的长程任务，把环境反馈转成学习信号：代码化交互维持中间状态，失败感知轨迹生成 + 错误轮掩码做 SFT，再用多维环境奖励与轮级优势保护做 RL。

## 核心结论

- 论文把轻量 agent 的长程失败归因于状态丢失、环境反馈利用低和优化信号稀疏。 [摘要]
- 交互演化阶段用可执行代码显式控制观测与中间状态，降低长上下文冗余。 [摘要]
- 经验演化阶段用失败感知轨迹生成，配合错误轮掩码：保留恢复行为，但不模仿错误动作。 [摘要]
- 决策演化阶段用多维环境奖励和 turn-level advantage protection 做 RL，缓解长序列信用分配。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

预印本；没有给出可安全引用的统一提升数字。不能把“错误轮掩码”直接等同于解决了最终答案错误，仍需单独报告步骤正确/答案正确的联合分布。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`vicot-agent`](vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis
- [`weaveagent`](weaveagent.md) — WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery
- [`hirs-agent`](hirs-agent.md) — HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving

## 何时必须打开全文

需要失败轨迹的构造方式、错误轮掩码的粒度、环境奖励组成、RL 的信用分配实现时。
