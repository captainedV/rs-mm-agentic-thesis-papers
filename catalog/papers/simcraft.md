# SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning

> 论文卡片 · `simcraft` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning |
| 作者 | Haoran Wang; Jing Yao; Xu Yang; Zeqing Wang; Yang Zhang; Pedram Ghamisi; Zhengchao Chen |
| 年份 | 2026 |
| 会址 / 状态 | EMNLP 2026 |
| arXiv | [arXiv:2608.30277](https://arxiv.org/abs/2608.30277) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://aclanthology.org/2026.emnlp-main.2674/) |
| Bib key | `simcraft`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-EMNLP-SimCRAFT-Wang.pdf`](../../pdfs/2026-EMNLP-SimCRAFT-Wang.pdf) |
| 代码 / 项目 | https://github.com/WangHrYii/SimCRAFT |
| 数据集 | synthetic RS agent trajectories |
| PDF 版本 | ACL Anthology 正式 PDF |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 正式会址为 EMNLP 2026 主会；本包使用 ACL Anthology 正式 PDF。 |

## 问题与方法

用多 agent 合成引擎 + Mock Execution Engine（检查 schema、工具间依赖、传感器/工具兼容性）生成 SimRS-14k 轨迹语料，再用 Contextual Retrieval-Augmented Fine-Tuning（CRAFT）把多步 RS 工作流规划蒸馏到 7B 模型。

## 核心结论

- SimCRAFT 的出发点是：强 RS agent 依赖大模型，部署成本高且缺领域知识，需要把“编排能力”蒸馏到小模型。 [摘要]
- 数据侧用多 agent 合成 + Mock Execution Engine 校验 schema、工具依赖与传感器/工具兼容性，产出 SimRS-14k。 [摘要]
- CRAFT 让模型在噪声检索下“类比改编”标准作业流程（SOP），而不是机械复制检索到的轨迹。 [摘要]
- 论文称 7B 模型显著优于开源 LLM，并可与闭源模型/专用 RS agent 竞争，且在三个 7B 骨干上复现。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 7B | 蒸馏目标模型规模 | 摘要 | 已核摘要 |
| SimRS-14k | 合成工作流语料规模 | 摘要 | 已核摘要 |
| 3 | 复现的 7B 骨干数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

合成轨迹的约束校验不等于真实执行正确；不能把 7B 的竞争性结果外推到灾害/SAR 长程任务。没有报告“步骤对、答案错”的联合指标，不能直接声称解决 P2 的核心错误模式。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`vicot-agent`](vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis
- [`rs-claw-evolution`](rs-claw-evolution.md) — RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks
- [`weaveagent`](weaveagent.md) — WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 SimRS-14k 的生成流程、Mock Engine 的校验规则、CRAFT 的噪声目标、三个骨干的逐项结果时。
