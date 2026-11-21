# OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation

> 论文卡片 · `openearth-agent-zhao` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation |
| 作者 | Sijie Zhao; Feng Liu; Xueliang Zhang; Hao Chen; Xinyu Gu; Zhe Jiang; Fenghua Ling; Ben Fei; Wenlong Zhang; Junjue Wang; Weihao Xuan; Pengfeng Xiao; Naoto Yokoya; Lei Bai |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2603.22148）；会址待确认 |
| arXiv | [arXiv:2603.22148](https://arxiv.org/abs/2603.22148) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2603.22148) |
| Bib key | `openearth-agent-zhao`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-arXiv-OpenEarth-Agent-Zhao.pdf`](../../pdfs/2026-arXiv-OpenEarth-Agent-Zhao.pdf) |
| 代码 / 项目 | https://github.com/walking-shadow/OpenEarth-Agent |
| 数据集 | OpenEarth-Bench, Earth-Bench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 与 Shabbir 等的 `openearthagent-shabbir` 是两篇不同论文；本条目强调工具创造，不是工具调用。 |

## 问题与方法

面向开放环境 EO 的工具创造 agent：先探测数据，再做 DAG 工作流规划，按节点生成专用 Python 工具并迭代校验，而不是只调用预定义工具。

## 核心结论

- 论文把“工具调用”推进到“工具创造”：面对未见数据/任务时，agent 通过数据探测、DAG 规划和按节点生成 Python 工具来完成流水线。 [摘要]
- 配套 OpenEarth-Bench 含 596 条真实全流程案例、7 个应用域，只提供必要的预训练模型工具，不提供任务专用工具。 [摘要]
- 在跨基准 Earth-Bench 上，仅带 6 个预训练模型工具的工具创造 agent 接近调用 104 个专用工具的 Earth-Agent；给全工具集时反超。 [摘要]
- 部分生成工具对数据异常的鲁棒性优于人工工程工具，说明“工具创造”可能补上固定工具集覆盖不到的长尾。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 596 | OpenEarth-Bench 全流程案例数 | 摘要 | 已核摘要 |
| 7 | 应用域数量 | 摘要 | 已核摘要 |
| 6 vs 104 | 工具创造 vs Earth-Agent 的工具数对照 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

预印本，会址待确认；“首个工具创造 agent”是作者自述，未独立复核。生成工具的可靠性/安全性没有在灾害应急闭环中验证。不能据此宣称工具创造已优于工具调用。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`openearthagent-shabbir`](openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents
- [`rs-claw`](rs-claw.md) — RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents
- [`rs-claw-evolution`](rs-claw-evolution.md) — RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks

## 何时必须打开全文

需要 DAG 规划表示、工具生成与校验循环、OpenEarth-Bench 的任务分布、与 Earth-Agent 的对齐评测设置时。
