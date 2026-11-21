# Asking like Socrates: Socrates helps VLMs understand remote sensing images

> 论文卡片 · `socrates` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | Asking like Socrates: Socrates helps VLMs understand remote sensing images |
| 作者 | Run Shao; Ziyu Li; Zhaoyang Zhang; Linrui Xu; Xinran He; Hongyuan Yuan; Bolei He; Yongxing Dai; Yiming Yan; Yijun Chen; Wang Guo; Haifeng Li |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | [arXiv:2511.22396](https://arxiv.org/abs/2511.22396) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/CVPR2026/papers/Shao_Asking_like_Socrates_Socrates_helps_VLMs_understand_remote_sensing_images_CVPR_2026_paper.pdf) |
| Bib key | `socrates`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-CVPR-AskingLikeSocrates-Shao.pdf`](../../pdfs/2026-CVPR-AskingLikeSocrates-Shao.pdf) |
| 代码 / 项目 | https://geoxlab.github.io/Asking_like_Socrates |
| 数据集 | RS VQA / grounding |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

提出 RS-EoT（Evidence-of-Thought）证据寻求范式：用 SocraticAgent 自博弈多 agent 合成“推理—视觉检查”交替轨迹，再用两阶段渐进式 RL 把证据寻求行为固化到模型。

## 核心结论

- 论文观察到 RS 任务普遍存在“伪推理/Glance Effect”：模型在叙述推理，而不是依据视觉证据得出答案。 [摘要]
- RS-EoT 要求模型在推理中反复回到图像取证，用自博弈多 agent 合成这类轨迹。 [摘要]
- 两阶段渐进式 RL 先在小数据上学格式，再扩展到更难任务，以提升证据寻求的泛化。 [摘要]
- 它针对的是模型内推理可靠性，不是外部工具规划；可作为 P2 中“过程监督/RL”的方法参照。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1；没有外部工具调用、参数校验或 SAR–光学切换。不能把“减少伪推理”直接等同于“降低最终答案错误率”，后者需要联合指标。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`geocot`](geocot.md) — GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective
- [`vicot-agent`](vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis
- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`remotereasoner`](remotereasoner.md) — RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow

## 何时必须打开全文

需要 RS-EoT 轨迹格式、SocraticAgent 的角色与停止条件、两阶段 RL 的奖励时。
