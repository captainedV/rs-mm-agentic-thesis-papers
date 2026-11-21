# LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model

> 论文卡片 · `lhrs-bot` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model |
| 作者 | Dilxat Muhtar; Zhenshi Li; Feng Gu; Xueliang Zhang; Pengfeng Xiao |
| 年份 | 2024 |
| 会址 / 状态 | ECCV 2024 |
| arXiv | [arXiv:2402.02544](https://arxiv.org/abs/2402.02544) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2402.02544) |
| Bib key | `lhrs-bot`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-ECCV-LHRS-Bot-Muhtar.pdf`](../../pdfs/2024-ECCV-LHRS-Bot-Muhtar.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | LHRS-Instruct, LHRS-Bench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

用 VGI（如 OSM）增强的 RS MLLM：构建 LHRS-Align 图文数据、LHRS-Instruct 指令数据与 LHRS-Bench，采用多级视觉–语言对齐与课程学习。

## 核心结论

- LHRS-Bot 指出 RS 影像的地物多样性与地理上下文没有被既有 MLLM 充分考虑。 [摘要]
- 它用 VGI 与全球 RS 影像构造大规模对齐/指令数据，并设计多级对齐与课程学习。 [摘要]
- 配套 LHRS-Bench 用于系统评估 RS 理解能力。 [摘要]
- 它是感知/指令跟随模型，不含工具规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把 VGI 增强当作地理空间工具调用。LHRS-Bench 是静态评测。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`lhrs-bot-nova`](lhrs-bot-nova.md) — LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing Vision-Language Interpretation
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model

## 何时必须打开全文

需要 LHRS-Align/LHRS-Instruct 的构造、课程学习阶段、LHRS-Bench 维度时。
