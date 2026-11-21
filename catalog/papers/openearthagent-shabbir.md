# OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents

> 论文卡片 · `openearthagent-shabbir` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P2 轨迹级后训练**

| 字段 | 值 |
| --- | --- |
| 标题 | OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents |
| 作者 | Akashah Shabbir; Muhammad Umer Sheikh; Muhammad Akhtar Munir; Hiyam Debary; Mustansar Fiaz; Muhammad Zaigham Zaheer; Paolo Fraccaro; Fahad Shahbaz Khan; Muhammad Haris Khan; Xiao Xiang Zhu; Salman Khan |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2602.17665）；有 ECCV 2026 poster 线索，需与正式论文集再核 |
| arXiv | [arXiv:2602.17665](https://arxiv.org/abs/2602.17665) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2602.17665) |
| Bib key | `openearthagent-shabbir`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-arXiv-OpenEarthAgent-Shabbir.pdf`](../../pdfs/2026-arXiv-OpenEarthAgent-Shabbir.pdf) |
| 代码 / 项目 | https://github.com/mbzuai-oryx/OpenEarthAgent |
| 数据集 | OpenEarthAgent corpus |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 与 Zhao 等的 `openearth-agent-zhao` 是两篇不同论文；ECCV 2026 poster 线索未核正式论文集，按预印本处理。 |

## 问题与方法

把视觉、光谱、GIS 与地理栅格操作统一到可执行工具注册表，再用结构化推理轨迹做监督微调（Qwen3-4B 量级），并用确定性回放验证可执行性与空间正确性。

## 核心结论

- 核心贡献是统一可执行工具注册表 + 轨迹策略学习，而不是只给一个 benchmark。 [摘要]
- 语料含 14,538 条训练、1,169 条评测实例，超过 107K 推理步，覆盖城市、环境、灾害与基础设施域。 [摘要]
- 工具面覆盖光学/SAR、GIS 操作与 NDVI/NBR/NDBI 等指数分析，直接对应“多源 + 工具参数”的 thesis 关切。 [摘要]
- 训练用确定性回放校验轨迹可执行性与空间正确性；这为 P2 的“步骤可执行但答案错”提供了可借鉴的监督接口。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 14,538 | 训练实例数 | 摘要 | 已核摘要 |
| 1,169 | 评测实例数 | 摘要 | 已核摘要 |
| 107K+ | 推理步数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

会址只能写 arXiv 预印本；ECCV 2026 poster 线索未与正式论文集交叉核到，不得写成 ECCV 录用。不能与 Zhao 等的 OpenEarth-Agent 混用。它主要报告自身语料上的提升，不能证明跨灾害/跨 SAR 泛化。

## 与主张的关系

**P2 轨迹级后训练**。这篇涉及轨迹监督、蒸馏、RL 或过程奖励，可作为 P2 的方法参照；若未分别报告“步骤正确/答案正确”，不能声称它降低了“步骤对、答案错”。

## 相关论文

- [`openearth-agent-zhao`](openearth-agent-zhao.md) — OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks
- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning

## 何时必须打开全文

需要工具 schema、轨迹格式、回放校验规则、SFT 数据构造、错误类型分布，或要与 Zhao 的工具创造路线对照时。
