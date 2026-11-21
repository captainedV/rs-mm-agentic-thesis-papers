# RemoteCLIP: A Vision Language Foundation Model for Remote Sensing

> 论文卡片 · `remoteclip` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | RemoteCLIP: A Vision Language Foundation Model for Remote Sensing |
| 作者 | Fan Liu; Delong Chen; Zhangqingyun Guan; Xiaocong Zhou; Jiale Zhu; Qiaolin Ye; Liyong Fu; Jun Zhou |
| 年份 | 2024 |
| 会址 / 状态 | IEEE TGRS 2024 |
| arXiv | [arXiv:2306.11029](https://arxiv.org/abs/2306.11029) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2306.11029) |
| Bib key | `remoteclip`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-TGRS-RemoteCLIP-Liu.pdf`](../../pdfs/2024-TGRS-RemoteCLIP-Liu.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | RemoteCLIP pretraining / RemoteCount |
| PDF 版本 | arXiv 版本（非 IEEE TGRS 出版社正式版） |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

首个 RS 视觉–语言基础模型：用 Box-to-Caption 等方式把异构标注转成统一图文对，学习可迁移的视觉表示与对齐文本嵌入，服务检索与零样本任务。

## 核心结论

- RemoteCLIP 指出既有 RS 自监督/MIM 基础模型偏底层特征，缺语言理解，难以做检索与零样本。 [摘要]
- 它通过数据缩放把异构标注转成统一 image-caption 格式，缓解 RS 图文数据稀缺。 [摘要]
- 模型提供对齐的视觉–文本嵌入，是开放词汇检索与下游微调的底座。 [摘要]
- 它是表示学习模型，不是对话/工具 agent。 [目录判断]

## 关键数字

- 本卡片暂不列关键数字：未在摘要或正文定位到可安全引用的数字。不要从 `papers.json` 的转述里抄数。

## 能力边界

不能支撑 P1/P2；不能把检索/零样本能力当作工具选择能力。无灾害或轨迹评测。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`skysense`](skysense.md) — SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery
- [`geochat`](geochat.md) — GeoChat: Grounded Large Vision-Language Model for Remote Sensing
- [`fusar-klip`](fusar-klip.md) — FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing
- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain

## 何时必须打开全文

需要预训练数据构造、Box-to-Caption 规则、检索/零样本评测协议时。
