# Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report)

> 论文卡片 · `falcon` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report) |
| 作者 | Kelu Yao; Nuo Xu; Rong Yang; Yingying Xu; Zhuoyan Gao; Titinunt Kitrungrotsakul; Yi Ren; Pu Zhang; Jin Wang; Ning Wei; Chao Li |
| 年份 | 2025 |
| 会址 / 状态 | 技术报告（arXiv:2503.11070）；会址待确认 |
| arXiv | [arXiv:2503.11070](https://arxiv.org/abs/2503.11070) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2503.11070) |
| Bib key | `falcon`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2025-arXiv-Falcon-Yao.pdf`](../../pdfs/2025-arXiv-Falcon-Yao.pdf) |
| 代码 / 项目 | https://github.com/TianHuiLab/Falcon |
| 数据集 | Falcon_SFT |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

统一的 RS 视觉–语言基础模型：用 prompt 驱动图像/区域/像素级任务，覆盖 14 类任务；配套 Falcon SFT 约 7800 万高质量样本。

## 核心结论

- Falcon 的目标是一个统一、prompt 驱动的 RS VLM，而不是每个任务一个专用模型。 [摘要]
- 它覆盖 14 个任务，包括分类、检测、分割、字幕等，并支持图像、区域、像素三个层级。 [摘要]
- Falcon SFT 约 7800 万样本，是其主要数据贡献。 [摘要]
- 作为技术报告/预印本，它是感知底座候选，不是工具 agent。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 14 | 任务数 | 摘要 | 已核摘要 |
| 78M | Falcon SFT 样本量（约） | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

会址按技术报告/预印本处理；不能写成已录用顶会。不能支撑工具规划；不能把 14 任务统一当作 agent 的多工具编排。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`skymoe`](skymoe.md) — SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts
- [`rsgpt`](rsgpt.md) — RSGPT: A remote sensing vision language model and benchmark

## 何时必须打开全文

需要 Falcon SFT 的构成、14 任务的逐项结果、与 GeoChat/EarthGPT 的同协议对比时。
