# VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis

> 论文卡片 · `vicot-agent` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis |
| 作者 | Chujie Wang; Zhiyuan Luo; Ruiqi Liu; Can Ran; Shenghua Fan; Xi Chen; Chu He |
| 年份 | 2025 |
| 会址 / 状态 | 预印本（arXiv:2511.20085）；会址待确认 |
| arXiv | [arXiv:2511.20085](https://arxiv.org/abs/2511.20085) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2511.20085) |
| Bib key | `vicot-agent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-arXiv-VICoT-Agent-Wang.pdf`](../../pdfs/2025-arXiv-VICoT-Agent-Wang.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RSVQA, MME-RealWorld-RS, LRS-VQA, VICoT-HRSC |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

VICoT 把视觉工具动态插入思维链，用栈式推理结构组织多轮“看—想—再取数”，并提供 MCP 兼容工具套件；再用 Reasoning Stack distillation 把复杂 agent 行为迁移到小模型。

## 核心结论

- VICoT 的关键不是一次性生成答案，而是把视觉工具调用嵌进 CoT，形成可解释的多轮视觉–语言交替推理。 [摘要]
- 栈式结构让 agent 能回退、重入和组合工具，适合需要多尺度观察的 RS 任务。 [摘要]
- Reasoning Stack distillation 把复杂 agent 行为蒸馏到轻量模型，直接对应“轨迹/推理过程可迁移”这一 P2 关切。 [摘要]
- 论文在多个 RS 基准上报告推理透明度、执行效率和生成质量的提升；具体数值需回正文表格核对。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

预印本，会址待确认；摘要没有给出可安全引用的统一分数，不能写“全面 SOTA”。蒸馏到小模型不等于降低“步骤对、答案错”的错误率，后者需要单独指标。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`rs-claw-evolution`](rs-claw-evolution.md) — RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks
- [`hirs-agent`](hirs-agent.md) — HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要栈式推理的形式化、工具调用记录格式、蒸馏损失、各基准的逐步结果时。
