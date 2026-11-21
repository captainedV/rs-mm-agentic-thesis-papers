# SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model

> 论文卡片 · `skyeyegpt` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model |
| 作者 | Yang Zhan; Zhitong Xiong; Yuan Yuan |
| 年份 | 2025 |
| 会址 / 状态 | ISPRS Journal of Photogrammetry and Remote Sensing 2025 |
| arXiv | [arXiv:2401.09712](https://arxiv.org/abs/2401.09712) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2401.09712) |
| Bib key | `skyeyegpt`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ISPRS-SkyEyeGPT-Zhan.pdf`](../../pdfs/2025-ISPRS-SkyEyeGPT-Zhan.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | SkyEye-968k |
| PDF 版本 | arXiv 版本（非 ISPRS JPRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

统一的 RS 多模态大模型：把 RS 视觉特征经对齐层投影到语言域，用 968k 指令样本覆盖字幕、VQA、场景分类、视觉定位、目标检测与多任务对话。

## 核心结论

- SkyEyeGPT 的目标是用一个简单对齐层统一多种 RS 视觉–语言任务，而不为每个任务加额外编码器。 [摘要]
- 构建并人工核验了 968k 样本的 RS 指令跟随数据集。 [摘要]
- 论文报告该设计在差异很大的任务上都能工作，说明统一指令微调是可行的感知路线。 [摘要]
- 它是单模型多任务 VLM，没有外部工具调用或轨迹规划。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 968k | 指令样本数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把多任务统一等同于 agent 的工具编排。数据集是指令数据，不是轨迹数据。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark
- [`skysensegpt`](skysensegpt.md) — SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding
- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model

## 何时必须打开全文

需要 968k 数据的任务配比、对齐层结构、各任务指标时。
