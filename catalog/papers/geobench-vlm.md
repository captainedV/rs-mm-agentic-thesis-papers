# GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks

> 论文卡片 · `geobench-vlm` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks |
| 作者 | Muhammad Danish; Muhammad Akhtar Munir; Syed Roshaan Ali Shah; Kartik Kuckreja; Fahad Shahbaz Khan; Paolo Fraccaro; Alexandre Lacoste; Salman Khan |
| 年份 | 2025 |
| 会址 / 状态 | ICCV 2025 |
| arXiv | [arXiv:2411.19325](https://arxiv.org/abs/2411.19325) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/ICCV2025/papers/Danish_GEOBench-VLM_Benchmarking_Vision-Language_Models_for_Geospatial_Tasks_ICCV_2025_paper.pdf) |
| Bib key | `geobench-vlm`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ICCV-GEOBench-VLM-Danish.pdf`](../../pdfs/2025-ICCV-GEOBench-VLM-Danish.pdf) |
| 代码 / 项目 | https://the-ai-alliance.github.io/GEO-Bench-VLM/ |
| 数据集 | GEOBench-VLM |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 项目页称最强模型选择题约 40% 量级；该数字未在本卡正文表格核对，引用前回正表。 |

## 问题与方法

面向地学任务的 VLM 基准，覆盖场景理解、目标计数、定位、细粒度分类、分割与时序分析，含 10,000+ 人工核验指令。

## 核心结论

- GEOBench-VLM 指出通用 VLM 基准没有覆盖地学特有的时序变化、大范围计数、小目标检测与实体关系。 [摘要]
- 基准含 10,000+ 人工核验指令，覆盖多种视觉条件、目标类型与尺度。 [摘要]
- 对多个 SOTA VLM 的评测显示，地学专用任务仍有明显差距，不能把通用多模态能力直接迁移。 [摘要]
- 它仍是固定输入/单轮协议，不是工具调用或轨迹评测。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 10,000+ | 人工核验指令数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；项目页称最强模型选择题约 40% 量级，但该数字来自项目页而非本卡核对的正文表格，引用前需回正文。不能与 CHOICE 的分数直接横排。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`choice`](choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models
- [`vrsbench`](vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding
- [`lrs-vqa`](lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning
- [`earthvqa`](earthvqa.md) — EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering

## 何时必须打开全文

需要 8 类任务的划分、指令构造、分割/时序子任务协议、逐模型结果时。
