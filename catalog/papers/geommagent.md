# GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing

> 论文卡片 · `geommagent` · 主题簇 [后训练、轨迹蒸馏与多智能体分工](../clusters/post-training.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing |
| 作者 | Aoran Xiao; Shihao Cheng; Yonghao Xu; Yexian Ren; Hongruixuan Chen; Naoto Yokoya |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | [arXiv:2604.08896](https://arxiv.org/abs/2604.08896) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/CVPR2026/papers/Xiao_GeoMMBench_and_GeoMMAgent_Toward_Expert-Level_Multimodal_Intelligence_in_Geoscience_and_CVPR_2026_paper.pdf) |
| Bib key | `geommagent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-CVPR-GeoMMBench-GeoMMAgent-Xiao.pdf`](../../pdfs/2026-CVPR-GeoMMBench-GeoMMAgent-Xiao.pdf) |
| 代码 / 项目 | https://geo-mm-agi.github.io/ |
| 数据集 | GeoMMBench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

先构建跨学科、多传感器、多任务的 GeoMMBench，评估 36 个开源/闭源模型；再提出检索–感知–推理多 agent 框架 GeoMMAgent，用领域 RS 模型和工具增强独立 LLM。

## 核心结论

- GeoMMBench 覆盖多学科、多传感器和多任务，目的是把“专家级”地学多模态能力拆成可诊断的维度。 [摘要]
- 对 36 个开源与闭源模型的评估显示，领域知识、感知接地与推理存在系统性不足，单靠通用 MLLM 不够。 [摘要]
- GeoMMAgent 把检索、感知、推理拆给不同 agent，并调用领域 RS 模型/工具；实验称其显著优于 standalone LLM。 [摘要]
- 它支持“多 agent 分工 + 外部工具”这一路线，但不能据此声称某个具体规划策略或后训练目标更优。 [正文]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 36 | 评估的开源/闭源模型数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不是轨迹级后训练论文，不能支撑 P2；没有公开、可复现的单一代码入口被仓库确认；GeoMMBench 分数不能与 Earth-Bench/ThinkGeo/DORA 直接比较。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`geollm-squad`](geollm-squad.md) — Multi-Agent Geospatial Copilots for Remote Sensing Workflows
- [`simcraft`](simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning
- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks

## 何时必须打开全文

需要 GeoMMBench 的题量、任务分布、36 个模型的逐项分数、GeoMMAgent 的 agent 拓扑与工具调用协议时。
