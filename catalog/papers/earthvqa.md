# EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering

> 论文卡片 · `earthvqa` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering |
| 作者 | Junjue Wang; Zhuo Zheng; Zihang Chen; Ailong Ma; Yanfei Zhong |
| 年份 | 2024 |
| 会址 / 状态 | AAAI 2024 |
| arXiv | [arXiv:2312.12222](https://arxiv.org/abs/2312.12222) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2312.12222) |
| Bib key | `earthvqa`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-AAAI-EarthVQA-Wang.pdf`](../../pdfs/2024-AAAI-EarthVQA-Wang.pdf) |
| 代码 / 项目 | https://github.com/Junjue-Wang/EarthVQA |
| 数据集 | EarthVQA |
| PDF 版本 | arXiv 版本（非 AAAI 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

关系推理型 RS VQA 数据集与方法：6,000 张图、对应语义掩膜、208,593 个 QA 对，任务含判断、计数与综合分析；方法 SOBA 用分割网络生成对象语义再做对象引导注意力。

## 核心结论

- EarthVQA 针对 RS 研究偏重目标位置/类别、忽视对象关系与综合推理的问题。 [摘要]
- 数据含 6,000 图、208,593 QA，问题嵌入城乡治理需求。 [摘要]
- SOBA 用分割网络生成对象语义，再用对象引导注意力做关系推理。 [摘要]
- 它是静态 VQA 对照基准，不是 agent 工具规划评测。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 6,000 | 图像数 | 摘要 | 已核摘要 |
| 208,593 | QA 对数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能与 VRSBench/CHOICE 的分数横排（协议不同）。不能把关系推理能力当作工具编排能力。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`rsvqa`](rsvqa.md) — RSVQA: Visual Question Answering for Remote Sensing Data
- [`vrsbench`](vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding
- [`choice`](choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models
- [`geobench-vlm`](geobench-vlm.md) — GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks

## 何时必须打开全文

需要 208,593 QA 的任务分布、SOBA 结构、评价指标时。
