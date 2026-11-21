# TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data

> 论文卡片 · `teochat` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data |
| 作者 | Jeremy Andrew Irvin; Emily Ruoyu Liu; Joyce Chuyi Chen; Ines Dormoy; Jinyoung Kim; Samar Khanna; Zhuo Zheng; Stefano Ermon |
| 年份 | 2025 |
| 会址 / 状态 | ICLR 2025 |
| arXiv | [arXiv:2410.06234](https://arxiv.org/abs/2410.06234) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://proceedings.iclr.cc/paper_files/paper/2025/file/ac3af725ae398b6184faae0828bdbd6c-Paper-Conference.pdf) |
| Bib key | `teochat`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ICLR-TEOChat-Irvin.pdf`](../../pdfs/2025-ICLR-TEOChat-Irvin.pdf) |
| 代码 / 项目 | https://github.com/ermongroup/teochat |
| 数据集 | temporal EO / change |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向时间序列 EO 数据的视觉–语言助手，能围绕多时相影像对话，覆盖建筑变化、损毁评估、语义变化检测与时序场景分类。

## 核心结论

- TEOChat 解决的是“只能看单张图”的限制，把多时相序列作为输入做对话与推理。 [摘要]
- 训练数据同时包含单图任务与时序任务，覆盖建筑变化、损毁评估、语义变化检测等。 [摘要]
- 论文称其在多种空间/时序任务上显著优于先前 VLM，并在部分任务上接近或超过专用模型。 [摘要]
- 它仍是模型内推理，不调用外部检测/分割/变化检测工具，因此不能替代工具规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把“时序对话”写成“时序工具编排”。没有灾害端到端流水线或 SAR 切换实验。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`disasterm3`](disasterm3.md) — DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning
- [`change-agent`](change-agent.md) — Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis

## 何时必须打开全文

需要时序任务的输入格式、训练数据规模、与专用模型的逐任务对比时。
