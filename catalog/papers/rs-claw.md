# RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents

> 论文卡片 · `rs-claw` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents |
| 作者 | Liangtian Liu; Zeyuan Wang; Ziyu Li; Kai Ouyang; Zichao Tang; Chengfu Liu; Haifeng Li; Hanwen Yu; Wentao Yang; Cheng Yang; Dongyang Hou |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2605.13391）；会址待确认 |
| arXiv | [arXiv:2605.13391](https://arxiv.org/abs/2605.13391) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2605.13391) |
| Bib key | `rs-claw`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-arXiv-RS-Claw-Liu.pdf`](../../pdfs/2026-arXiv-RS-Claw-Liu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | 无记录 |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

把工具选择从“全量注册”或“RAG 检索”改成主动探索：用 Skill 封装把工具描述分层，agent 先读工具摘要选分支，再按需加载详细说明，最后精确调用。

## 核心结论

- 论文指出全量工具注册会撑爆长程任务的上下文，RAG 检索又可能漏掉关键工具，两者都难以兼顾上下文负载与工具集完整性。 [摘要]
- RS-Claw 用层级化 Skill 树组织海量异构 RS 工具，把工具描述拆成摘要层与细节层。 [摘要]
- agent 按需逐层展开，先选相关技能分支，再加载参数级说明，从而在长程任务中控制上下文。 [摘要]
- 这是“工具空间主动探索”的架构贡献，适合支撑 P1 中“工具选择不是一次检索”的论点。 [摘要]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

预印本；没有灾害/SAR 的端到端证据，也没有可与其他基准横排的分数。不能声称层级 Skill 树一定优于更强的规划模型。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`rs-claw-evolution`](rs-claw-evolution.md) — RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`openearth-agent-zhao`](openearth-agent-zhao.md) — OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation
- [`hirs-agent`](hirs-agent.md) — HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving

## 何时必须打开全文

需要 Skill 树的结构、摘要/细节的触发规则、工具数量与上下文预算、消融结果时。
