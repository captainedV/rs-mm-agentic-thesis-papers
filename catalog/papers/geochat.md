# GeoChat: Grounded Large Vision-Language Model for Remote Sensing

> 论文卡片 · `geochat` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | GeoChat: Grounded Large Vision-Language Model for Remote Sensing |
| 作者 | Kartik Kuckreja; Muhammad Sohail Danish; Muzammal Naseer; Abhijit Das; Salman Khan; Fahad Shahbaz Khan |
| 年份 | 2024 |
| 会址 / 状态 | CVPR 2024 |
| arXiv | [arXiv:2311.15826](https://arxiv.org/abs/2311.15826) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2311.15826) |
| Bib key | `geochat`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-CVPR-GeoChat-Kuckreja.pdf`](../../pdfs/2024-CVPR-GeoChat-Kuckreja.pdf) |
| 代码 / 项目 | https://github.com/mbzuai-oryx/geochat |
| 数据集 | GeoChat instruction data |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

首个面向 RS 的 grounded 对话 VLM：支持区域输入与坐标输出，用约 318k 指令数据做 RS 多任务对话，是后续大量 RS-MLLM/agent 的对比基线。

## 核心结论

- GeoChat 的核心是 region-level reasoning：用户可给区域，模型可输出坐标，而不只做整图描述。 [摘要]
- 它构建了约 318k 条 RS 多模态指令跟随数据，覆盖对话、描述、定位等任务。 [正文]
- 它让 RS VLM 具备“指哪看哪”的交互能力，是裁剪/对齐类工具的重要感知前端。 [摘要]
- 但它没有外部工具注册或长程规划，不能当作 agent 方法。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 318k | 指令数据量（约） | 正文 | 已核正文检索 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把 grounded 对话当作工具调用。不能把 GeoChat 的定位分数写成 agent 的裁剪策略收益。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain
- [`geopixel`](geopixel.md) — GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing
- [`lhrs-bot`](lhrs-bot.md) — LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 318k 数据的任务构成、区域输入/坐标输出格式、定位评测指标时。
