# Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows

> 论文卡片 · `geo-olm` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows |
| 作者 | Dimitrios Stamoulis; Diana Marculescu |
| 年份 | 2025 |
| 会址 / 状态 | ACM COMPASS 2025 |
| arXiv | [arXiv:2504.04319](https://arxiv.org/abs/2504.04319) |
| DOI / 正式页 | [10.1145/3715335.3735494](https://doi.org/10.1145/3715335.3735494) · [正式/开放页](https://arxiv.org/abs/2504.04319) |
| Bib key | `geo-olm`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-COMPASS-Geo-OLM-Stamoulis.pdf`](../../pdfs/2025-COMPASS-Geo-OLM-Stamoulis.pdf) |
| 代码 / 项目 | https://github.com/dstamoulis/geo-olms |
| 数据集 | EO workflows |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

用状态驱动提示把“任务推进”与“工具调用”解耦，使低资源开源语言模型也能完成地理空间工作流，并以成本/能效作为一等目标。

## 核心结论

- Geo-OLM 观察到：直接用开源小模型替换 GPT-4o 会因逻辑依赖 GPT 优化而显著退化。 [摘要]
- 状态驱动推理把任务阶段与工具调用拆开，降低小模型的工作流推理负担。 [摘要]
- 在低于 7B 参数的设置下，论文称相对最强地理空间基线，成功查询完成率提升 32.8%。 [摘要]
- 论文称效果在 GPT-4o 的 10% 以内，同时把推理成本从 500–1000 美元降到 10 美元以下，量级约两个数量级。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| <7B | 小模型参数规模设置 | 摘要 | 已核摘要 |
| 32.8% | 成功查询完成率相对提升 | 摘要 | 已核摘要 |
| 10% | 与 GPT-4o 的效果差距 | 摘要 | 已核摘要 |
| $500–1000 → <$10 | 推理成本变化 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

成本与完成率是特定平台/模型/任务下的结果，不能当作灾害应急的精度证据；不是轨迹级后训练；不能证明小模型在 SAR 定量任务上可靠。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`geollm-squad`](geollm-squad.md) — Multi-Agent Geospatial Copilots for Remote Sensing Workflows
- [`geollm-engine`](geollm-engine.md) — GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`expertsrs`](expertsrs.md) — An LLM-based multi-agent system for remote sensing analysis

## 何时必须打开全文

需要状态机的阶段定义、工具 API 集合、成本核算口径、低于 7B 的具体模型与任务集时。
