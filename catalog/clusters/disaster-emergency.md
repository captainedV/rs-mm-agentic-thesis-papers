# 灾害应急与可执行评测

> 主题簇 · `disaster-emergency` · 6 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

从灾害感知走向端到端作业：模态切换、空间关系、疏散规划与可回放的轨迹评测。

## 代表论文

### [`dora`](../papers/dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations

DORA 把灾害响应从“损毁评估”扩展到路网、人口、关键设施、疏散规划与行动报告，弥补了 RS 感知与通用工具评测之间的空白；数据含 515 个专家任务、45 场灾害、10 类灾害、3,500 个工具调用步；工具库 108 个，覆盖光学/SAR/多光谱、DEM 与社会矢量层。

[打开卡片](../papers/dora.md) · 2026 · NeurIPS 2026

### [`thinkgeo`](../papers/thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks

ThinkGeo 含 486 个结构化 agent 任务、1,778 个专家核验推理步；其中光学 RGB 436 条、SAR 50 条；评测同时报告 step-wise 执行指标与最终答案正确率，能暴露“中间步骤像对、最终答案错”的分离。

[打开卡片](../papers/thinkgeo.md) · 2025 · 预印本（arXiv:2505.23752）。ICLR 2026 OpenReview 显示已撤稿；有 CVPR 2026 MONTI workshop 线索，不以 CVPR 主会论文引用

### [`eo-gym`](../papers/eo-gym.md) — EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents

EO-Gym 把“交互式取证”写成一等公民：agent 可扩大区域、拉历史观测、在光学与 SAR 之间切换，而不是做固定输入单轮问答；环境含超过 66 万多模态文件、35 个 EO 工具、六类任务族。

[打开卡片](../papers/eo-gym.md) · 2026 · 预印本（arXiv:2605.01250）；会址待确认

### [`rescueadi`](../papers/rescueadi.md) — RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents

RescueADI 指出灾害解译不能只做孤立的分割/检测/VQA，而要把多种感知方法与专用工具串起来；数据含 4,044 张高分辨率影像、16,949 个语义掩膜、14,483 个目标框、13,424 条解译请求，覆盖 9 类请求。

[打开卡片](../papers/rescueadi.md) · 2025 · IEEE TGRS 2025

### [`disasterm3`](../papers/disasterm3.md) — DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response

DisasterM3 的“三多”设定是 multi-hazard、multi-sensor、multi-task；灾后光学常被天气切断，因此显式纳入 SAR；数据含 26,988 张双时相影像、123k 指令对、36 场灾害、10 类灾害。

[打开卡片](../papers/disasterm3.md) · 2025 · NeurIPS 2025 Datasets and Benchmarks

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |
| [`raven`](../papers/raven.md) | 2026 | WACV 2026 Workshop (GeoCV) | 背景文献 |

## 共同能力边界

- DORA、ThinkGeo、EO-Gym 的动作空间、工具集与评分协议不同，任何分数都不能横排成 SOTA 榜。
- 这些是离线、可回放的评测环境，不等于真实应急部署；不能把 benchmark 增益写成业务已落地。
- SAR 子集仍然薄（ThinkGeo 为 50 条），长程报告/疏散/路网任务更薄；不能声称灾害全流水线已被覆盖。
- DisasterM3 是静态指令数据，不能当作工具轨迹评测。

## 写作时何时进入

写灾害场景、端到端作业、长程轨迹评测、光学–SAR 切换或“步骤对但答案错”时进入。写感知精度或静态 VQA 时先看 `perception-foundation` / `static-benchmarks`。
