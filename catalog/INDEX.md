# 文献目录分层总目

> 入口：[`SKILL.md`](SKILL.md) · 主张：[`CLAIM.md`](CLAIM.md) · 机器索引：[`index.json`](index.json) · 官方条目 **61 篇**，PDF **59 篇**。

本页只做“跳到哪张卡”的路由，不替代 `CLAIM.md` 的主张边界，也不替代论文卡片里的来源核对。**不要从本页直接抄结论或数字。**

## 0. 先选路径

| 你现在要写的是 | 先走哪条路径 | 典型产出 |
| --- | --- | --- |
| 研究主张、贡献点、P1/P2 关系 | [主张路径](#1-主张路径) | `CLAIM.md` + 2–4 张核心卡 |
| 一个具体问题（灾害、SAR、工具选择、步骤–答案不一致） | [问题路径](#2-问题路径) | 1 个 cluster + 2–3 张卡 |
| 一个方法族（MCP、多 agent、蒸馏、RL、主动感知） | [方法路径](#3-方法路径) | 方法对比 + 能力边界 |
| 一个基准或实验协议 | [基准路径](#4-基准路径) | 协议差异 + 可/不可比较的结论 |
| 找某篇论文 | [全目录](#5-全目录61-篇) 或 [`index.json`](index.json) | 卡片 |

## 1. 主张路径

### P1 模态–工具规划

要回答：何时切换光学/SAR、切换后如何对齐/裁剪、如何调用检测/分割/损毁评估工具并校验参数与中间结果。

| 卡片 | 它能支撑的主张环节 | 不能支撑什么 |
| --- | --- | --- |
| [`earth-agent`](papers/earth-agent.md) | 工具生态 + 轨迹/最终答案双层评测；“工具选对 ≠ 参数/轨迹对” | SAR 切换策略、后训练增益 |
| [`openearth-agent-zhao`](papers/openearth-agent-zhao.md) | 从工具调用到工具创造；开放环境长尾覆盖 | 工具创造已普遍优于工具调用 |
| [`thinkgeo`](papers/thinkgeo.md) | 逐步执行指标与最终答案的分离；SAR 子集暴露跨模态困难 | 与 DORA/Earth-Bench 横排分数 |
| [`dora`](papers/dora.md) | 灾害端到端五维任务；长程轨迹组合脆弱性 | 某个规划算法的普遍有效性 |
| [`eo-gym`](papers/eo-gym.md) | 交互式取证；光学–SAR 切换作为一等动作 | 0.49→0.74 是通用后训练算法增益 |
| [`rescueadi`](papers/rescueadi.md) | 灾害任务级 planning/perception/recognition 标注 | SAR 切换或 MCP 工具生态 |
| [`change-agent`](papers/change-agent.md) | 早期“感知模型 + LLM + Python 工具”的可执行变化分析 | 通用灾害多工具流水线 |
| [`rs-agent`](papers/rs-agent.md) | 任务感知检索 + 双路 RAG + 光学/SAR 输入 | “支持 SAR”= 已解决 SAR 规划 |
| [`geommagent`](papers/geommagent.md) | 检索–感知–推理多 agent 分工；36 模型系统性不足 | 轨迹级后训练 |
| [`geollm-squad`](papers/geollm-squad.md) | 编排与任务求解解耦；+17% agentic correctness | 灾害场景泛化 |
| [`geo-olm`](papers/geo-olm.md) | 状态驱动工作流；小模型成本/完成率 | 灾害精度或 SAR 可靠性 |
| [`univearth`](papers/univearth.md) | GEE 代码取证；执行失败率与 reflexion 上限 | 多传感器工具规划 |
| [`rs-claw`](papers/rs-claw.md) | 工具空间主动探索；上下文负载 vs 工具完整性 | 层级 Skill 树普遍优于强规划器 |
| [`geoagent-chen`](papers/geoagent-chen.md) | 代码解释器 + 静态分析 + RAG + MCTS 的多步地理空间编程 | 卫星影像工具规划/灾害流水线 |
| [`expertsrs`](papers/expertsrs.md) | Data–Tools–Brain 多 agent 处理非专家查询（仅元数据） | 任何具体方法/数字；缺全文，未核正文 |

### P2 轨迹级后训练

要回答：如何用轨迹监督/蒸馏/RL 降低“步骤看似正确、最终答案却错误”，而不是再训一个更强的灾害 VLM。

| 卡片 | 它能支撑的主张环节 | 不能支撑什么 |
| --- | --- | --- |
| [`simcraft`](papers/simcraft.md) | 合成轨迹 + 执行校验 + 检索增强蒸馏到 7B | 合成轨迹=真实执行；已降低步骤–答案不一致 |
| [`openearthagent-shabbir`](papers/openearthagent-shabbir.md) | 轨迹 SFT + 确定性回放校验；光学/SAR/GIS/指数工具 | ECCV 录用；跨灾害泛化 |
| [`vicot-agent`](papers/vicot-agent.md) | 视觉交错 CoT + Reasoning Stack 蒸馏 | 统一 SOTA 分数；外部工具规划 |
| [`rs-claw-evolution`](papers/rs-claw-evolution.md) | 失败感知轨迹 + 错误轮掩码 + 分层 RL | 已解决最终答案错误 |
| [`weaveagent`](papers/weaveagent.md) | 路由 SFT + GRPO；分阶段归因 | 多传感器灾害流水线；0.965 是部署精度 |
| [`hirs-agent`](papers/hirs-agent.md) | Manager/Specialist 分层 + 步级验证 + 分层 RL | ACM MM 录用；灾害泛化 |
| [`socrates`](papers/socrates.md) | 证据寻求轨迹合成 + 两阶段 RL，针对伪推理 | 外部工具调用；联合步骤/答案指标 |
| [`geocot`](papers/geocot.md) | RSV-GRPO + RS-CoT-20k；模型内 CoT | 工具轨迹；步骤–答案不一致 |

## 2. 问题路径

| 写作问题 | 先读 cluster | 再读卡片 | 不要用来证明 |
| --- | --- | --- | --- |
| 灾害端到端作业/应急响应 | [`disaster-emergency`](clusters/disaster-emergency.md) | [`dora`](papers/dora.md), [`thinkgeo`](papers/thinkgeo.md), [`eo-gym`](papers/eo-gym.md) | 感知 VLM 已能替代应急规划 |
| 光学被云/烟/夜切断，需要 SAR 补盲 | [`perception-foundation`](clusters/perception-foundation.md) | [`earthdial`](papers/earthdial.md), [`fusar-gpt`](papers/fusar-gpt.md), [`fusar-klip`](papers/fusar-klip.md), [`ringmo-agent`](papers/ringmo-agent.md), [`earthgpt`](papers/earthgpt.md), [`teochat`](papers/teochat.md) | “支持 SAR”= 已验证切换策略 |
| 工具太多、上下文放不下，怎么选工具 | [`tool-planning`](clusters/tool-planning.md) | [`rs-claw`](papers/rs-claw.md), [`earth-agent`](papers/earth-agent.md), [`openearth-agent-zhao`](papers/openearth-agent-zhao.md), [`hirs-agent`](papers/hirs-agent.md) | 工具数量=规划能力 |
| 工具选对但参数/中间结果错 | [`tool-planning`](clusters/tool-planning.md) | [`earth-agent`](papers/earth-agent.md), [`dora`](papers/dora.md), [`thinkgeo`](papers/thinkgeo.md), [`univearth`](papers/univearth.md) | 最终答案分数能诊断参数错误 |
| 步骤看似正确、最终答案错 | [`post-training`](clusters/post-training.md) | [`simcraft`](papers/simcraft.md), [`weaveagent`](papers/weaveagent.md), [`hirs-agent`](papers/hirs-agent.md), [`rs-claw-evolution`](papers/rs-claw-evolution.md) | 只报最终分数的论文已解决该问题 |
| 多 agent 分工是否值得 | [`post-training`](clusters/post-training.md) | [`geommagent`](papers/geommagent.md), [`geollm-squad`](papers/geollm-squad.md), [`hirs-agent`](papers/hirs-agent.md) | 多 agent 增益全部来自分工 |
| 从调用工具到创造工具 | [`tool-planning`](clusters/tool-planning.md) | [`openearth-agent-zhao`](papers/openearth-agent-zhao.md), [`rs-claw`](papers/rs-claw.md), [`rs-claw-evolution`](papers/rs-claw-evolution.md) | 工具创造已普遍更优 |
| GEE/代码 agent 的可靠性 | [`tool-planning`](clusters/tool-planning.md) | [`univearth`](papers/univearth.md), [`geoagent-chen`](papers/geoagent-chen.md), [`risk-aware`](papers/risk-aware.md) | 代码能跑=答案正确 |
| 感知底座/对比基线选谁 | [`perception-foundation`](clusters/perception-foundation.md) | [`earthdial`](papers/earthdial.md), [`teochat`](papers/teochat.md), [`terrascope`](papers/terrascope.md), [`skysense`](papers/skysense.md), [`remoteclip`](papers/remoteclip.md) | 感知模型可替代工具规划 |
| 静态 VLM 评测协议 | [`static-benchmarks`](clusters/static-benchmarks.md) | [`vrsbench`](papers/vrsbench.md), [`geobench-vlm`](papers/geobench-vlm.md), [`choice`](papers/choice.md), [`lrs-vqa`](papers/lrs-vqa.md), [`earthvqa`](papers/earthvqa.md), [`rsvqa`](papers/rsvqa.md) | 静态分数可与 agent 分数横排 |
| 领域地图/系统背景 | [`survey-infra`](clusters/survey-infra.md) | [`talemi-survey`](papers/talemi-survey.md), [`space-air-ground`](papers/space-air-ground.md), [`risk-aware`](papers/risk-aware.md) | 综述可替代原论文证据 |

## 3. 方法路径

| 方法族 | 代表卡片 | 关键差异 | 主要风险 |
| --- | --- | --- | --- |
| MCP / ReAct 工具生态 | [`earth-agent`](papers/earth-agent.md), [`dora`](papers/dora.md), [`eo-gym`](papers/eo-gym.md) | 工具注册表 + 多步调用 + 轨迹评测 | 工具集/动作空间不同，分数不可横排 |
| 工具创造 | [`openearth-agent-zhao`](papers/openearth-agent-zhao.md) | 数据探测→DAG 规划→生成 Python 工具→校验 | 生成工具的安全性与可复现性未验证 |
| 工具空间主动探索 | [`rs-claw`](papers/rs-claw.md) | Skill 树分层加载，控制上下文 | 预印本；缺灾害/SAR 端到端 |
| 多 agent 分工 | [`geommagent`](papers/geommagent.md), [`geollm-squad`](papers/geollm-squad.md), [`hirs-agent`](papers/hirs-agent.md) | 编排/求解分离，或 Manager/Specialist 分层 | 增益可能来自额外调用/算力 |
| 轨迹合成 + 蒸馏 | [`simcraft`](papers/simcraft.md), [`vicot-agent`](papers/vicot-agent.md) | 合成/蒸馏轨迹到 7B 或小模型 | 合成≠真实执行；跨域迁移未证 |
| 路由训练 + RL | [`weaveagent`](papers/weaveagent.md), [`rs-claw-evolution`](papers/rs-claw-evolution.md) | 先学“是否/调用哪个工具”，再用环境奖励优化 | 奖励设计敏感；长程信用分配难 |
| 推理 RL / 证据寻求 | [`socrates`](papers/socrates.md), [`geocot`](papers/geocot.md) | 模型内 CoT + RL，减少伪推理 | 不是外部工具规划；联合指标缺失 |
| 主动感知/裁剪 | [`zoomearth`](papers/zoomearth.md), [`lrs-vqa`](papers/lrs-vqa.md) | 裁剪–缩放或 token 剪枝 | 视觉动作≠工具规划 |
| 代码/GEE agent | [`univearth`](papers/univearth.md), [`geoagent-chen`](papers/geoagent-chen.md) | 代码解释器 + 静态分析/RAG/MCTS | 执行成功率与答案正确性分离 |
| 像素接地/感知前端 | [`geopixel`](papers/geopixel.md), [`terrascope`](papers/terrascope.md), [`lisat`](papers/lisat.md) | 掩膜/像素推理，提供视觉证据 | 不能替代工具选择与参数校验 |

## 4. 基准路径

**先看协议，再看分数。** 轨迹级与静态基准不可横排；轨迹级之间也因工具集/动作空间/评分不同而不可横排。

| 基准 | 协议 | 规模（仓库记录） | 能回答 | 不能回答 |
| --- | --- | --- | --- | --- |
| Earth-Bench | 轨迹 + 最终答案；Spectrum/Products/RGB | 248 题、13,729 图 | 工具调用与最终定量答案的分离 | SAR 切换策略；其他基准的排名 |
| ThinkGeo | ReAct 工具序列；step + final | 486 任务、1,778 步；RGB 436 / SAR 50 | 逐步执行 vs 最终答案；SAR 子集困难 | 与 DORA/Earth-Bench 横排 |
| DORA | 端到端灾害五维；黄金轨迹可回放 | 515 任务、45 灾害、3,500 步、108 工具 | 长程灾害流水线的组合脆弱性 | 某个规划算法的普遍优越 |
| EO-Gym | Gymnasium 交互；光学–SAR 切换 | 9,078 轨迹、34,604 步、35 工具 | 交互式取证与跨模态工作流 | 通用后训练算法增益 |
| OpenEarth-Bench | 开放环境全流程；工具创造 | 596 案例、7 应用域 | 工具创造/开放环境适应 | 与固定工具 agent 的公平排名 |
| UnivEARTH | GEE 代码是/否题 | 408 题、7 主题、15+ 仪器 | 代码执行失败与 reflexion 上限 | 多传感器灾害规划 |
| GeoMMBench | 多学科多传感器多模态 QA | 36 个模型；题量见项目页 | 专家级地学多模态短板 | 工具轨迹能力 |
| VRSBench | 静态字幕/定位/开放 VQA | 29,614 图、52,472 指称、123,221 QA | 感知/定位基线 | 工具调用或轨迹 |
| GEOBench-VLM | 静态地学任务（含时序/分割） | 10,000+ 指令 | 地学专用感知差距 | agent 规划能力 |
| CHOICE | 静态选择题，感知/推理两层 | 10,507 题、50 城市 | 遥感感知/推理分层诊断 | 轨迹级能力 |
| LRS-VQA | 超大图 VQA | 7,333 QA、最长边 27,328 px | 大图感知与 token 效率 | 工具规划 |
| EarthVQA | 关系推理 VQA | 6,000 图、208,593 QA | 对象关系推理 | agent 工具编排 |
| RSVQA | 经典静态 VQA | RSVQA-LR/HR | 领域评测祖先/背景 | 现代 agent 能力 |

## 5. 全目录（61 篇）

按年份倒序、同 year 按标题。`关系` 只表示与 thesis 主张的关系，不表示论文质量。

| id | 年份 | 标题 | 会址 / 状态 | 主题簇 | 关系 |
| --- | --- | --- | --- | --- | --- |
| [`talemi-survey`](papers/talemi-survey.md) | 2026 | Agentic AI in Remote Sensing: Foundations, Taxonomy, and Emerging Systems | WACV 2026 Workshop (GeoCV) | [综述、系统与基础设施](clusters/survey-infra.md) | 背景文献 |
| [`expertsrs`](papers/expertsrs.md) | 2026 | An LLM-based multi-agent system for remote sensing analysis | Big Earth Data | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`socrates`](papers/socrates.md) | 2026 | Asking like Socrates: Socrates helps VLMs understand remote sensing images | CVPR 2026 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`dora`](papers/dora.md) | 2026 | Can LLM Agents Respond to Disasters? Benchmarking Heterogeneous Geospatial Reasoning in Emergency Operations | NeurIPS 2026 | [灾害应急与可执行评测](clusters/disaster-emergency.md) | P1 模态–工具规划 |
| [`earth-agent`](papers/earth-agent.md) | 2026 | Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents | ICLR 2026 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`eo-gym`](papers/eo-gym.md) | 2026 | EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents | 预印本（arXiv:2605.01250）；会址待确认 | [灾害应急与可执行评测](clusters/disaster-emergency.md) | P1 模态–工具规划 |
| [`fusar-gpt`](papers/fusar-gpt.md) | 2026 | FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery | CVPR 2026 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`geocot`](papers/geocot.md) | 2026 | GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective | CVPR 2026 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`geommagent`](papers/geommagent.md) | 2026 | GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing | CVPR 2026 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P1 模态–工具规划 |
| [`hirs-agent`](papers/hirs-agent.md) | 2026 | HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving | 预印本（arXiv:2608.30672）；会址待确认。arXiv 注释写 ACM MM 2026，未与正式论文集交叉核对，不升格 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`space-air-ground`](papers/space-air-ground.md) | 2026 | Integration and Intelligent Monitoring Technology System of Space-Air-Ground Remote Sensing | ISPRS Archives XLIX-B1-2026 | [综述、系统与基础设施](clusters/survey-infra.md) | 背景文献 |
| [`openearth-agent-zhao`](papers/openearth-agent-zhao.md) | 2026 | OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation | 预印本（arXiv:2603.22148）；会址待确认 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`openearthagent-shabbir`](papers/openearthagent-shabbir.md) | 2026 | OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents | 预印本（arXiv:2602.17665）；有 ECCV 2026 poster 线索，需与正式论文集再核 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P2 轨迹级后训练 |
| [`raven`](papers/raven.md) | 2026 | RAVEN: A Rapid Agentic Vision Framework for Emergency Response in Vulnerable Settlements | WACV 2026 Workshop (GeoCV) | [灾害应急与可执行评测](clusters/disaster-emergency.md) | 背景文献 |
| [`remotereasoner`](papers/remotereasoner.md) | 2026 | RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow | AAAI 2026 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`ringmo-agent`](papers/ringmo-agent.md) | 2026 | RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning | IEEE TPAMI（DOI: 10.1109/tpami.2026.3718699；卷期页以 Xplore 为准） | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`risk-aware`](papers/risk-aware.md) | 2026 | Risk-Aware LLM Agents for Geospatial Data Retrieval | ISPRS Archives XLIX-B3-2026 | [综述、系统与基础设施](clusters/survey-infra.md) | 背景文献 |
| [`rs-claw-evolution`](papers/rs-claw-evolution.md) | 2026 | RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents in Long-Horizon Tasks | 预印本（arXiv:2609.22258）；会址待确认 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`rs-claw`](papers/rs-claw.md) | 2026 | RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents | 预印本（arXiv:2605.13391）；会址待确认 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`simcraft`](papers/simcraft.md) | 2026 | SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning | EMNLP 2026 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`skymoe`](papers/skymoe.md) | 2026 | SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts | AAAI（OJS 37653）；届次以期刊页为准 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`spext`](papers/spext.md) | 2026 | SPEXT: A Decoupled Multi-Spectral Foundation Model for Earth Observation and Vision-Language Grounding | NeurIPS 2026 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`terrascope`](papers/terrascope.md) | 2026 | TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation | CVPR 2026 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`weaveagent`](papers/weaveagent.md) | 2026 | WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery | 预印本（arXiv:2609.31234）；会址待确认 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`zoomearth`](papers/zoomearth.md) | 2026 | ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks | CVPR 2026 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`choice`](papers/choice.md) | 2025 | CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models | NeurIPS 2025 Datasets and Benchmarks | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |
| [`disasterm3`](papers/disasterm3.md) | 2025 | DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response | NeurIPS 2025 Datasets and Benchmarks | [灾害应急与可执行评测](clusters/disaster-emergency.md) | 仅作感知底座或对照 |
| [`earthdial`](papers/earthdial.md) | 2025 | EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues | CVPR 2025 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`falcon`](papers/falcon.md) | 2025 | Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report) | 技术报告（arXiv:2503.11070）；会址待确认 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`fusar-klip`](papers/fusar-klip.md) | 2025 | FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing | 预印本（arXiv:2509.23927）；会址待确认 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`geo-olm`](papers/geo-olm.md) | 2025 | Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows | ACM COMPASS 2025 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`geobench-vlm`](papers/geobench-vlm.md) | 2025 | GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks | ICCV 2025 | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |
| [`geopixel`](papers/geopixel.md) | 2025 | GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing | ICML 2025 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`lisat`](papers/lisat.md) | 2025 | LISAT: Language-Instructed Segmentation Assistant for Satellite Imagery | NeurIPS 2025 Datasets and Benchmarks | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`geollm-squad`](papers/geollm-squad.md) | 2025 | Multi-Agent Geospatial Copilots for Remote Sensing Workflows | IGARSS 2025 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P1 模态–工具规划 |
| [`rescueadi`](papers/rescueadi.md) | 2025 | RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents | IEEE TGRS 2025 | [灾害应急与可执行评测](clusters/disaster-emergency.md) | P1 模态–工具规划 |
| [`rsgpt`](papers/rsgpt.md) | 2025 | RSGPT: A remote sensing vision language model and benchmark | ISPRS Journal of Photogrammetry and Remote Sensing 2025 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`skyeyegpt`](papers/skyeyegpt.md) | 2025 | SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning with large language model | ISPRS Journal of Photogrammetry and Remote Sensing 2025 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`teochat`](papers/teochat.md) | 2025 | TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data | ICLR 2025 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`thinkgeo`](papers/thinkgeo.md) | 2025 | ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks | 预印本（arXiv:2505.23752）。ICLR 2026 OpenReview 显示已撤稿；有 CVPR 2026 MONTI workshop 线索，不以 CVPR 主会论文引用 | [灾害应急与可执行评测](clusters/disaster-emergency.md) | P1 模态–工具规划 |
| [`univearth`](papers/univearth.md) | 2025 | Towards LLM Agents for Earth Observation | 预印本（arXiv:2504.12110）；会址待确认。arXiv 注释写 ACL 2026 Findings，本轮未在 Anthology 交叉核到正式页，不升格 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`vicot-agent`](papers/vicot-agent.md) | 2025 | VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis | 预印本（arXiv:2511.20085）；会址待确认 | [后训练、轨迹蒸馏与多智能体分工](clusters/post-training.md) | P2 轨迹级后训练 |
| [`lrs-vqa`](papers/lrs-vqa.md) | 2025 | When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning | ICCV 2025 | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |
| [`geoagent-chen`](papers/geoagent-chen.md) | 2024 | An LLM Agent for Automatic Geospatial Data Analysis | 预印本（arXiv:2410.18792）；会址待确认 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`change-agent`](papers/change-agent.md) | 2024 | Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis | IEEE TGRS 2024 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`earthgpt`](papers/earthgpt.md) | 2024 | EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension in Remote Sensing Domain | IEEE TGRS 2024 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`earthvqa`](papers/earthvqa.md) | 2024 | EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering | AAAI 2024 | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |
| [`eval-tool-agents`](papers/eval-tool-agents.md) | 2024 | Evaluating Tool-Augmented Agents in Remote Sensing Platforms | 预印本（arXiv:2405.00709）；会址按预印本 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | 背景文献 |
| [`geochat`](papers/geochat.md) | 2024 | GeoChat: Grounded Large Vision-Language Model for Remote Sensing | CVPR 2024 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`geollm-engine`](papers/geollm-engine.md) | 2024 | GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots | CVPR 2024 Workshop (EarthVision) | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | 背景文献 |
| [`lhrs-bot-nova`](papers/lhrs-bot-nova.md) | 2024 | LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing Vision-Language Interpretation | 预印本（arXiv:2411.09301）；会址待确认 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`lhrs-bot`](papers/lhrs-bot.md) | 2024 | LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model | ECCV 2024 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`rs-chatgpt`](papers/rs-chatgpt.md) | 2024 | Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models | IGARSS 2024 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | 背景文献 |
| [`remoteclip`](papers/remoteclip.md) | 2024 | RemoteCLIP: A Vision Language Foundation Model for Remote Sensing | IEEE TGRS 2024 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`rs-agent`](papers/rs-agent.md) | 2024 | RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent | 预印本（arXiv:2406.07089）；正文有 Science China Information Sciences 2025 卷线索，期刊页待交叉确认 | [工具规划、MCP 与遥感智能体](clusters/tool-planning.md) | P1 模态–工具规划 |
| [`rs-llava`](papers/rs-llava.md) | 2024 | RS-LLaVA: A Large Vision-Language Model for Joint Captioning and Question Answering in Remote Sensing Imagery | Remote Sensing 16(9):1477 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`rs-moe`](papers/rs-moe.md) | 2024 | RS-MoE: Mixture of Experts for Remote Sensing Image Captioning and Visual Question Answering | 预印本（arXiv:2411.01595）；会址待确认 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`skysense`](papers/skysense.md) | 2024 | SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery | CVPR 2024 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`skysensegpt`](papers/skysensegpt.md) | 2024 | SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding | 预印本（arXiv:2406.10100）；至交接清单完成时仍以预印本为主 | [感知底座与多源视觉语言模型](clusters/perception-foundation.md) | 仅作感知底座或对照 |
| [`vrsbench`](papers/vrsbench.md) | 2024 | VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding | NeurIPS 2024 Datasets and Benchmarks | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |
| [`rsvqa`](papers/rsvqa.md) | 2020 | RSVQA: Visual Question Answering for Remote Sensing Data | IEEE TGRS 2020 | [静态或单轮评测基准](clusters/static-benchmarks.md) | 仅作感知底座或对照 |

## 6. 术语跳转

| 术语 | 先读 | 说明 |
| --- | --- | --- |
| MCP | [`earth-agent`](papers/earth-agent.md), [`dora`](papers/dora.md), [`eo-gym`](papers/eo-gym.md) | 把工具/模型暴露成可调用接口；注意各文工具数与 schema 不同 |
| ReAct | [`earth-agent`](papers/earth-agent.md), [`thinkgeo`](papers/thinkgeo.md) | 推理–行动循环；不等于“规划一定正确” |
| 工具创造 | [`openearth-agent-zhao`](papers/openearth-agent-zhao.md) | 从预定义工具转向按节点生成工具 |
| 轨迹蒸馏 | [`simcraft`](papers/simcraft.md), [`vicot-agent`](papers/vicot-agent.md) | 把强 agent 的编排能力迁移到小模型 |
| agentic correctness | [`geollm-squad`](papers/geollm-squad.md) | 任务完成正确性指标；定义依论文而异 |
| step/final gap | [`thinkgeo`](papers/thinkgeo.md), [`dora`](papers/dora.md), [`eo-gym`](papers/eo-gym.md) | 步骤指标与最终答案的分离 |
| 光学–SAR 切换 | [`eo-gym`](papers/eo-gym.md), [`earthdial`](papers/earthdial.md), [`fusar-gpt`](papers/fusar-gpt.md) | 感知支持 vs 切换策略要分开写 |
| 伪推理 / Glance Effect | [`socrates`](papers/socrates.md) | 模型叙述推理但未真正取证 |
| 像素接地 | [`geopixel`](papers/geopixel.md), [`terrascope`](papers/terrascope.md), [`lisat`](papers/lisat.md) | 输出掩膜/像素证据，不等于工具规划 |
