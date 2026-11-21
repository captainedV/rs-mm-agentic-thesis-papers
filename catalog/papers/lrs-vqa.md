# When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning

> 论文卡片 · `lrs-vqa` · 主题簇 [静态或单轮评测基准](../clusters/static-benchmarks.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning |
| 作者 | Junwei Luo; Yingying Zhang; Xue Yang; Kang Wu; Qi Zhu; Lei Liang; Jingdong Chen; Yansheng Li |
| 年份 | 2025 |
| 会址 / 状态 | ICCV 2025 |
| arXiv | [arXiv:2503.07588](https://arxiv.org/abs/2503.07588) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2503.07588) |
| Bib key | `lrs-vqa`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ICCV-LRS-VQA-Luo.pdf`](../../pdfs/2025-ICCV-LRS-VQA-Luo.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | LRS-VQA |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向超大遥感影像的 VQA 基准与方法：7,333 个 QA 对、8 类问题，图像最长边可达 27,328 像素；方法用文本引导的 token 剪枝 + 动态图像金字塔。

## 核心结论

- 论文指出固定网格会丢失 gigapixel RS 影像的细节，而无限制网格会带来不可接受的计算成本。 [摘要]
- LRS-VQA 含 7,333 个 QA 对、8 类问题，图像最长边 27,328 像素，专门压力测试大图感知。 [摘要]
- 方法用 Region Focus Module 做文本感知的区域定位，再用由粗到细的切片选择与 token 剪枝。 [摘要]
- 它在四个数据集上优于既有高分辨率策略，并与 token 缩减方法比较效率。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 7,333 | QA 对数 | 摘要 | 已核摘要 |
| 27,328 | 最大图像边长（像素） | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

这是大图 VQA/感知效率论文，不是工具规划；不能把 token 剪枝当成裁剪工具的规划策略。静态 QA 协议不能与轨迹 benchmark 横比。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`vrsbench`](vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding
- [`zoomearth`](zoomearth.md) — ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks
- [`geobench-vlm`](geobench-vlm.md) — GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks
- [`choice`](choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models

## 何时必须打开全文

需要 8 类问题的分布、切片/token 预算、四个数据集的逐项结果时。
