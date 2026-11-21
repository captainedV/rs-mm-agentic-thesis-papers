# EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain

> 论文卡片 · `earthgpt` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain |
| 作者 | Wei Zhang; Miaoxin Cai; Tong Zhang; Yin Zhuang; Xuerui Mao |
| 年份 | 2024 |
| 会址 / 状态 | IEEE TGRS 2024 |
| arXiv | [arXiv:2401.16822](https://arxiv.org/abs/2401.16822) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2401.16822) |
| Bib key | `earthgpt`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-TGRS-EarthGPT-Zhang.pdf`](../../pdfs/2024-TGRS-EarthGPT-Zhang.pdf) |
| 代码 / 项目 | https://github.com/wivizhang/EarthGPT |
| 数据集 | MMRS-1M |
| PDF 版本 | arXiv 版本（非 IEEE TGRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

统一光学/SAR/红外的 RS 多模态大模型：视觉增强感知 + 跨模态互相理解 + 多任务统一指令微调；构建 MMRS-1M（100 万+ 图文对，来自 34 个 RS 数据集）。

## 核心结论

- EarthGPT 的目标是用一个 MLLM 统一多传感器 RS 解译任务，而不是每个传感器/任务一个模型。 [摘要]
- MMRS-1M 含超过 100 万图文对，来自 34 个既有 RS 数据集，覆盖光学、SAR、红外。 [正文]
- 视觉增强感知融合粗粒度语义与细粒度细节，跨模态互相理解增强视觉–语言交互。 [摘要]
- 它是多传感器感知底座，常被后续 agent 当作视觉前端/对照，但本身不做工具规划。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| >1M | MMRS-1M 图文对数 | 正文 | 已核正文检索 |
| 34 | 来源 RS 数据集数 | 正文 | 已核正文检索 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把“支持 SAR”写成“具备 SAR–光学切换策略”。MMRS-1M 是指令数据，不是 agent 轨迹。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`fusar-gpt`](fusar-gpt.md) — FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery
- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning

## 何时必须打开全文

需要 MMRS-1M 的传感器/任务配比、视觉增强模块、统一指令格式与逐任务结果时。
