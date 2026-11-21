# 静态或单轮评测基准

> 主题簇 · `static-benchmarks` · 6 篇 · 入口见 [`../INDEX.md`](../INDEX.md)

## 这类工作回答什么问题

VQA、字幕、定位、分类等固定输入协议；不能当作轨迹级 agent 评测。

## 代表论文

### [`vrsbench`](../papers/vrsbench.md) — VRSBench: A Versatile Vision-Language Benchmark Dataset for Remote Sensing Image Understanding

VRSBench 针对既有 RS 数据集单任务、缺目标细节、质控不足的问题，构建统一的多任务 VL 基准；规模为 29,614 图、52,472 指称、123,221 QA，且字幕经过人工核验。

[打开卡片](../papers/vrsbench.md) · 2024 · NeurIPS 2024 Datasets and Benchmarks

### [`geobench-vlm`](../papers/geobench-vlm.md) — GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks

GEOBench-VLM 指出通用 VLM 基准没有覆盖地学特有的时序变化、大范围计数、小目标检测与实体关系；基准含 10,000+ 人工核验指令，覆盖多种视觉条件、目标类型与尺度。

[打开卡片](../papers/geobench-vlm.md) · 2025 · ICCV 2025

### [`choice`](../papers/choice.md) — CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models

CHOICE 用选择题形式把遥感能力拆成感知与推理两层，避免开放式生成难以客观评分；10,507 道题经过统一采集、构造与质量控制，来源覆盖 50 个全球城市。

[打开卡片](../papers/choice.md) · 2025 · NeurIPS 2025 Datasets and Benchmarks

### [`lrs-vqa`](../papers/lrs-vqa.md) — When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning

论文指出固定网格会丢失 gigapixel RS 影像的细节，而无限制网格会带来不可接受的计算成本；LRS-VQA 含 7,333 个 QA 对、8 类问题，图像最长边 27,328 像素，专门压力测试大图感知。

[打开卡片](../papers/lrs-vqa.md) · 2025 · ICCV 2025

### [`earthvqa`](../papers/earthvqa.md) — EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering

EarthVQA 针对 RS 研究偏重目标位置/类别、忽视对象关系与综合推理的问题；数据含 6,000 图、208,593 QA，问题嵌入城乡治理需求。

[打开卡片](../papers/earthvqa.md) · 2024 · AAAI 2024

### [`rsvqa`](../papers/rsvqa.md) — RSVQA: Visual Question Answering for Remote Sensing Data

RSVQA 把 RS 信息提取统一成“自然语言问、影像答”的接口，降低非专家使用门槛；问题覆盖图像内容与关系依赖，答案可来自影像或外部地理数据。

[打开卡片](../papers/rsvqa.md) · 2020 · IEEE TGRS 2020

### 其余成员（只给跳转，不重复结论）

| 卡片 | 年份 | 会址 / 状态 | 与主张 |
| --- | --- | --- | --- |

## 共同能力边界

- 固定输入、单轮问答/字幕/定位，不包含工具调用或轨迹。
- 与轨迹级基准（Earth-Bench、ThinkGeo、DORA、EO-Gym）协议不同，不能横排分数。
- 彼此之间题目来源、答案形式与指标也不同，不能拼成一张总榜。
- 适合证明感知/推理底座不足，不能证明 agent 规划有效。

## 写作时何时进入

写静态 VLM 对比、benchmark 背景、任务定义或“感知仍不足”时进入。不要用它证明 agent 能力。
