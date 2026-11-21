# ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks

> 论文卡片 · `thinkgeo` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks |
| 作者 | Akashah Shabbir; Muhammad Akhtar Munir; Akshay Dudhane; Muhammad Umer Sheikh; Muhammad Haris Khan; Paolo Fraccaro; Juan Bernabe Moreno; Fahad Shahbaz Khan; Salman Khan |
| 年份 | 2025 |
| 会址 / 状态 | 预印本（arXiv:2505.23752）。ICLR 2026 OpenReview 显示已撤稿；有 CVPR 2026 MONTI workshop 线索，不以 CVPR 主会论文 |
| arXiv | [arXiv:2505.23752](https://arxiv.org/abs/2505.23752) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2505.23752) |
| Bib key | `thinkgeo`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-arXiv-ThinkGeo-Shabbir.pdf`](../../pdfs/2025-arXiv-ThinkGeo-Shabbir.pdf) |
| 代码 / 项目 | https://github.com/mbzuai-oryx/ThinkGeo · https://mbzuai-oryx.github.io/ThinkGeo/ |
| 数据集 | ThinkGeo |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 只按 arXiv:2505.23752 预印本引用；ICLR 2026 投稿已撤稿，CVPR 2026 workshop 线索不得写成主会。 |

## 问题与方法

用 ReAct 式交互循环评测 LLM agent 在遥感任务上的结构化工具使用与多步规划；任务覆盖城市、灾害、变化、环境、交通、航空、休闲设施与工业场地，输入含光学 RGB 与 SAR。

## 核心结论

- ThinkGeo 含 486 个结构化 agent 任务、1,778 个专家核验推理步；其中光学 RGB 436 条、SAR 50 条。 [正文]
- 评测同时报告 step-wise 执行指标与最终答案正确率，能暴露“中间步骤像对、最终答案错”的分离。 [摘要]
- 任务要求 agent 在卫星/航空影像上通过多种工具完成真实应用分析，而不是固定模板 VQA。 [摘要]
- 论文的分析显示工具执行指标与最终答案之间存在明显落差，SAR 子集尤其能暴露跨模态困难。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 486 | agent 任务数 | 摘要 | 已核摘要 |
| 1,778 | 专家推理步数 | 摘要 | 已核摘要 |
| 436 / 50 | 光学 RGB / SAR 任务数 | 正文 | 已核正文检索 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

只能按 arXiv:2505.23752 预印本引用；ICLR 2026 投稿已撤稿，CVPR 2026 workshop 线索也不能写成主会。不能把 ThinkGeo 分数与 DORA/Earth-Bench 横排。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`eo-gym`](eo-gym.md) — EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents
- [`openearthagent-shabbir`](openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents

## 何时必须打开全文

需要 486 条任务的类别分布、工具清单、SAR 50 条的逐项结果、step/final 指标定义，或要引用具体模型分数时。
