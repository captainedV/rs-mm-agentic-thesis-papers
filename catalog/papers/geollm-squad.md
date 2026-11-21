# Multi-Agent Geospatial Copilots for Remote Sensing Workflows

> 论文卡片 · `geollm-squad` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Multi-Agent Geospatial Copilots for Remote Sensing Workflows |
| 作者 | Chaehong Lee; Varatheepan Paramanayakam; Andreas Karatzas; Yanan Jian; Michael Fore; Heming Liao; Fuxun Yu; Ruopu Li; Iraklis Anagnostopoulos; Dimitrios Stamoulis |
| 年份 | 2025 |
| 会址 / 状态 | IGARSS 2025 |
| arXiv | [arXiv:2501.16254](https://arxiv.org/abs/2501.16254) |
| DOI / 正式页 | [10.1109/igarss55030.2025.11243915](https://doi.org/10.1109/igarss55030.2025.11243915) · [正式/开放页](https://arxiv.org/abs/2501.16254) |
| Bib key | `geollm-squad`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-IGARSS-GeoLLM-Squad-Lee.pdf`](../../pdfs/2025-IGARSS-GeoLLM-Squad-Lee.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | MODIS, GHS, Hansen GFC, xView, FAIR, fMoW |
| PDF 版本 | arXiv 版本（非 IEEE IGARSS 正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 作者以 PDF 首页 Chaehong Lee 等为准；`SURVEY.md` 表中曾写“Liao 等”，卡片按 PDF 更正，引用时不要沿用旧写法。 |

## 问题与方法

在 AutoGen 与 GeoLLM-Engine 上把 agentic 编排与地理空间任务求解分离，由城市、农业、森林、气候、卫星视觉等专用子 agent 分工完成 RS 工作流。

## 核心结论

- GeoLLM-Squad 的出发点是单 agent 随 RS 任务复杂度上升而退化，因此把编排与任务求解解耦，交给专用子 agent。 [摘要]
- 实现基于开源 AutoGen 与 GeoLLM-Engine，可模块化接入城市监测、森林保护、气候分析和农业研究等应用。 [摘要]
- 论文报告相对当时最强基线，agentic correctness 提升 17%；这是多 agent 分工的直接量化证据。 [摘要]
- 它强调的是任务复杂度扩展性，而不是轨迹级后训练；对 P1 有用，对 P2 只能作为“多 agent 轨迹来源”的背景。 [正文]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 17% | 相对 SOTA 基线的 agentic correctness 提升 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

单一基准、单一套件上的 +17% 不能外推为灾害场景的通用增益；没有证明多 agent 一定优于更好的单 agent 规划器；不能支撑 SAR 切换或参数校验。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`geollm-engine`](geollm-engine.md) — GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots
- [`geommagent`](geommagent.md) — GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows

## 何时必须打开全文

需要子 agent 的职责边界、任务生成协议、agentic correctness 的定义、按任务类型的误差分析时。
