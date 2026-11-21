# SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts

> 论文卡片 · `skymoe` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts |
| 作者 | Jiaqi Liu; Ronghao Fu; Lang Sun; Haoran Liu; Xiao Yang; Weipeng Zhang; Xu Na; Zhuoran Duan; Bo Yang |
| 年份 | 2026 |
| 会址 / 状态 | AAAI（OJS 37653）；届次以期刊页为准 |
| arXiv | [arXiv:2512.02517](https://arxiv.org/abs/2512.02517) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://ojs.aaai.org/index.php/AAAI/article/view/37653) |
| Bib key | `skymoe`（**尚未写入开题 `.bib`**） |
| 仓库内 PDF | [`pdfs/2026-arXiv-SkyMoE-Liu.pdf`](../../pdfs/2026-arXiv-SkyMoE-Liu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | geospatial interpretation |
| PDF 版本 | arXiv 版本（非 AAAI 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |
| 引用注意 | 会址按 AAAI OJS 37653 记录，具体届次未独立核对；打包 PDF 是 arXiv 预印本，不得升格为确定主会届次或出版社正式版。 |

## 问题与方法

面向多模态、多任务 RS 解译的 MoE 视觉–语言模型：自适应路由器生成任务/粒度感知的路由指令，让不同 LLM 专家处理不同子任务，并用上下文解耦增强专家分工。

## 核心结论

- SkyMoE 针对“统一建模难以区分任务类型与解译粒度”的问题，用任务/粒度感知路由。 [摘要]
- 不同 LLM 专家处理不同子任务，以兼顾局部细节与全局上下文。 [摘要]
- 上下文解耦增强用于促进专家分工与粒度敏感性。 [摘要]
- 它是感知/解译模型，不是工具调用 agent。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

会址按 AAAI OJS 37653 记录，届次未独立核对，不得升格为确定的主会届次。不能支撑 P1/P2。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`rs-moe`](rs-moe.md) — RS-MoE: Mixture of Experts for Remote Sensing Image Captioning and Visual Question Answering
- [`geocot`](geocot.md) — GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective
- [`falcon`](falcon.md) — Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report)
- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain

## 何时必须打开全文

需要路由指令格式、专家数量、上下文解耦策略、各任务结果时。
