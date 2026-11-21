# RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning

> 论文卡片 · `ringmo-agent` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning |
| 作者 | Huiyang Hu; Peijin Wang; Yingchao Feng; Kaiwen Wei; Wenxin Yin; Wenhui Diao; Mengyu Wang; Hanbo Bi; Kaiyue Kang; Tong Ling; Kun Fu; Xian Sun |
| 年份 | 2026 |
| 会址 / 状态 | IEEE TPAMI（DOI: 10.1109/tpami.2026.3718699；卷期页以 Xplore 为准） |
| arXiv | [arXiv:2507.20776](https://arxiv.org/abs/2507.20776) |
| DOI / 正式页 | [10.1109/tpami.2026.3718699](https://doi.org/10.1109/tpami.2026.3718699) · [正式/开放页](https://arxiv.org/abs/2507.20776) |
| Bib key | `ringmo-agent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-TPAMI-RingMo-Agent-Hu.pdf`](../../pdfs/2026-TPAMI-RingMo-Agent-Hu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RS-VL3M, CityNav |
| PDF 版本 | arXiv 版本（非 IEEE TPAMI 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 会址为 IEEE TPAMI DOI 记录，卷期页以 Xplore 为准；本包使用 arXiv。 |

## 问题与方法

多平台、多模态 RS 基础模型：RS-VL3M 含 300 万+ 图文对，覆盖光学/SAR/红外、卫星与无人机、8 类任务；模型支持指令驱动的感知与推理，并含外部视觉定位工具与 RL 轨迹解码。

## 核心结论

- RingMo-Agent 的数据覆盖面是其主要贡献：3 个模态、2 个平台、8 类任务的 300 万+ 图文对。 [摘要]
- 它不只做分类/字幕，还覆盖空间推理与具身导航类任务，处于 VLM 与 agent 之间。 [摘要]
- 模型包含外部视觉定位工具与 RL 优化的轨迹解码，因此比纯 VLM 多了一点“工具/轨迹”成分。 [papers.json 摘要要点；未核正文]
- 但它没有 MCP 式工具注册、参数校验与灾害多工具流水线，不能当作通用工具规划方法。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 3M+ | RS-VL3M 图文对数 | 摘要 | 已核摘要 |
| 3 / 2 / 8 | 模态数 / 平台数 / 任务数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能写成“RingMo-Agent 是灾害工具规划 agent”；其工具使用范围窄，主要是视觉定位/导航。不能把 RS-VL3M 的规模当作 agent 轨迹监督规模。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`earthdial`](earthdial.md) — EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues
- [`teochat`](teochat.md) — TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data
- [`terrascope`](terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 RS-VL3M 的模态/平台/任务配比、外部工具接口、RL 轨迹解码细节时。
