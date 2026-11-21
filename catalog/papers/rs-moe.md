# RS-MoE: Mixture of Experts for Remote Sensing Image Captioning and Visual Question Answering

> 论文卡片 · `rs-moe` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RS-MoE: Mixture of Experts for Remote Sensing Image Captioning and Visual Question Answering |
| 作者 | Hui Lin; Danfeng Hong; Shuhang Ge; Chuyao Luo; Kai Jiang; Hao Jin; Congcong Wen |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2411.01595）；会址待确认 |
| arXiv | [arXiv:2411.01595](https://arxiv.org/abs/2411.01595) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2411.01595) |
| Bib key | `rs-moe`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2024-arXiv-RS-MoE-Lin.pdf`](../../pdfs/2024-arXiv-RS-MoE-Lin.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | captioning / VQA |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向 RS 字幕与 VQA 的 MoE 视觉–语言模型：用 MoE Block 与指令路由让不同专家处理不同任务/粒度。

## 核心结论

- RS-MoE 指出多数 RS VLM 只是对通用模型做微调，没有针对 RS 影像特点设计结构。 [摘要]
- 它用 MoE Block 与指令路由，把字幕与 VQA 的不同需求分给专家。 [摘要]
- 这是感知/生成侧的专家化，不是工具选择或轨迹规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把 MoE 路由当成工具路由。没有灾害/多传感器 agent 实验。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`skymoe`](skymoe.md) — SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts
- [`geocot`](geocot.md) — GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective
- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark

## 何时必须打开全文

需要专家数量、路由损失、字幕/VQA 数据与逐项结果时。
