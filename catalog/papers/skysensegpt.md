# SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding

> 论文卡片 · `skysensegpt` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding |
| 作者 | Junwei Luo; Zhen Pang; Yongjun Zhang; Tingzhu Wang; Linlin Wang; Bo Dang; Jiangwei Lao; et al. |
| 年份 | 2024 |
| 会址 / 状态 | 预印本（arXiv:2406.10100）；至交接清单完成时仍以预印本为主 |
| arXiv | [arXiv:2406.10100](https://arxiv.org/abs/2406.10100) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2406.10100) |
| Bib key | `skysensegpt`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2024-arXiv-SkySenseGPT-Luo.pdf`](../../pdfs/2024-arXiv-SkySenseGPT-Luo.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | FIT-RS |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

细粒度 RS 指令微调数据与模型：FIT-RS 含 1,800,851 条指令样本，覆盖常见解译任务并引入关系推理、图像级场景图生成等复杂任务；配套 FIT-RSFG 等基准。

## 核心结论

- SkySenseGPT 针对 RS LMM 对复杂场景中对象语义关系理解不足的问题，构建细粒度关系指令数据。 [摘要]
- FIT-RS 含 1,800,851 条指令样本，任务从常见解译逐步升级到关系推理与场景图生成。 [摘要]
- 配套 FIT-RSFG 等基准用于评估细粒度关系理解。 [摘要]
- 它是感知/指令跟随模型，不是 agent；会址仍按预印本处理。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 1,800,851 | FIT-RS 指令样本数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把关系推理能力当作工具规划能力。会址不得写成已录用顶会。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`skyeyegpt`](skyeyegpt.md) — SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model
- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing

## 何时必须打开全文

需要 FIT-RS 的任务层级、场景图标注、FIT-RSFG 评测协议时。
