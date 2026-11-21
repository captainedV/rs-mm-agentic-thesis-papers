# RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow

> 论文卡片 · `remotereasoner` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow |
| 作者 | Liang Yao; Fan Liu; Hongbo Lu; Chuanyi Zhang; Rui Min; Shengxiang Xu; Shimin Di; Pai Peng |
| 年份 | 2026 |
| 会址 / 状态 | AAAI 2026 |
| arXiv | [arXiv:2507.19280](https://arxiv.org/abs/2507.19280) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2507.19280) |
| Bib key | `remotereasoner`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-AAAI-RemoteReasoner-Yao.pdf`](../../pdfs/2026-AAAI-RemoteReasoner-Yao.pdf) |
| 代码 / 项目 | https://github.com/1e12Leon/RemoteReasoner |
| 数据集 | multi-granularity geospatial reasoning |
| PDF 版本 | arXiv 版本（非 AAAI 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

统一的 geospatial reasoning workflow：让模型自主探索推理路径，而不是被限定在预定义 ground-truth 序列；用强化学习与任务特定奖励统一多种推理任务。

## 核心结论

- RemoteReasoner 的目标是让 EO 推理“自主探索推理路径”，而不是监督微调+任务头的固定流程。 [摘要]
- 它把多种地理空间推理任务统一到一个模型/工作流中，减少任务专用头。 [摘要]
- 强化学习与任务奖励用于优化推理路径，但工具调用仍发生在模型内部，不是外部工具编排。 [目录判断]
- 它适合作为“模型内推理”对照，说明不调用外部工具也能做部分地理空间推理。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1 的外部工具规划；不能把“自主推理路径”等同于“可执行工具轨迹”。没有灾害或 SAR 切换评测。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`terrascope`](terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation
- [`geocot`](geocot.md) — GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective
- [`socrates`](socrates.md) — Asking like Socrates: Socrates helps VLMs understand remote sensing images
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 RL 奖励设计、推理路径表示、统一任务的评测协议时。
