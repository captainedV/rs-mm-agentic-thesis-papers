# 后训练、轨迹蒸馏与多智能体分工

> 主题簇 · `post-training` · 9 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

用轨迹监督、蒸馏、偏好/RL 与多 agent 分工改善步骤质量；这是 P2 的主战场。

## 代表论文

### [`simcraft`](../papers/simcraft.md) — SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning

SimCRAFT 的出发点是：强 RS agent 依赖大模型，部署成本高且缺领域知识，需要把“编排能力”蒸馏到小模型；数据侧用多 agent 合成 + Mock Execution Engine 校验 schema、工具依赖与传感器/工具兼容性，产出 SimRS-14k。

[打开卡片](../papers/simcraft.md) · 2026 · EMNLP 2026

### [`geommagent`](../papers/geommagent.md) — GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing

GeoMMBench 覆盖多学科、多传感器和多任务，目的是把“专家级”地学多模态能力拆成可诊断的维度；对 36 个开源与闭源模型的评估显示，领域知识、感知接地与推理存在系统性不足，单靠通用 MLLM 不够。

[打开卡片](../papers/geommagent.md) · 2026 · CVPR 2026

### [`geollm-squad`](../papers/geollm-squad.md) — Multi-Agent Geospatial Copilots for Remote Sensing Workflows

GeoLLM-Squad 的出发点是单 agent 随 RS 任务复杂度上升而退化，因此把编排与任务求解解耦，交给专用子 agent；实现基于开源 AutoGen 与 GeoLLM-Engine，可模块化接入城市监测、森林保护、气候分析和农业研究等应用。

[打开卡片](../papers/geollm-squad.md) · 2025 · IGARSS 2025

### [`hirs-agent`](../papers/hirs-agent.md) — HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving

论文把单体决策的长程失败归因于任务多阶段、工具误用与错误跨阶段传播；Manager/Specialist 分层把“下一步做什么”和“具体怎么调工具”拆开，并在步级做验证与重规划。

[打开卡片](../papers/hirs-agent.md) · 2026 · 预印本（arXiv:2608.30672）；会址待确认。arXiv 注释写 ACM MM 2026，未与正式论文集交叉核对，不升格

### [`weaveagent`](../papers/weaveagent.md) — WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery

论文指出预训练模型零样本几乎不发射工具调用，因此把路由做成“训练出来的能力”，而不是靠提示诱导；Stage A 的路由优先设计把 extrinsic 查询的路由率从 0% 提到 80.75%（323/400）。

[打开卡片](../papers/weaveagent.md) · 2026 · 预印本（arXiv:2609.31234）；会址待确认

### [`vicot-agent`](../papers/vicot-agent.md) — VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework for Interpretable Multimodal Reasoning and Scalable Remote Sensing Analysis

VICoT 的关键不是一次性生成答案，而是把视觉工具调用嵌进 CoT，形成可解释的多轮视觉–语言交替推理；栈式结构让 agent 能回退、重入和组合工具，适合需要多尺度观察的 RS 任务。

[打开卡片](../papers/vicot-agent.md) · 2025 · 预印本（arXiv:2511.20085）；会址待确认

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |
| [`socrates`](../papers/socrates.md) | 2026 | CVPR 2026 | P2 轨迹级后训练 |
| [`geocot`](../papers/geocot.md) | 2026 | CVPR 2026 | P2 轨迹级后训练 |
| [`rs-claw-evolution`](../papers/rs-claw-evolution.md) | 2026 | 预印本（arXiv:2609.22258）；会址待确认 | P2 轨迹级后训练 |

## 共同能力边界

- 各文的训练数据、奖励、基线与评测基准不同，不能把提升百分比横向比较。
- 只有少数工作报告“步骤正确/答案正确”的联合指标；多数只报最终任务分数，不能直接证明降低了 P2 的错误模式。
- 合成轨迹的可执行性校验不等于真实环境执行正确；蒸馏增益也可能来自数据规模而非方法本身。
- 多 agent 分工的增益可能来自额外调用/算力，不能全部归因于后训练。

## 写作时何时进入

写 P2 的轨迹监督、蒸馏、RL、多 agent 分工或“步骤–答案不一致”时进入。写工具接口本身时转到 `tool-planning`。
