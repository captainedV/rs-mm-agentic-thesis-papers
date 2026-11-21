# WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery

> 论文卡片 · `weaveagent` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery |
| 作者 | Zhongyu Pang（PDF 元数据仅列该名） |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2609.31234）；会址待确认 |
| arXiv | [arXiv:2609.31234](https://arxiv.org/abs/2609.31234) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2609.31234) |
| Bib key | `weaveagent`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-arXiv-WeaveAgent-Pang.pdf`](../../pdfs/2026-arXiv-WeaveAgent-Pang.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | 无记录 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向超高分辨率遥感与模糊意图的两阶段工具路由 agent：Stage A 先训练“是否/调用哪个工具”的路由发射，Stage B 再条件执行；训练为 alignment SFT 后接 GRPO。

## 核心结论

- 论文指出预训练模型零样本几乎不发射工具调用，因此把路由做成“训练出来的能力”，而不是靠提示诱导。 [摘要]
- Stage A 的路由优先设计把 extrinsic 查询的路由率从 0% 提到 80.75%（323/400）。 [摘要]
- Stage B 对 intrinsic 查询走固定预算约 5k token 的压缩视觉问答，对 extrinsic 查询在原分辨率上执行工具调用。 [摘要]
- 把工具观测载入上下文使 extrinsic 答案准确率从 0.025 提到 0.425；两轮 SFT 再增加 9.3 点到 0.518（训练分布返回下 0.965）。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 0% → 80.75% | alignment SFT 后 extrinsic 路由率 | 摘要 | 已核摘要 |
| 0.025 → 0.425 | 载入工具观测后的 extrinsic 答案准确率 | 摘要 | 已核摘要 |
| +9.3 点 → 0.518 | 两轮 SFT 的增益与准确率 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

预印本；任务集中在 VagueUHR 单影像工具路由，不是多传感器灾害流水线。0.965 是训练分布返回下的 oracle/annotation-grounded 结果，不能当作真实部署精度。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`rs-claw-evolution`](rs-claw-evolution.md) — RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks
- [`vicot-agent`](vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis
- [`geommagent`](geommagent.md) — GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing

## 何时必须打开全文

需要 VagueUHR 的构造、路由标签、GRPO 奖励 RWA2、两轮观察掩码协议、oracle 归因实验时。
