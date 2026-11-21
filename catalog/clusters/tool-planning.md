# 工具规划、MCP 与遥感智能体

> 主题簇 · `tool-planning` · 13 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

外部工具注册、选择、参数接地、模态切换与工具创造；这是 P1 的主战场。

## 代表论文

### [`earth-agent`](../papers/earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

Earth-Agent 的核心不是再训一个更强的 EO MLLM，而是把 104 个专家工具/模型通过 MCP 组织成可调用生态，用 ReAct 完成跨模态多步推理；Earth-Bench 含 248 个专家题、13,729 张图，覆盖 spectrum、products、RGB 三种模态，并采用轨迹与最终结果的双层评测。

[打开卡片](../papers/earth-agent.md) · 2026 · ICLR 2026

### [`openearth-agent-zhao`](../papers/openearth-agent-zhao.md) — OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation

论文把“工具调用”推进到“工具创造”：面对未见数据/任务时，agent 通过数据探测、DAG 规划和按节点生成 Python 工具来完成流水线；配套 OpenEarth-Bench 含 596 条真实全流程案例、7 个应用域，只提供必要的预训练模型工具，不提供任务专用工具。

[打开卡片](../papers/openearth-agent-zhao.md) · 2026 · 预印本（arXiv:2603.22148）；会址待确认

### [`openearthagent-shabbir`](../papers/openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents

核心贡献是统一可执行工具注册表 + 轨迹策略学习，而不是只给一个 benchmark；语料含 14,538 条训练、1,169 条评测实例，超过 107K 推理步，覆盖城市、环境、灾害与基础设施域。

[打开卡片](../papers/openearthagent-shabbir.md) · 2026 · 预印本（arXiv:2602.17665）；有 ECCV 2026 poster 线索，需与正式论文集再核

### [`rs-claw`](../papers/rs-claw.md) — RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents

论文指出全量工具注册会撑爆长程任务的上下文，RAG 检索又可能漏掉关键工具，两者都难以兼顾上下文负载与工具集完整性；RS-Claw 用层级化 Skill 树组织海量异构 RS 工具，把工具描述拆成摘要层与细节层。

[打开卡片](../papers/rs-claw.md) · 2026 · 预印本（arXiv:2605.13391）；会址待确认

### [`change-agent`](../papers/change-agent.md) — Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis

Change-Agent 针对 RS 变化解译中“检测”和“字幕”各自为战的问题，把两者统一进交互式分析；MCI 模型含像素级变化检测与语义级变化字幕两支，并用 BI3 层增强双时相交互特征。

[打开卡片](../papers/change-agent.md) · 2024 · IEEE TGRS 2024

### [`rs-agent`](../papers/rs-agent.md) — RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent

RS-Agent 把 RS 工作流拆成中央控制器、动态工具包、Solution Space 与 Knowledge Space 四部分，是早期“规划 + 工具编排”的代表；Task-Aware Retrieval 先推断任务类型再检索专家流程，避免只按查询相似度拼工具链。

[打开卡片](../papers/rs-agent.md) · 2024 · 预印本（arXiv:2406.07089）；正文有 Science China Information Sciences 2025 卷线索，期刊页待交叉确认

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |
| [`expertsrs`](../papers/expertsrs.md) | 2026 | Big Earth Data | P1 模态–工具规划 |
| [`geo-olm`](../papers/geo-olm.md) | 2025 | ACM COMPASS 2025 | P1 模态–工具规划 |
| [`univearth`](../papers/univearth.md) | 2025 | 预印本（arXiv:2504.12110）；会址待确认。arXiv 注释写 ACL 2026 Findings，本轮未在 Anthology 交叉核到正式页，不升格 | P1 模态–工具规划 |
| [`geoagent-chen`](../papers/geoagent-chen.md) | 2024 | 预印本（arXiv:2410.18792）；会址待确认 | P1 模态–工具规划 |
| [`eval-tool-agents`](../papers/eval-tool-agents.md) | 2024 | 预印本（arXiv:2405.00709）；会址按预印本 | 背景文献 |
| [`geollm-engine`](../papers/geollm-engine.md) | 2024 | CVPR 2024 Workshop (EarthVision) | 背景文献 |
| [`rs-chatgpt`](../papers/rs-chatgpt.md) | 2024 | IGARSS 2024 | 背景文献 |

## 共同能力边界

- 工具数量、是否给黄金工具提示、动作空间与评分都不同；“工具多”不等于“规划强”。
- “支持 SAR/多光谱”是输入能力，不等于已验证光学–SAR 切换策略或参数接地。
- OpenEarthAgent（Shabbir）、OpenEarth-Agent（Zhao）、RS-Claw 等仍为预印本；不得写成主会录用。
- 固定工具调用与工具创造是两条设计轴，现有证据不足以判定哪条普遍更优。

## 写作时何时进入

写 P1 的方法、工具生态、MCP/ReAct、工具选择/参数接地、工具创造或长程规划时进入。写 P2 训练目标时转到 `post-training`。
