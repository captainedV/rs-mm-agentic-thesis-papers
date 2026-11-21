# RSGPT: A remote sensing vision language model and benchmark

> 论文卡片 · `rsgpt` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RSGPT: A remote sensing vision language model and benchmark |
| 作者 | Yuan Hu; Jianlong Yuan; Congcong Wen; Xiaonan Lu; Xiang Li |
| 年份 | 2025 |
| 会址 / 状态 | ISPRS Journal of Photogrammetry and Remote Sensing 2025 |
| arXiv | [arXiv:2307.15266](https://arxiv.org/abs/2307.15266) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2307.15266) |
| Bib key | `rsgpt`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ISPRS-RSGPT-Hu.pdf`](../../pdfs/2025-ISPRS-RSGPT-Hu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RSICap, RSIEval |
| PDF 版本 | arXiv 版本（非 ISPRS JPRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

RS 视觉–语言模型与 benchmark：用高质量 RS 图文数据做指令微调，配套 RSICap 字幕数据与 RSIEval 人工评测集。

## 核心结论

- RSGPT 指出 RS 领域缺少大规模、对齐良好的图文数据，直接阻碍 RS VLM 训练。 [摘要]
- 论文构建高质量 RS 图文与指令数据，并用小规模高质量微调获得可用的 RS 对话能力。 [摘要]
- 配套 RSICap/RSIEval 强调人工核验与可解释评测，而不是只追求数据量。 [papers.json 摘要要点；未核正文]
- 它是感知/字幕/VQA 路线，不是工具 agent。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑工具规划；不能把字幕质量当作 agent 的最终答案可靠性。RSIEval 的规模与任务范围有限。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model
- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model
- [`rs-llava`](rs-llava.md) — RS-LLaVA: A Large Vision-Language Model for Joint Captioning and Question Answering in Remote Sensing Imagery
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing

## 何时必须打开全文

需要 RSICap 的构造、RSIEval 的评分维度、微调数据规模时。
