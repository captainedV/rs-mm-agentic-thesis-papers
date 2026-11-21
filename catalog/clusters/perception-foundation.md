# 感知底座与多源视觉语言模型

> 主题簇 · `perception-foundation` · 24 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

光学/SAR/多光谱的视觉前端与对照基线；默认不是工具规划方法。

## 代表论文

### [`earthdial`](../papers/earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues

EarthDial 的定位是“把多感官 EO 观测转成交互对话”，覆盖 RGB、SAR、多光谱（含 NIR/红外）等模态；训练集 EarthDial-Instruct 超过 11.11M 指令对，覆盖 44 个下游 EO 任务。

[打开卡片](../papers/earthdial.md) · 2025 · CVPR 2025

### [`teochat`](../papers/teochat.md) — TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data

TEOChat 解决的是“只能看单张图”的限制，把多时相序列作为输入做对话与推理；训练数据同时包含单图任务与时序任务，覆盖建筑变化、损毁评估、语义变化检测等。

[打开卡片](../papers/teochat.md) · 2025 · ICLR 2025

### [`fusar-gpt`](../papers/fusar-gpt.md) — FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery

FUSAR-GPT 针对 SAR 成像机制复杂、散射特征敏感、高质量文本稀缺的问题，做 SAR 专用 VLM；主要数据贡献是 SAR Image-Text-AlphaEarth 特征三元组，把地理空间基线作为世界知识先验。

[打开卡片](../papers/fusar-gpt.md) · 2026 · CVPR 2026

### [`fusar-klip`](../papers/fusar-klip.md) — FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing

论文指出 SAR 的相干成像机制与通用图像存在显著模态异质性，直接套用通用 VLM 不合适；FUSAR-KLIP 用知识引导做 SAR 多模态基础模型，并构建大规模 SAR 图文/地理知识数据。

[打开卡片](../papers/fusar-klip.md) · 2025 · 预印本（arXiv:2509.23927）；会址待确认

### [`earthgpt`](../papers/earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain

EarthGPT 的目标是用一个 MLLM 统一多传感器 RS 解译任务，而不是每个传感器/任务一个模型；MMRS-1M 含超过 100 万图文对，来自 34 个既有 RS 数据集，覆盖光学、SAR、红外。

[打开卡片](../papers/earthgpt.md) · 2024 · IEEE TGRS 2024

### [`ringmo-agent`](../papers/ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning

RingMo-Agent 的数据覆盖面是其主要贡献：3 个模态、2 个平台、8 类任务的 300 万+ 图文对；它不只做分类/字幕，还覆盖空间推理与具身导航类任务，处于 VLM 与 agent 之间。

[打开卡片](../papers/ringmo-agent.md) · 2026 · IEEE TPAMI（DOI: 10.1109/tpami.2026.3718699；卷期页以 Xplore 为准）

### [`terrascope`](../papers/terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation

TerraScope 把“答案 + 掩膜”放在同一条推理链里，要求模型在像素级证据上推理；它支持单模态（光学或 SAR）与双模态自适应融合，也支持多时相变化分析。

[打开卡片](../papers/terrascope.md) · 2026 · CVPR 2026

### [`skysense`](../papers/skysense.md) — SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery

SkySense 的核心是多模态时空编码：同时处理光学与 SAR 的时序序列，而不是单幅单模态；预训练数据含 2150 万时序序列，规模远大于多数 RS VLM 的图文数据。

[打开卡片](../papers/skysense.md) · 2024 · CVPR 2024

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |
| [`remotereasoner`](../papers/remotereasoner.md) | 2026 | AAAI 2026 | 仅作感知底座或对照 |
| [`spext`](../papers/spext.md) | 2026 | NeurIPS 2026 | 仅作感知底座或对照 |
| [`skymoe`](../papers/skymoe.md) | 2026 | AAAI（OJS 37653）；届次以期刊页为准 | 仅作感知底座或对照 |
| [`zoomearth`](../papers/zoomearth.md) | 2026 | CVPR 2026 | 仅作感知底座或对照 |
| [`falcon`](../papers/falcon.md) | 2025 | 技术报告（arXiv:2503.11070）；会址待确认 | 仅作感知底座或对照 |
| [`geopixel`](../papers/geopixel.md) | 2025 | ICML 2025 | 仅作感知底座或对照 |
| [`lisat`](../papers/lisat.md) | 2025 | NeurIPS 2025 Datasets and Benchmarks | 仅作感知底座或对照 |
| [`rsgpt`](../papers/rsgpt.md) | 2025 | ISPRS Journal of Photogrammetry and Remote Sensing 2025 | 仅作感知底座或对照 |
| [`skyeyegpt`](../papers/skyeyegpt.md) | 2025 | ISPRS Journal of Photogrammetry and Remote Sensing 2025 | 仅作感知底座或对照 |
| [`geochat`](../papers/geochat.md) | 2024 | CVPR 2024 | 仅作感知底座或对照 |
| [`lhrs-bot-nova`](../papers/lhrs-bot-nova.md) | 2024 | 预印本（arXiv:2411.09301）；会址待确认 | 仅作感知底座或对照 |
| [`lhrs-bot`](../papers/lhrs-bot.md) | 2024 | ECCV 2024 | 仅作感知底座或对照 |
| [`rs-llava`](../papers/rs-llava.md) | 2024 | Remote Sensing 16(9):1477 | 仅作感知底座或对照 |
| [`rs-moe`](../papers/rs-moe.md) | 2024 | 预印本（arXiv:2411.01595）；会址待确认 | 仅作感知底座或对照 |
| [`remoteclip`](../papers/remoteclip.md) | 2024 | IEEE TGRS 2024 | 仅作感知底座或对照 |
| [`skysensegpt`](../papers/skysensegpt.md) | 2024 | 预印本（arXiv:2406.10100）；至交接清单完成时仍以预印本为主 | 仅作感知底座或对照 |

## 共同能力边界

- 这些是视觉前端或对照基线，默认不能替代模态–工具规划方法。
- 支持 SAR/多光谱/时序是感知能力，不是“何时切换、如何裁剪、如何校验参数”的策略。
- 模型名含 Agent（如 RingMo-Agent）也不等于通用工具 agent；其工具面很窄。
- 各文预训练数据、分辨率与任务协议差异很大，分数不能横排。

## 写作时何时进入

写感知底座、SAR/多光谱视觉前端、对比基线或“为什么通用 VLM 不够”时进入。不要用它证明工具规划。
