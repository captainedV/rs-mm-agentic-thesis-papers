# 已锁定的研究主张

> 本文件只记录开题已锁定的主张，不新增主张。目录与写作都必须回到这里对齐；检索入口见 [`SKILL.md`](SKILL.md)，路由见 [`INDEX.md`](INDEX.md)。

## 题目

**面向灾害应急的多源遥感可靠工具规划与后训练智能体。**

## 主张（原文锁定）

在洪水、地震、野火等灾害应急中，光学常被云、烟、夜间切断，SAR 能补盲但几何与语义都不同。系统的关键增益应来自可检验的工具规划：决定何时切换光学/SAR，切换后如何对齐、裁剪，并正确调用检测、分割、损毁评估工具（含参数与中间结果校验）；再在轨迹级后训练中降低「步骤看似正确、最终答案却错误」的情况。不靠再训练一个更强的灾害视觉语言模型来消化这些错误。

## 主张拆解（只用于检验，不改写主张）

| 编号 | 可检验子命题 | 需要的证据 | 现有文献能到哪 |
| --- | --- | --- | --- |
| P1a | 灾害场景中，光学/SAR 的切换决策应显式建模并可检验 | 切换动作、触发条件、切换后的对齐/裁剪、失败案例 | EO-Gym 把光学–SAR 切换写成一等动作；Earth-Agent 把光谱/产品纳入工具生态；但专门评估“切换策略”的工作仍薄 |
| P1b | 工具调用的主要瓶颈不只是“选对工具”，还包括参数与中间结果接地 | 工具/参数/步骤级指标，与最终答案分开报告 | Earth-Agent、ThinkGeo、DORA、Univearth 均报告了步骤/执行与最终答案的分离或参数接地问题 |
| P1c | 灾害端到端作业需要感知之外的空间关系、路网/人口/疏散/报告 | 多维度任务、黄金轨迹、长程组合评测 | DORA 覆盖五维灾害流水线；RescueADI 覆盖灾害任务规划；但 SAR 子集与真实部署仍不足 |
| P2 | 轨迹级后训练可以降低“步骤看似正确、最终答案却错误” | 轨迹监督/蒸馏/RL；步骤正确与答案正确的联合指标 | SimCRAFT、OpenEarthAgent、VICoT-Agent、WeaveAgent、HiRS-Agent 等提供方法参照；**本目录 61 篇中，尚无一篇在灾害多传感器任务上直接报告该联合指标的改善** |

## 文献支撑矩阵

| 主张环节 | 最强证据（先读） | 辅助证据 | 只能说明 | 不能说明 |
| --- | --- | --- | --- | --- |
| 灾害端到端与长程脆弱性 | [`dora`](papers/dora.md)、[`thinkgeo`](papers/thinkgeo.md) | [`eo-gym`](papers/eo-gym.md)、[`rescueadi`](papers/rescueadi.md) | 现有 agent 在灾害五维任务/长程轨迹上仍与黄金轨迹有明显差距 | 某个规划算法普遍更优；真实应急已可用 |
| 工具生态与轨迹/答案双层评测 | [`earth-agent`](papers/earth-agent.md) | [`openearthagent-shabbir`](papers/openearthagent-shabbir.md)、[`openearth-agent-zhao`](papers/openearth-agent-zhao.md) | 工具注册、参数/轨迹正确性与最终定量答案必须分开评 | SAR 切换策略已被解决 |
| 光学–SAR 交互式取证 | [`eo-gym`](papers/eo-gym.md) | [`earthdial`](papers/earthdial.md)、[`fusar-gpt`](papers/fusar-gpt.md)、[`fusar-klip`](papers/fusar-klip.md) | 环境层面可把切换当动作；感知层面 SAR 可补盲 | 感知支持 SAR = 会规划切换/对齐/裁剪 |
| 工具选择与上下文负载 | [`rs-claw`](papers/rs-claw.md)、[`hirs-agent`](papers/hirs-agent.md) | [`earth-agent`](papers/earth-agent.md)、[`rs-agent`](papers/rs-agent.md) | 全量注册/RAG 都难以兼顾上下文与工具完整性 | 层级探索一定优于强规划模型 |
| 代码/GEE 工具接地 | [`univearth`](papers/univearth.md) | [`geoagent-chen`](papers/geoagent-chen.md) | 代码执行失败与答案错误是分离的；reflexion 只能部分缓解 | 代码 agent 可直接迁移到灾害多工具流水线 |
| 轨迹合成与蒸馏 | [`simcraft`](papers/simcraft.md)、[`vicot-agent`](papers/vicot-agent.md) | [`openearthagent-shabbir`](papers/openearthagent-shabbir.md) | 可把编排能力迁移到 7B/小模型；执行校验可提升轨迹可执行性 | 合成轨迹=真实执行；已降低步骤–答案不一致 |
| 路由/过程奖励/RL | [`weaveagent`](papers/weaveagent.md)、[`rs-claw-evolution`](papers/rs-claw-evolution.md) | [`socrates`](papers/socrates.md)、[`geocot`](papers/geocot.md) | 路由与工具使用可以被训练；过程奖励可改善推理行为 | 在灾害多传感器任务上已通用有效 |
| 多 agent 分工 | [`geollm-squad`](papers/geollm-squad.md)、[`geommagent`](papers/geommagent.md) | [`hirs-agent`](papers/hirs-agent.md) | 编排与求解分离、Manager/Specialist 分层可扩展复杂任务 | 增益全部来自分工而非额外调用/算力 |
| 感知底座/对照 | [`earthdial`](papers/earthdial.md)、[`teochat`](papers/teochat.md)、[`terrascope`](papers/terrascope.md) | [`earthgpt`](papers/earthgpt.md)、[`ringmo-agent`](papers/ringmo-agent.md)、[`skysense`](papers/skysense.md) | 视觉前端能力、SAR/多光谱支持、强对照基线 | 可以替代模态–工具规划方法 |
| 静态评测协议 | [`vrsbench`](papers/vrsbench.md)、[`geobench-vlm`](papers/geobench-vlm.md) | [`choice`](papers/choice.md)、[`lrs-vqa`](papers/lrs-vqa.md)、[`earthvqa`](papers/earthvqa.md) | 感知/推理/定位仍有系统性不足 | 静态分数可代表 agent 的轨迹能力 |

## 各类文献能支撑什么、不能支撑什么

### 灾害应急与可执行评测（DORA、ThinkGeo、EO-Gym、DisasterM3、RescueADI）

**能支撑**：

- 灾害响应不是单一损毁评估，而是感知、空间关系、行动规划、时序演化与报告的综合流水线（DORA）。
- 工具执行指标与最终答案会分离；SAR 子集的最终答案尤其弱（ThinkGeo）。
- 交互式环境可以把区域扩展、历史观测、光学–SAR 切换作为动作（EO-Gym）。
- 灾害任务级 planning/perception/recognition 可以标注并监督（RescueADI）。

**不能支撑**：

- 这些基准的分数不能互相横排；DORA 的 56% 长程差距不是所有 agent 的普遍上限。
- 离线可回放环境不等于真实应急部署。
- DisasterM3 是静态指令数据，不能当作工具轨迹评测。

### 工具规划、MCP 与遥感智能体（Earth-Agent、RS-Agent、Change-Agent、OpenEarthAgent、OpenEarth-Agent、RS-Claw、HiRS-Agent）

**能支撑**：

- 工具注册/选择/参数接地是独立于“感知能力”的工程与科学问题（Earth-Agent、ThinkGeo）。
- 工具可以从“调用预定义”推进到“按需创造”（OpenEarth-Agent）。
- 工具空间探索、层级 Skill、Manager/Specialist 分层可以缓解长程上下文与错误传播（RS-Claw、HiRS-Agent）。
- 早期系统（RS-ChatGPT、Change-Agent）已经把 LLM 作为调度器接视觉工具，但规划较浅。

**不能支撑**：

- “支持 SAR/多光谱输入”不等于“会决定何时切换、如何对齐裁剪”。
- 工具数量多不等于规划强；工具创造也未被证明普遍优于工具调用。
- 这些工作多在自建/少量基准上评测，不能拼成跨协议排名。

### 后训练、轨迹蒸馏与多智能体分工（SimCRAFT、VICoT-Agent、GeoMMAgent、GeoLLM-Squad、WeaveAgent、RS-Claw-Evolution、Socrates、GeoCoT）

**能支撑**：

- 轨迹可以被合成、校验、蒸馏或用于 SFT/RL（SimCRAFT、VICoT-Agent、OpenEarthAgent）。
- 路由/工具使用可以被训练，且可分阶段归因（WeaveAgent）。
- 过程奖励、证据寻求与分层 RL 可以改善推理/协作行为（Socrates、GeoCoT、HiRS-Agent）。
- 多 agent 分工可以扩展任务复杂度（GeoLLM-Squad、GeoMMAgent）。

**不能支撑**：

- 没有一篇在灾害多传感器任务上直接报告“步骤正确率上升、最终答案错误率下降”的联合指标。
- 合成轨迹的可执行性校验不等于真实执行正确。
- 多 agent 的增益可能来自额外调用/算力，不能全部归因于分工或后训练。

### 感知底座与多源 VLM（EarthDial、TEOChat、FUSAR-GPT、FUSAR-KLIP、EarthGPT、RingMo-Agent、TerraScope、SkySense、RemoteCLIP 等）

**能支撑**：

- 光学/SAR/多光谱/时序的视觉前端能力与强对照基线。
- 多传感器对话、像素接地、时序变化与 SAR 专用表示。
- “通用 VLM 在 RS 上不够”的感知层证据。

**不能支撑**：

- 不能替代模态–工具规划方法；不能把“支持 SAR”写成“会切换/校验”。
- 不能把感知分数当作工具调用可靠性。
- 不能把模型名里的 “Agent” 当作通用 agent 能力。

### 静态/单轮基准（VRSBench、GEOBench-VLM、CHOICE、LRS-VQA、EarthVQA、RSVQA）

**能支撑**：

- 感知、定位、计数、关系推理、超大图理解等能力诊断。
- 作为 agent 感知前端的对照基线。

**不能支撑**：

- 工具调用、轨迹规划、参数接地或灾害端到端能力。
- 与轨迹级 benchmark 的分数横排。

### 综述、系统与基础设施（Talemi 综述、Space-Air-Ground、Risk-Aware）

**能支撑**：

- Agentic RS 的 taxonomy、单/多 agent 区分、规划/RAG/记忆等架构轴（Talemi 综述）。
- 空天地系统的数据治理、组件化解译与应用 agent 的系统背景（Space-Air-Ground）。
- 云目录检索中的意图解析、schema 感知 API 生成与安全护栏（Risk-Aware）。

**不能支撑**：

- 具体规划算法或后训练目标的实验增益。
- 生产级安全/可靠性；Risk-Aware 只有初步对抗评测。
- 把系统愿景写成已实现的灾害端到端能力。

## 证据缺口（写作时应主动承认）

1. **SAR 上的 tool-augmented 评测很薄**：ThinkGeo 仅 50 条 SAR 任务；DORA/EO-Gym 虽有 SAR，但专门分析“切换策略”的实验不足。
2. **长程灾害流水线的组合脆弱性**：DORA 显示差距随轨迹变长从 7% 到 56%，但还没有方法在该设置上系统验证改进。
3. **参数/中间结果接地的细粒度诊断**：Earth-Agent/ThinkGeo 报 step 指标，但工具参数错误、裁剪错误、对齐错误的分型仍不统一。
4. **P2 的联合指标缺失**：多数后训练论文只报最终任务分数，未分别报“步骤正确/答案正确”的混淆矩阵。
5. **跨协议不可比**：工具集、动作空间、是否给黄金提示、光学/光谱设置差异很大，不能做 SOTA 榜。
6. **真实部署与安全**：离线 benchmark、合成轨迹、生成工具的安全/复现性都未在真实应急中验证。

## 写作边界（不要写进正文的“过度主张”）

- 不要写“我们提出了一个更强的灾害 VLM”；主张明确不靠再训更强 VLM 来消化错误。
- 不要写“某基准证明我们的 agent 达到 SOTA”；跨协议不可比，且多数工作是预印本。
- 不要写“感知底座可以替代工具规划”；EarthDial/TEOChat/FUSAR-GPT 等只能做前端/对照。
- 不要写“多 agent 一定优于单 agent”；现有证据只说明在特定任务/设置下可扩展。
- 不要写“轨迹蒸馏已经解决步骤–答案不一致”；目前最多是方法参照，缺灾害场景的联合指标。
- 不要写“OpenEarthAgent 已被 ECCV 录用”或“ThinkGeo 是 ICLR/CVPR 主会论文”；按预印本处理。

## 与章节的对应

| 章节 | 先读 | 用途 |
| --- | --- | --- |
| 引言/动机 | `CLAIM.md` + [`dora`](papers/dora.md)、[`thinkgeo`](papers/thinkgeo.md)、[`eo-gym`](papers/eo-gym.md) | 灾害多源、模态切换、长程失败的业务动机 |
| 相关工作 | [`talemi-survey`](papers/talemi-survey.md) + 三个 cluster | 领域地图与分类，不堆论文 |
| 方法-P1 | [`earth-agent`](papers/earth-agent.md)、[`openearth-agent-zhao`](papers/openearth-agent-zhao.md)、[`rs-claw`](papers/rs-claw.md) | 工具生态、选择/创造、参数校验 |
| 方法-P2 | [`simcraft`](papers/simcraft.md)、[`weaveagent`](papers/weaveagent.md)、[`hirs-agent`](papers/hirs-agent.md) | 轨迹监督、路由训练、过程奖励 |
| 实验设计 | [`dora`](papers/dora.md)、[`thinkgeo`](papers/thinkgeo.md)、[`eo-gym`](papers/eo-gym.md) | 轨迹/最终答案双层指标、长程与 SAR 子集 |
| 讨论/局限 | 本文件“证据缺口” | 主动承认 SAR 评测薄、联合指标缺失、跨协议不可比 |
