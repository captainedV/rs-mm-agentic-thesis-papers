# Towards LLM Agents for Earth Observation

> 论文卡片 · `univearth` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Towards LLM Agents for Earth Observation |
| 作者 | Chia Hsiang Kao; Wenting Zhao; Cheryl Lam; Aarush Umap; Shreelekha Revankar; Samuel Speas; Snehal Bhagat; Rajeev Datta; Cheng Perng Phoo; Utkarsh Mall; Carl Vondrick; Kavita Bala; Bharath Hariharan |
| 年份 | 2025 |
| 会址 / 状态 | 预印本（arXiv:2504.12110）；会址待确认。arXiv 注释写 ACL 2026 Findings，本轮未在 Anthology 交叉核到正式页，不升格 |
| arXiv | [arXiv:2504.12110](https://arxiv.org/abs/2504.12110) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://iandrover.github.io/2025_univearth/) |
| Bib key | `univearth`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-arXiv-UnivEARTH-Kao.pdf`](../../pdfs/2025-arXiv-UnivEARTH-Kao.pdf) |
| 代码 / 项目 | https://iandrover.github.io/2025_univearth/ |
| 数据集 | UnivEARTH |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | arXiv 注释写 ACL 2026 Findings，但未在 Anthology 交叉核到正式页；按预印本处理，不升格。 |

## 问题与方法

从 NASA Earth Observatory 文章构建 408 道需要 GEE 代码取证的“是/否”题，覆盖 7 个主题、15+ 卫星仪器，用 Google Earth Engine API 做零样本代码 agent 评测。

## 核心结论

- UnivEARTH 把 EO agent 的任务定义为“写代码取证并回答是/否”，更接近真实科学核查而不是模板化 VQA。 [摘要]
- 零样本设置下 LLM agent 准确率 40.0%，代码无法运行的比例超过 44%。 [摘要]
- 加入 reflexion 后，Claude-4.5-Sonnet、Gemini-2.5-Pro、GPT-5 的准确率升到约 60%，但仍只略高于随机。 [摘要]
- 论文还比较 JavaScript/Python API 与提供文档的影响，说明工具接口与上下文是代码 agent 的关键变量。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 408 | 是/否题数 | 摘要 | 已核摘要 |
| 40.0% | 零样本准确率 | 摘要 | 已核摘要 |
| >44% | 代码无法运行比例 | 摘要 | 已核摘要 |
| ~60% | reflexion 后准确率 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

它是 GEE 代码 benchmark，不是多传感器灾害规划；没有光学–SAR 切换、没有检测/分割工具链。不能把 40%/60% 当作所有 EO agent 的上限。会址按预印本处理，不升格 ACL Findings。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`geoagent-chen`](geoagent-chen.md) — An LLM Agent for Automatic Geospatial Data Analysis
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`geo-olm`](geo-olm.md) — Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows

## 何时必须打开全文

需要题目构造、代码执行环境、reflexion 轮数、JS/Python 差异、文档注入方式时。
