# TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation

> 论文卡片 · `terrascope` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation |
| 作者 | Yan Shu; Bin Ren; Zhitong Xiong; Xiao Xiang Zhu; Begüm Demir; Nicu Sebe; Paolo Rota |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | [arXiv:2603.19039](https://arxiv.org/abs/2603.19039) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2603.19039) |
| Bib key | `terrascope`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-CVPR-TerraScope-Shu.pdf`](../../pdfs/2026-CVPR-TerraScope-Shu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | Terra-CoT, TerraScope-Bench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

像素接地的 EO 视觉推理模型：支持光学或 SAR 单模态、双模态自适应融合与多时相推理，并在推理链中交错生成像素级掩膜；配套 Terra-CoT（100 万样本）与 TerraScope-Bench。

## 核心结论

- TerraScope 把“答案 + 掩膜”放在同一条推理链里，要求模型在像素级证据上推理。 [摘要]
- 它支持单模态（光学或 SAR）与双模态自适应融合，也支持多时相变化分析。 [摘要]
- Terra-CoT 含 100 万样本，掩膜嵌入推理链；TerraScope-Bench 同时评估答案准确率与掩膜质量。 [摘要]
- 论文明确把自己与“依赖外部工具的 EO VLM”对照，属于模型内像素推理路线。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 1M | Terra-CoT 样本数 | 摘要 | 已核摘要 |
| 6 | TerraScope-Bench 子任务数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1 的工具规划；不能把“自适应融合光学/SAR”写成“会决定何时切换传感器并调用工具”。它是强感知/推理对照，不是 agent。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`geopixel`](geopixel.md) — GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing
- [`remotereasoner`](remotereasoner.md) — RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning
- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues

## 何时必须打开全文

需要双模态融合机制、掩膜质量指标、TerraScope-Bench 六子任务定义时。
