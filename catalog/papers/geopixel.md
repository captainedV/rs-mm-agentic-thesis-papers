# GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing

> 论文卡片 · `geopixel` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing |
| 作者 | Akashah Shabbir; Mohammed Zumri; Mohammed Bennamoun; Fahad S. Khan; Salman Khan |
| 年份 | 2025 |
| 会址 / 状态 | ICML 2025 |
| arXiv | [arXiv:2501.13925](https://arxiv.org/abs/2501.13925) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://proceedings.mlr.press/v267/shabbir25a.html) |
| Bib key | `geopixel`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2025-ICML-GeoPixel-Shabbir.pdf`](../../pdfs/2025-ICML-GeoPixel-Shabbir.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | pixel-level grounding |
| PDF 版本 | arXiv 版本（PMLR 正式 PDF 未下载） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

首个端到端高分辨率 RS 像素级 grounding LMM：在对话中生成交错掩膜，支持最高 4K HD 分辨率与像素级视觉感知。

## 核心结论

- GeoPixel 把 pixel-level grounding 引入 RS LMM，让模型在对话中输出掩膜而不是只给文本。 [摘要]
- 它针对 RS 的俯视视角、尺度变化和小目标问题，支持高分辨率输入（最高 4K HD）。 [摘要]
- 像素级掩膜为裁剪/对齐/损毁评估提供了更细的视觉接口，但模型本身仍是感知前端。 [摘要]
- 论文的贡献是 grounding 能力与数据，不是工具选择或长程规划。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把“能输出掩膜”写成“能规划分割工具的调用与参数”。没有灾害多工具实验。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`lisat`](lisat.md) — LISAT: Language-Instructed Segmentation Assistant for Satellite Imagery
- [`terrascope`](terrascope.md) — TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

## 何时必须打开全文

需要高分辨率编码方式、掩膜生成协议、grounding 数据规模与评测指标时。
