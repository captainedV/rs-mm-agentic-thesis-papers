# SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery

> 论文卡片 · `skysense` · 主题簇 [感知底座与多源视觉语言模型](../clusters/perception-foundation.md) · 关系 **仅作感知底座或对照**

| 字段 | 值 |
| --- | --- |
| 标题 | SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery |
| 作者 | Xin Guo; Jiangwei Lao; Bo Dang; Yingying Zhang; Lei Yu; Lixiang Ru; Liheng Zhong; Ziyuan Huang; Kang Wu; Dingxiang Hu; Huimei He; Jian Wang; Jingdong Chen; Ming Yang; Yongjun Zhang; Yansheng Li |
| 年份 | 2024 |
| 会址 / 状态 | CVPR 2024 |
| arXiv | [arXiv:2312.10115](https://arxiv.org/abs/2312.10115) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2312.10115) |
| Bib key | `skysense`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2024-CVPR-SkySense-Guo.pdf`](../../pdfs/2024-CVPR-SkySense-Guo.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | multi-modal EO imagery |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

十亿参数级多模态 RS 基础模型：在 2150 万时序序列上预训练，用因子化多模态时空编码器处理光学与 SAR 时序，并用多粒度对比学习与地理上下文增强表示。

## 核心结论

- SkySense 的核心是多模态时空编码：同时处理光学与 SAR 的时序序列，而不是单幅单模态。 [摘要]
- 预训练数据含 2150 万时序序列，规模远大于多数 RS VLM 的图文数据。 [摘要]
- 多粒度对比学习让表示在不同模态与空间粒度上对齐，地理上下文进一步增强表示。 [摘要]
- 它是视觉基础模型，不提供对话、工具调用或 agent 轨迹。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 21.5M | 预训练时序序列数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能支撑 P1/P2；不能把“光学+SAR 时序编码”写成“会规划模态切换”。没有灾害响应闭环。

## 与主张的关系

**仅作感知底座或对照**。这篇提供视觉前端、感知能力或对照基线，不能替代模态–工具规划方法；只能用于说明感知层能力或作为对比。

## 相关论文

- [`remoteclip`](remoteclip.md) — RemoteCLIP: A Vision Language Foundation Model for Remote Sensing
- [`ringmo-agent`](ringmo-agent.md) — RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning
- [`earthgpt`](earthgpt.md) — EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain
- [`fusar-gpt`](fusar-gpt.md) — FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery

## 何时必须打开全文

需要预训练数据构成、时空编码器结构、对比学习目标、下游任务协议时。
