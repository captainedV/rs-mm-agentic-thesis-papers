# LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing Vision-Language Interpretation

> 论文卡片 · `lhrs-bot-nova` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing Vision-Language Interpretation |
| 作者 | Zhenshi Li; Dilxat Muhtar; Feng Gu; Xueliang Zhang; Pengfeng Xiao; Guangjun He; Xiaoxiang Zhu |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2411.09301）；会址待确认 |
| arXiv | [arXiv:2411.09301](https://arxiv.org/abs/2411.09301) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2411.09301) |
| Bib key | `lhrs-bot-nova`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2024-arXiv-LHRS-Bot-Nova-Li.pdf`](../../pdfs/2024-arXiv-LHRS-Bot-Nova-Li.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RS instruction following |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

LHRS-Bot 的改进版 RS MLLM：增强视觉编码器与 bridge 层，提升 RS 图像理解与指令跟随能力。

## 核心结论

- LHRS-Bot-Nova 是针对 RS 图像理解优化的 MLLM，重点在视觉编码器与跨模态桥接层。 [摘要]
- 它延续 LHRS-Bot 的 RS 指令跟随路线，面向多种 RS 理解任务。 [摘要]
- 模型本身不包含外部工具注册或长程规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

会址按预印本处理；不能支撑 P1/P2；不能把编码器改进写成 agent 能力提升。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark
- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model
- [`falcon`](falcon.md) — Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report)

## 何时必须打开全文

需要增强编码器结构、bridge 层设计、训练数据与各任务指标时。
