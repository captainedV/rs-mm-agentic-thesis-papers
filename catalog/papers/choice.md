# CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models

> 论文卡片 · `choice` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models |
| 作者 | Xiao An; Jiaxing Sun; Zihan Gui; Wei He |
| 年份 | 2025 |
| 会址 / 状态 | NeurIPS 2025 Datasets and Benchmarks |
| arXiv | [arXiv:2411.18145](https://arxiv.org/abs/2411.18145) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://proceedings.neurips.cc/paper_files/paper/2025/file/befe25a01cf4dbe9635e85f835d31250-Paper-Datasets_and_Benchmarks_Track.pdf) |
| Bib key | `choice`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-NeurIPS-CHOICE-An.pdf`](../../pdfs/2025-NeurIPS-CHOICE-An.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | CHOICE |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向遥感 LVLM 的分层能力基准：2 个一级维度（感知、推理）、6 个二级维度、23 个叶子任务，共 10,507 道选择题，数据来自 50 个全球城市。

## 核心结论

- CHOICE 用选择题形式把遥感能力拆成感知与推理两层，避免开放式生成难以客观评分。 [摘要]
- 10,507 道题经过统一采集、构造与质量控制，来源覆盖 50 个全球城市。 [摘要]
- 对 3 个闭源与 21 个开源 VLM 的评测显示，模型在遥感专用语境下仍有明显短板。 [摘要]
- 它是静态单轮基准，适合评估感知/推理底座，不适合评估工具序列或轨迹。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 10,507 | 题目数 | 摘要 | 已核摘要 |
| 50 | 数据来源城市数 | 摘要 | 已核摘要 |
| 3 + 21 | 闭源 / 开源评测模型数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能用来证明 agent 的工具规划能力；选择题协议与轨迹级 benchmark（ThinkGeo/DORA/Earth-Bench）不可横比。没有官方唯一仓库被仓库记录确认。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`geobench-vlm`](geobench-vlm.md) — GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks
- [`vrsbench`](vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding
- [`lrs-vqa`](lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning
- [`earthvqa`](earthvqa.md) — EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering

## 何时必须打开全文

需要 23 个叶子任务的定义、题目分布、各模型分维度结果时。
