# DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response

> 论文卡片 · `disasterm3` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response |
| 作者 | Junjue Wang; Weihao Xuan; Heli Qi; Zhihao Liu; Kunyi Liu; Yuhan Wu; Hongruixuan Chen; Jian Song; Junshi Xia; Zhuo Zheng; Naoto Yokoya |
| 年份 | 2025 |
| 会址 / 状态 | NeurIPS 2025 Datasets and Benchmarks |
| arXiv | 无 |
| DOI / 正式页 | 仓库未记录 DOI · 仓库未记录 |
| Bib key | `disasterm3`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-NeurIPS-DisasterM3-Wang.pdf`](../../pdfs/2025-NeurIPS-DisasterM3-Wang.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | DisasterM3 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

全球尺度灾害遥感视觉–语言数据集：26,988 张双时相卫星图、123k 指令对，覆盖 5 大洲、36 场灾害、10 类灾害与 9 个灾害任务，含灾后 SAR。

## 核心结论

- DisasterM3 的“三多”设定是 multi-hazard、multi-sensor、multi-task；灾后光学常被天气切断，因此显式纳入 SAR。 [摘要]
- 数据含 26,988 张双时相影像、123k 指令对、36 场灾害、10 类灾害。 [摘要]
- 9 个任务从承灾体识别、结构损毁评估到对象关系推理，最终到长文本灾害报告。 [摘要]
- 14 个通用/RS VLM 在灾害任务上明显吃力；微调 4 个模型后报告最高 +10.4% QA、+2.1 Report、+40.8% Referring Seg.。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 26,988 | 双时相影像数 | 摘要 | 已核摘要 |
| 123k | 指令对数 | 摘要 | 已核摘要 |
| 36 / 10 | 灾害事件数 / 类型数 | 摘要 | 已核摘要 |
| 9 | 灾害任务数 | 摘要 | 已核摘要 |
| +10.4% / +2.1 / +40.8% | QA / Report / Referring Seg. 的最高提升 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

这是静态指令数据集，不是 agent 轨迹或工具调用 benchmark；不能支撑 P1/P2。其 +10.4% 等数字是特定模型/任务上的微调结果，不能写成“灾害 VLM 已解决”。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`rescueadi`](rescueadi.md) — RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents
- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`teochat`](teochat.md) — TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data

## 何时必须打开全文

需要 9 个任务的定义、SAR 子集比例、微调模型与评测协议、报告生成指标时。
