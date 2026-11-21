# EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues

> 论文卡片 · `earthdial` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues |
| 作者 | Sagar Soni; Akshay Dudhane; Hiyam Debary; Mustansar Fiaz; Muhammad Akhtar Munir; Muhammad Sohail Danish; Paolo Fraccaro; Campbell D Watson; Levente J Klein; Fahad Shahbaz Khan; Salman Khan |
| 年份 | 2025 |
| 会址 / 状态 | CVPR 2025 |
| arXiv | [arXiv:2412.15190](https://arxiv.org/abs/2412.15190) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/CVPR2025/papers/Soni_EarthDial_Turning_Multi-sensory_Earth_Observations_to_Interactive_Dialogues_CVPR_2025_paper.pdf) |
| Bib key | `earthdial`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-CVPR-EarthDial-Soni.pdf`](../../pdfs/2025-CVPR-EarthDial-Soni.pdf) |
| 代码 / 项目 | https://github.com/hiyamdebary/EarthDial |
| 数据集 | EarthDial-Instruct |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

面向 EO 数据的对话式 VLM，支持多光谱、多时相、多分辨率与 SAR 输入，并把分类、检测、字幕、VQA、视觉推理与 grounding 统一到指令对话中。

## 核心结论

- EarthDial 的定位是“把多感官 EO 观测转成交互对话”，覆盖 RGB、SAR、多光谱（含 NIR/红外）等模态。 [摘要]
- 训练集 EarthDial-Instruct 超过 11.11M 指令对，覆盖 44 个下游 EO 任务。 [正文]
- 它支持多分辨率与多时相，因此比固定分辨率、少模态的早期 RS VLM 更接近多源业务。 [摘要]
- 但它是单轮/对话式视觉前端，不包含外部工具注册、参数校验或长程规划。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 11.11M+ | EarthDial-Instruct 指令对数 | 正文 Table 1 / 摘要 | 已核正文检索 |
| 44 | 下游 EO 任务数 | 正文 | 已核正文检索 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能写成“可以替代模态–工具规划的智能体方法”；不能把 EarthDial 的对话能力当作工具调用能力。多传感器支持是感知层能力，不是 SAR–光学切换策略。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`teochat`](teochat.md) — TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning
- [`fusar-gpt`](fusar-gpt.md) — FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 44 个下游任务的清单、SAR/多光谱子集结果、指令数据构造与多时相协议时。
