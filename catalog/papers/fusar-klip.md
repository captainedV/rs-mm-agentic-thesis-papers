# FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing

> 论文卡片 · `fusar-klip` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing |
| 作者 | Yi Yang; Xiaokun Zhang; Qingchen Fang; Jing Liu; Ziqi Ye; Rui Li; Li Liu; Haipeng Wang |
| 年份 | 2025 |
| 会址 / 状态 | 预印本（arXiv:2509.23927）；会址待确认 |
| arXiv | [arXiv:2509.23927](https://arxiv.org/abs/2509.23927) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2509.23927) |
| Bib key | `fusar-klip`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2025-arXiv-FUSAR-KLIP-Yang.pdf`](../../pdfs/2025-arXiv-FUSAR-KLIP-Yang.pdf) |
| 代码 / 项目 | https://github.com/yangyifremad/FUSAR-KLIP |
| 数据集 | SAR multimodal |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

首个知识引导的 SAR 通用多模态基础模型，配套 FUSAR-GEOVL-1M 数据与可复用评测基线，目标是把 SAR 与地理知识/语言对齐。

## 核心结论

- 论文指出 SAR 的相干成像机制与通用图像存在显著模态异质性，直接套用通用 VLM 不合适。 [摘要]
- FUSAR-KLIP 用知识引导做 SAR 多模态基础模型，并构建大规模 SAR 图文/地理知识数据。 [摘要]
- 它提供可复用的数据与评测基线，适合做 SAR 感知前端或对照。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

预印本，会址待确认；不能支撑工具规划；不能把 SAR 图文对齐当作 SAR 工具参数接地。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`fusar-gpt`](fusar-gpt.md) — FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery
- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain
- [`remoteclip`](remoteclip.md) — RemoteCLIP: A Vision Language Foundation Model for Remote Sensing
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning

## 何时必须打开全文

需要 FUSAR-GEOVL-1M 的规模与构造、知识引导方式、评测基线时。
