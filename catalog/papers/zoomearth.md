# ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks

> 论文卡片 · `zoomearth` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks |
| 作者 | Ruixun Liu; Bowen Fu; Jiayi Song; Kaiyu Li; Wanchen Li; Lanxuan Xue; Hui Qiao; Weizhan Zhang; Deyu Meng; Xiangyong Cao |
| 年份 | 2026 |
| 会址 / 状态 | CVPR 2026 |
| arXiv | [arXiv:2511.12267](https://arxiv.org/abs/2511.12267) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_ZoomEarth_Active_Perception_for_Ultra-High-Resolution_Geospatial_Vision-Language_Tasks_CVPR_2026_paper.pdf) |
| Bib key | `zoomearth`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-CVPR-ZoomEarth-Liu.pdf`](../../pdfs/2026-CVPR-ZoomEarth-Liu.pdf) |
| 代码 / 项目 | https://github.com/earth-insights/ZoomEarth |
| 数据集 | ultra-high-resolution geospatial VL |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

超高分辨率地学 VL 的主动感知框架：在推理中自适应裁剪–缩放，回到信息密集区域；配套 LRS-GRO（17 类问题，全局/区域/目标三级），训练为 SFT + GRPO。

## 核心结论

- ZoomEarth 把“被动看整图”改成“主动回看信息密集区域”，用裁剪–缩放作为感知动作。 [摘要]
- LRS-GRO 覆盖 17 类问题、全局/区域/目标三个层级，专门评测主动感知。 [摘要]
- 模型用 Region-Guided reward 做 SFT + GRPO，在 LRS-GRO 与三个公开 UHR 基准的零样本设置上报告 SOTA。 [摘要]
- 它还能通过简单工具接口接入去云、去噪、分割、编辑等下游模型，但核心仍是感知策略而非多工具规划。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 17 | LRS-GRO 问题类型数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能把“裁剪–缩放”直接等同于“模态–工具规划”；没有光学–SAR 切换、检测/分割工具的参数校验。不能支撑灾害端到端结论。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`lrs-vqa`](lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning
- [`geopixel`](geopixel.md) — GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing
- [`terrascope`](terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要 LRS-GRO 的 17 类问题、Region-Guided reward、裁剪动作空间、与下游工具的接口时。
