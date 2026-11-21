# GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective

> 论文卡片 · `geocot` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective |
| 作者 | Daixun Li; Zirui Li; Sibo He; Jiayun Tian; Mingxiang Cao; Weiying Xie; Yunke Wang; Xin Zhang; Yusi Zhang; Yunsong Li; Chang Xu; Leyuan Fang |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · 仓库未记录 |
| Bib key | `geocot`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-CVPR-GeoCoT-Li.pdf`](../../pdfs/2026-CVPR-GeoCoT-Li.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RS-CoT-20k |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

GeoCoT 用流形驱动的 MoE（Mani-MoE）做 RS 多任务推理：把高维 token 投影到低秩子空间、按流形结构路由专家，并用冷启动 + RSV-GRPO 的两阶段训练强化 CoT；配套 RS-CoT-20k。

## 核心结论

- GeoCoT 认为单一共享专家难以同时满足 RS 多任务的精度与可靠性，且 RS 图像存在冗余与同质性。 [摘要]
- Mani-MoE 用局部流形映射把 token 投到低秩子空间，再用稀疏专家路径处理不同任务。 [摘要]
- 训练为冷启动领域适应 + RS Vision GRPO，从全局到目标强化结构化推理。 [摘要]
- 论文报告相对此前 SOTA 平均准确率提升 5.27%；这是模型内 CoT 的增益，不是工具轨迹的增益。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 5.27% | 平均准确率相对提升 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1：没有外部工具调用。不能把 5.27% 写成“后训练降低了步骤–答案不一致”，因为它主要报告任务准确率。RS-CoT-20k 是推理数据，不是 agent 轨迹。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`socrates`](socrates.md) — Asking like Socrates: Socrates helps VLMs understand remote sensing images
- [`remotereasoner`](remotereasoner.md) — RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow
- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`skymoe`](skymoe.md) — SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts

## 何时必须打开全文

需要 RSV-GRPO 的奖励、Mani-MoE 路由细节、RS-CoT-20k 的构造、逐任务结果时。
