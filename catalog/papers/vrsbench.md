# VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding

> 论文卡片 · `vrsbench` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding |
| 作者 | Xiang Li; Jian Ding; Mohamed Elhoseiny |
| 年份 | 2024 |
| 会址 / 状态 | NeurIPS 2024 Datasets and Benchmarks |
| arXiv | [arXiv:2406.12384](https://arxiv.org/abs/2406.12384) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://proceedings.neurips.cc/paper_files/paper/2024/file/05b7f821234f66b78f99e7803fffa78a-Paper-Datasets_and_Benchmarks_Track.pdf) |
| Bib key | `vrsbench`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-NeurIPS-VRSBench-Li.pdf`](../../pdfs/2024-NeurIPS-VRSBench-Li.pdf) |
| 代码 / 项目 | https://github.com/lx709/VRSBench · https://vrsbench.github.io/ |
| 数据集 | VRSBench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

通用遥感视觉–语言基准：29,614 张图、29,614 条人工核验详细字幕、52,472 个目标指称、123,221 个 QA 对，覆盖字幕、视觉定位与开放 VQA。

## 核心结论

- VRSBench 针对既有 RS 数据集单任务、缺目标细节、质控不足的问题，构建统一的多任务 VL 基准。 [摘要]
- 规模为 29,614 图、52,472 指称、123,221 QA，且字幕经过人工核验。 [摘要]
- 论文在字幕、视觉定位、VQA 三类任务上评估 SOTA 模型，说明通用模型仍有明显不足。 [摘要]
- 它是静态 VL 基准，适合做感知/定位对照，不是 agent 轨迹评测。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 29,614 | 图像数 / 详细字幕数 | 摘要 | 已核摘要 |
| 52,472 | 目标指称数 | 摘要 | 已核摘要 |
| 123,221 | QA 对数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑工具规划或灾害响应；不能把 VRSBench 的定位分数当作 agent 的裁剪/对齐能力证据。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`choice`](choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models
- [`geobench-vlm`](geobench-vlm.md) — GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks
- [`earthvqa`](earthvqa.md) — EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering
- [`lrs-vqa`](lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning

## 何时必须打开全文

需要数据构造、指称类型、QA 分布、各任务的评价指标时。
