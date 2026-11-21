# LISAT: Language-Instructed Segmentation Assistant for Satellite Imagery

> 论文卡片 · `lisat` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | LISAT: Language-Instructed Segmentation Assistant for Satellite Imagery |
| 作者 | Jerome Quenum; Wen-Han Hsieh; Tsung-Han Wu; Ritwik Gupta; Trevor Darrell; David M. Chan |
| 年份 | 2025 |
| 会址 / 状态 | NeurIPS 2025 Datasets and Benchmarks |
| arXiv | [arXiv:2505.02829](https://arxiv.org/abs/2505.02829) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2505.02829) |
| Bib key | `lisat`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2025-NeurIPS-LISAT.pdf`](../../pdfs/2025-NeurIPS-LISAT.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | GRES, PreGRES |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

语言指令驱动的卫星影像分割助手：描述复杂 RS 场景、回答相关问题并分割目标；训练于 GRES（27,615 个标注、9,205 张图）与 PreGRES（>1M QA）。

## 核心结论

- LISAT 把“推理分割”扩展到 RS：模型需要理解隐含指代多个目标的复杂查询，并输出掩膜。 [摘要]
- GRES 含 27,615 个标注、9,205 张图；PreGRES 含超过 100 万 QA 对用于预训练。 [摘要]
- 论文报告 LISAT 在 RS 推理分割上优于现有通用/RS 模型。 [摘要]
- 它是分割助手，不是工具规划 agent；掩膜输出可作为下游工具的输入。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 27,615 / 9,205 | GRES 标注数 / 图像数 | 摘要 | 已核摘要 |
| >1M | PreGRES QA 对数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把分割精度当作 agent 的裁剪/对齐策略证据。没有灾害多工具流水线。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`geopixel`](geopixel.md) — GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing
- [`terrascope`](terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 GRES 的任务类型、PreGRES 构造、推理分割评测指标时。
