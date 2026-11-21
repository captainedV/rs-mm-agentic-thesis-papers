# Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents

> 论文卡片 · `earth-agent` · 主题簇 [工具规划、MCP 与遥感智能体](../clusters/tool-planning.md) · 关系 **P1 模态–工具规划**

| 字段 | 值 |
| --- | --- |
| 标题 | Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents |
| 作者 | Peilin Feng; Zhutao Lv; Junyan Ye; Xiaolei Wang; Xinjie Huo; Jinhua Yu; Wanghan Xu; Wenlong Zhang; Lei Bai; Conghui He; Weijia Li |
| 年份 | 2026 |
| 会址 / 状态 | ICLR 2026 |
| arXiv | [arXiv:2509.23141](https://arxiv.org/abs/2509.23141) |
| DOI / 正式页 | 仓库未记录 DOI · [正式/开放页](https://proceedings.iclr.cc/paper_files/paper/2026/file/5b4a459db23e6db9be2a128380953d96-Paper-Conference.pdf) |
| Bib key | `earth-agent`（已写入开题 `ref.bib`） |
| 仓库内 PDF | [`pdfs/2026-ICLR-Earth-Agent-Feng.pdf`](../../pdfs/2026-ICLR-Earth-Agent-Feng.pdf) |
| 代码 / 项目 | https://github.com/opendatalab/Earth-Agent |
| 数据集 | Earth-Bench |
| 核对状态 | 已核摘要（PDF 摘要抽取） |

## 问题与方法

把 RGB 与光谱/产品统一进 MCP 工具生态，用 ReAct 做多步定量时空推理，并配套 Earth-Bench 同时评估轨迹与最终答案。工具集按五类工具箱组织，目标是让 agent 在预训练 MLLM 之外调用领域专家模型。

## 核心结论

- Earth-Agent 的核心不是再训一个更强的 EO MLLM，而是把 104 个专家工具/模型通过 MCP 组织成可调用生态，用 ReAct 完成跨模态多步推理。 [正文]
- Earth-Bench 含 248 个专家题、13,729 张图，覆盖 spectrum、products、RGB 三种模态，并采用轨迹与最终结果的双层评测。 [摘要]
- 论文明确区分“工具选对”和“参数/轨迹正确”：工具调用指标高不代表最终定量答案正确，这是 P1 需要直接引用的评测动机。 [正文]
- 它把光谱与产品数据纳入一等公民，而不是只处理 RGB，这一点比早先 RS agent 更接近航天定量遥感业务。 [目录判断]

## 关键数字

| 数字 | 含义 | 来源位置 | 核对 |
| --- | --- | --- | --- |
| 104 | MCP 工具数量 | 正文第 1 节 / 第 3.2 节 | 已核正文检索 |
| 248 | Earth-Bench 专家题数 | 摘要 | 已核摘要 |
| 13,729 | Earth-Bench 图像数 | 摘要 | 已核摘要 |

> 只列摘要/正文中能定位的数字；不把不同协议下的分数拼成对照表。

## 能力边界

不能用来证明 SAR 上的模态切换策略有效；不能把 Earth-Bench 分数与其他 agent 基准横排；它也不是轨迹级后训练方法，不能支撑 P2 的增益归因。

## 与主张的关系

**P1 模态–工具规划**。这篇直接涉及工具选择、参数接地、模态切换或轨迹评测，可作为 P1 的方法/评测证据；引用时必须限定在其任务与协议内。

## 相关论文

- [`thinkgeo`](thinkgeo.md) — ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks
- [`dora`](dora.md) — Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations
- [`openearth-agent-zhao`](openearth-agent-zhao.md) — OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation
- [`openearthagent-shabbir`](openearthagent-shabbir.md) — OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents

## 何时必须打开全文

需要具体工具清单、每个工具的参数 schema、Earth-Bench 的评分细则、按模态/工具类别的分层结果，或要引用某条具体实验数字时。
