# RSVQA: Visual Question Answering for Remote Sensing Data

> 论文卡片 · `rsvqa` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RSVQA: Visual Question Answering for Remote Sensing Data |
| 作者 | Sylvain Lobry; Diego Marcos; Jesse Murray; Devis Tuia |
| 年份 | 2020 |
| 会址 / 状态 | IEEE TGRS 2020 |
| arXiv | [arXiv:2003.07333](https://arxiv.org/abs/2003.07333) |
| DOI / 正式页 | [10.1109/TGRS.2020.2988782](https://doi.org/10.1109/TGRS.2020.2988782) · [正式/开放页](https://arxiv.org/abs/2003.07333) |
| Bib key | `rsvqa`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2020-TGRS-RSVQA-Lobry.pdf`](../../pdfs/2020-TGRS-RSVQA-Lobry.pdf) |
| 代码 / 项目 | https://rsvqa.sylvainlobry.com/ |
| 数据集 | RSVQA-LR, RSVQA-HR |
| PDF 版本 | 开放预印本（非 IEEE TGRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

RS VQA 的奠基性工作：用自然语言问题查询遥感影像，答案来自图像内容或 OSM 等外部地理数据；构建 RSVQA-LR/HR 基准。

## 核心结论

- RSVQA 把 RS 信息提取统一成“自然语言问、影像答”的接口，降低非专家使用门槛。 [摘要]
- 问题覆盖图像内容与关系依赖，答案可来自影像或外部地理数据。 [摘要]
- 它奠定了后续 RS VQA 的数据与评测范式，但协议是静态单轮。 [摘要]
- 时间上超出本包主窗口，仅作评测祖先与背景。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能与 agent 轨迹基准横排。不能把 VQA 准确率当作工具调用可靠性。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthvqa`](earthvqa.md) — EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering
- [`vrsbench`](vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding
- [`choice`](choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models
- [`lrs-vqa`](lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning

## 何时必须打开全文

需要 LR/HR 划分、答案来源、问题类型分布时。
