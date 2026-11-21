# FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery

> 论文卡片 · `fusar-gpt` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery |
| 作者 | Xiaokun Zhang; Yi Yang; Ziqi Ye; Baiyun Baiyun; Xiaorong Guo; Qingchen Fang; Ruyi Zhang; Xinpeng Zhou; Haipeng Wang |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_FUSAR-GPT_A_Spatiotemporal_Feature-Embedded_and_Two-Stage_Decoupled_Visual_Language_Model_CVPR_2026_paper.html) |
| Bib key | `fusar-gpt`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-CVPR-FUSAR-GPT-Zhang.pdf`](../../pdfs/2026-CVPR-FUSAR-GPT-Zhang.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | SAR vision-language |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 无 arXiv；本包为 CVF Open Access 正式 PDF。 |

## 问题与方法

SAR 专用 VLM：构建 SAR Image-Text-AlphaEarth 三元组数据，把地理空间基线模型作为“世界知识”先验，并通过“时空锚点”把多源时序特征嵌入视觉骨干，两阶段解耦训练。

## 核心结论

- FUSAR-GPT 针对 SAR 成像机制复杂、散射特征敏感、高质量文本稀缺的问题，做 SAR 专用 VLM。 [摘要]
- 主要数据贡献是 SAR Image-Text-AlphaEarth 特征三元组，把地理空间基线作为世界知识先验。 [摘要]
- “时空锚点”把多源遥感时序特征嵌入视觉骨干，用于动态补偿稀疏表示。 [摘要]
- 它是 SAR 感知底座，不是 tool-augmented agent；不能替代工具规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把 SAR VLM 的理解能力写成“会决定何时切换 SAR 并调用检测/分割工具”。没有灾害端到端实验。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`fusar-klip`](fusar-klip.md) — FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing
- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain
- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning

## 何时必须打开全文

需要三元组数据构造、时空锚点实现、两阶段解耦训练细节与 SAR 评测协议时。
