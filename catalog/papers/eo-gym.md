# EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents

> 论文卡片 · `eo-gym` · 主题簇 [灾害应急与可执行评测](../clusters/disaster-emergency.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents |
| 作者 | Sai Ma; Zhuang Li; Sichao Li; Xinyue Xu; Ruibiao Zhu; Tony Boston; John A. Taylor |
| 年份 | 2026 |
| 会址 / 状态 | 预印本（arXiv:2605.01250）；会址待确认 |
| arXiv | [arXiv:2605.01250](https://arxiv.org/abs/2605.01250) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://arxiv.org/abs/2605.01250) |
| Bib key | `eo-gym`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-arXiv-EO-Gym-Ma.pdf`](../../pdfs/2026-arXiv-EO-Gym-Ma.pdf) |
| 代码 / 项目 | 无记录 |
| 数据集 | EO-Gym-Data |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

把 EO 分析建成 Gymnasium 风格的本地可执行工作空间：按位置、时间、传感器索引 66 万多模态文件，提供 35 个 EO 工具，支持平移/缩放、历史观测拉取和光学–SAR 切换。

## 核心结论

- EO-Gym 把“交互式取证”写成一等公民：agent 可扩大区域、拉历史观测、在光学与 SAR 之间切换，而不是做固定输入单轮问答。 [摘要]
- 环境含超过 66 万多模态文件、35 个 EO 工具、六类任务族。 [摘要]
- EO-Gym-Data 含 9,078 条轨迹、34,604 个推理步，基于 8 个公开 EO 数据集与 Landsat/Sentinel-2 影像。 [摘要]
- 10 个开源/闭源 VLM 在时序与跨模态工作流上仍明显吃力；4B 基线经数据微调后 Pass@3 从 0.49 提到 0.74（主设置）。 [摘要]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 660k+ | 多模态文件数 | 摘要 | 已核摘要 |
| 35 | EO 专用工具数 | 摘要 | 已核摘要 |
| 9,078 / 34,604 | 轨迹数 / 推理步数 | 摘要 | 已核摘要 |
| 0.49 → 0.74 | EO-Gym-4B 主设置 Pass@3 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

这是环境 + 数据 + 基线论文，不能把 0.49→0.74 当作某种通用后训练算法的增益；Pass@3 是特定主设置，不能与其他基准横比。预印本，会址未确认；Hugging Face 账户名异常，数据镜像需再核。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks
- [`earth-agent`](earth-agent.md) — Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents
- [`openearthagent-shabbir`](openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents

## 何时必须打开全文

需要动作空间、工具参数、轨迹评分、主设置定义、跨模态子集结果，或要把“光学–SAR 切换”写进实验设计时。
