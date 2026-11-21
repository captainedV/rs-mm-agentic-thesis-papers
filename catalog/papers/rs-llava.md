# RS-LLaVA: A Large Vision-Language Model for Joint Captioning and Question Answering in Remote Sensing Imagery

> 论文卡片 · `rs-llava` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RS-LLaVA: A Large Vision-Language Model for Joint Captioning and Question Answering in Remote Sensing Imagery |
| 作者 | Yakoub Bazi; Laila Bashmal; Mohamad Mahmoud Al Rahhal; Riccardo Ricci; Farid Melgani |
| 年份 | 2024 |
| 会址 / 状态 | Remote Sensing 16(9):1477 |
| arXiv | 无 |
| DOI / 正式页 | [10.3390/rs16091477](https://doi.org/10.3390/rs16091477) · [正式/开放页](https://www.mdpi.com/2072-4292/16/9/1477) |
| Bib key | `rs-llava`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2024-RemoteSensing-RS-LLaVA-Bazi.pdf`](../../pdfs/2024-RemoteSensing-RS-LLaVA-Bazi.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | captioning / VQA |
| PDF 版本 | MDPI 官方开放获取 PDF（CC BY 4.0） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 已收入 MDPI 官方开放获取 PDF（CC BY 4.0），不是付费墙镜像。 |

## 问题与方法

RS 版 LLaVA：用 LoRA 适配 RS 影像，联合图像字幕与 VQA 多任务；构建 RS-instructions 数据集整合四个单任务数据。

## 核心结论

- RS-LLaVA 用低秩适配把 LLaVA 迁移到 RS，强调字幕与 VQA 的联合多任务能力。 [摘要]
- RS-instructions 整合四个 RS 字幕/VQA 数据集，用于统一评测与训练。 [摘要]
- 论文报告 LoRA 适配在 RS 多任务上有效，是轻量适配路线的代表。 [摘要]
- 它是感知/生成模型，不是工具 agent。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把联合字幕/VQA 当作工具编排。RS-instructions 是静态任务集合。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark
- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model

## 何时必须打开全文

需要 LoRA 配置、RS-instructions 的四个数据源、联合训练比例与逐任务指标时。
