# Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations

> 论文卡片 · `dora` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations |
| 作者 | Junjue Wang; Weihao Xuan; Heli Qi; Pengyu Dai; Kunyi Liu; Hongruixuan Chen; Zhuo Zheng; Junshi Xia; Stefano Ermon; Naoto Yokoya |
| 年份 | 2026 |
| 会址 / 状态 | NeurIPS 2026 |
| arXiv | [arXiv:2605.11633](https://arxiv.org/abs/2605.11633) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://neurips.cc/virtual/2026/poster/139774) |
| Bib key | `dora`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-NeurIPS-DORA-Wang.pdf`](../../pdfs/2026-NeurIPS-DORA-Wang.pdf) |
| 代码 / 项目 | https://github.com/Junjue-Wang/DORA |
| 数据集 | DORA |
| PDF 版本 | arXiv 预印本（正式 proceedings 页码未在本包核对） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 本包使用 arXiv 预印本；正式会址按 NeurIPS 2026 记录，若投正文请以正式 proceedings 复核页码。 |

## 问题与方法

首个端到端灾害响应 agentic benchmark：515 个专家任务、45 场真实灾害、10 类灾害，配 3,500 步可回放黄金轨迹；agent 从 108 个 MCP 工具中组合调用，覆盖感知、空间关系、行动规划、时序演化与多模态报告。

## 核心结论

- DORA 把灾害响应从“损毁评估”扩展到路网、人口、关键设施、疏散规划与行动报告，弥补了 RS 感知与通用工具评测之间的空白。 [摘要]
- 数据含 515 个专家任务、45 场灾害、10 类灾害、3,500 个工具调用步；工具库 108 个，覆盖光学/SAR/多光谱、DEM 与社会矢量层。 [摘要]
- 13 个前沿 LLM 的评测暴露三类问题：灾害域接地失败、工具选择与参数接地双重瓶颈、轨迹越长组合越脆弱。 [摘要]
- 给黄金工具顺序提示只提升 1.08–4.40%，换 scaffold 最多提升 3.24%；agent 与黄金轨迹的差距随流水线变长从 7% 扩大到 56%。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 515 | 专家任务数 | 摘要 | 已核摘要 |
| 45 / 10 | 灾害事件数 / 灾害类型数 | 摘要 | 已核摘要 |
| 3,500 | 黄金轨迹工具调用步 | 摘要 | 已核摘要 |
| 108 | MCP 工具数 | 摘要 | 已核摘要 |
| 1.08–4.40% | 黄金工具顺序提示带来的提升 | 摘要 | 已核摘要 |
| 3.24% | 替代 scaffold 的最大提升 | 摘要 | 已核摘要 |
| 7% → 56% | agent 与黄金轨迹差距随轨迹长度的变化 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

这是 benchmark，不是某个规划算法的有效性证明；不能把 56% 差距写成所有灾害 agent 的普遍上限。任务与黄金轨迹是专家构造的可回放设置，不等于真实应急部署。不能与其他基准横排分数。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks
- [`eo-gym`](eo-gym.md) — EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`disasterm3`](disasterm3.md) — DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response

## 何时必须打开全文

需要五维任务的评分细则、108 工具的参数 schema、黄金轨迹的回放格式、13 个模型的逐维结果，或要设计自己的灾害实验时。
