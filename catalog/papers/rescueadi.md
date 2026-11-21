# RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents

> 论文卡片 · `rescueadi` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents |
| 作者 | Zhuoran Liu; Danpei Zhao; Bo Yuan |
| 年份 | 2025 |
| 会址 / 状态 | IEEE TGRS 2025 |
| arXiv | [arXiv:2410.13384](https://arxiv.org/abs/2410.13384) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2410.13384) |
| Bib key | `rescueadi`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-TGRS-RescueADI-Liu.pdf`](../../pdfs/2025-TGRS-RescueADI-Liu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RescueADI |
| PDF 版本 | arXiv 版本（非 IEEE TGRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

提出 Adaptive Disaster Interpretation（ADI）任务：agent 根据请求规划并顺序执行多个相互关联的解译任务，给出灾害场景的综合分析；配套 RescueADI 数据。

## 核心结论

- RescueADI 指出灾害解译不能只做孤立的分割/检测/VQA，而要把多种感知方法与专用工具串起来。 [摘要]
- 数据含 4,044 张高分辨率影像、16,949 个语义掩膜、14,483 个目标框、13,424 条解译请求，覆盖 9 类请求。 [摘要]
- 标注同时覆盖 planning、perception、recognition 三个方面，可直接监督多步任务规划。 [摘要]
- 它是灾害任务级规划数据，但不是多传感器（SAR）切换或 MCP 工具生态。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 4,044 | 影像数 | 摘要 | 已核摘要 |
| 16,949 | 语义掩膜数 | 摘要 | 已核摘要 |
| 14,483 | 目标框数 | 摘要 | 已核摘要 |
| 13,424 | 解译请求数 | 摘要 | 已核摘要 |
| 9 | 请求类型数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P2；不能把 ADI 的规划能力写成“光学–SAR 切换策略”。数据以高分辨率光学灾害影像为主，跨传感器泛化未验证。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`disasterm3`](disasterm3.md) — DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response
- [`change-agent`](change-agent.md) — Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis
- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks

## 何时必须打开全文

需要 9 类请求的定义、planning 标注格式、工具/模型清单、评价指标时。
