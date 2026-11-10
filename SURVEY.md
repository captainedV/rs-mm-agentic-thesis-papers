# 多模态 + Agentic 遥感 / 地球观测：硕士开题文献综述与论文打包

**对象用户：** 夏浩翔（航天学院背景）  
**日期：** 2026-11-10（Asia/Shanghai）  
**文献清单权威来源：** `/workspace/handoffs/eo_agentic_ms_literature_2026-11-10.md`（本文不增补清单外论文）  
**配套文件：** `papers.json`（机器可读条目）、`pdfs/`（已重命名开放获取 PDF）、`papers-pdfs.zip`、`missing-pdfs.md`

---

## 0. 简明综述（开题用）

近两年，遥感多模态与 agentic 方法的交汇已从「遥感 VLM 对话」迅速转向「工具调用、多步规划与可执行评测」。2023–2024 的 GeoChat、EarthGPT、RemoteCLIP、RS-ChatGPT、Change-Agent、GeoLLM-Engine 等，分别奠定了接地对话、多传感器理解，以及用大模型调度视觉工具的早期范式。进入 2025–2026 年，可核验的主会主轴更加清晰：ICLR 2026 的 Earth-Agent 把 RGB 与光谱/产品纳入 MCP 工具生态并给出 Earth-Bench；CVPR 2026 的 GeoMMAgent 强调检索–感知–推理的多 agent；NeurIPS 2026 的 DORA 把评测拉到端到端灾害作业；EMNLP 2026 的 SimCRAFT 讨论轨迹蒸馏；IGARSS 2025 的 GeoLLM-Squad 展示子 agent 分工。与此同时，大量重要工作仍为预印本，且存在 `OpenEarthAgent`（工具调用，Shabbir 等）与 `OpenEarth-Agent`（工具创造，Zhao 等）等名称碰撞，引用时必须区分。ThinkGeo、GeoAssistant 等还出现撤稿记录，不能按已录用顶会引用。

底座侧，EarthDial、TEOChat、RingMo-Agent、FUSAR-GPT、GeoPixel、TerraScope 等提供了多传感器、时序与像素级推理能力，但它们多数是单轮或模型内推理，**不能直接等同于 tool-using agent**。评测协议正在从 RSVQA、EarthVQA、VRSBench、GEOBench-VLM、CHOICE 等静态 VLM 基准，迁移到 ThinkGeo、Earth-Bench、EO-Gym、UnivEARTH、OpenEarth-Bench、DORA 等轨迹级协议。工具集、是否允许规划提示、光学与光谱设定差异很大，不宜横排成一张 SOTA 榜。对航天场景尤其关键的缺口是：光谱/定量反演工具的参数接地仍然困难，SAR 上的 tool-augmented 评测很薄，长程灾害流水线在轨迹变长时与黄金路径差距显著，以及面向星上/边侧的轻量化与开放目录上的工具创造、安全问题。两年硕士宜避免从零预训练巨型 VLM，而应在已开源基准上做可评测的工具生态、模态策略或蒸馏。

---

## 0.1 本包交付统计

- 交接清单中的文献条目（含附录、工作坊、预印本与会址未确认工作，不含已撤稿不引用的 GeoAssistant）：见下文第 3 节表格。
- 已打包开放获取 PDF：**57** 篇，合计约 **467.5 MB**。
- 未能打包全文：**4** 篇（ExpertsRS、SkyMoE、SPEXT、RS-LLaVA），详见 0.2 节。
- 压缩包：`/workspace/rs-mm-agentic-survey/papers-pdfs.zip`

## 0.2 未能打包的开放/正式 PDF（见 missing-pdfs.md）

| 论文 | 原因 | 正式页 |
|---|---|---|
| ExpertsRS (Sun et al., *Big Earth Data* 2026) | Taylor & Francis 可能需订阅，未发现开放预印本 | https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178 |
| SkyMoE (AAAI OJS 37653) | 本环境从 OJS download 接口只得到 HTML，未发现对应 arXiv | https://ojs.aaai.org/index.php/AAAI/article/view/37653 |
| SPEXT (NeurIPS 2026) | 交接清单仅有海报页，未给出论文 PDF 或 arXiv | https://neurips.cc/virtual/2026/poster/153724 |
| RS-LLaVA (MDPI *Remote Sensing* 16(9):1477) | 期刊页一般为开放获取，但本环境请求 PDF 返回 403 | https://www.mdpi.com/2072-4292/16/9/1477 |

另：若干 IEEE TGRS / TPAMI / ISPRS JPRS / IGARSS 正式出版 PDF 可能需订阅。凡有 arXiv 或 CVF/NeurIPS/ICLR/ACL/ISPRS Archives 开放文本者，本包已收录开放版本，不下载付费墙全文。PMLR 上 GeoPixel 的官方 PDF 本环境下载失败，已改用 arXiv:2501.13925。AAAI 正式页（RemoteReasoner、EarthVQA）同样未能下到出版社 PDF，已改用对应 arXiv。

## 0.3 核心数据集与基准（交接清单 + 已核官方页）

说明：下列 URL 仅列出本轮能核对到的项目页、GitHub 或 Hugging Face；没有可靠官方地址的不编造。静态 VLM 基准与工具轨迹基准协议不同，不能直接横比分数。

| 名称 | 任务 | 模态 | 规模（以论文/项目页为准） | 来源论文 | 官方 URL | 指标/关系 |
|---|---|---|---|---|---|---|
| Earth-Bench | EO agent 轨迹与最终答案（Spectrum / Products / RGB） | 光谱、产品、RGB | 248 题、13,729 图 | Earth-Agent (ICLR 2026) | https://huggingface.co/datasets/Sssunset/Earth-Bench ；代码 https://github.com/opendatalab/Earth-Agent | 轨迹 + 最终答案 |
| GeoMMBench | 地学/遥感多模态问答 | 多传感器、多学科 | 评估 36 个模型；题量以项目页为准 | GeoMMAgent (CVPR 2026) | https://geo-mm-agi.github.io/ | 多模态问答 |
| ThinkGeo | 工具增强 RS agent 逐步/端到端评测 | 光学 RGB + SAR | 486 任务、1,778 专家步骤、14 工具（含 50 条 SAR） | ThinkGeo (arXiv:2505.23752；不以 ICLR/CVPR 主会计) | https://github.com/mbzuai-oryx/ThinkGeo ；https://huggingface.co/datasets/MBZUAI/ThinkGeo | Inst/Tool/Arg 与最终答案；SAR 上最终答案很低 |
| DORA | 端到端灾害响应 agent | 光学/SAR/多光谱、DEM、OSM/WorldPop 等 | 515 专家任务、45 场灾害、108 个 MCP 工具 | DORA (NeurIPS 2026) | https://github.com/Junjue-Wang/DORA | 与黄金轨迹差距等；摘要称最长流水线差距可约 56% |
| CHOICE | LVLM 遥感感知与推理（多图/多时相） | 遥感影像 | 约 10,507 任务 | CHOICE (NeurIPS 2025 D&B) | 交接清单未确认唯一官方仓 | 静态 VLM，非 tool agent |
| GEOBench-VLM | 地学 VLM：场景、计数、定位、分割、时间分析 | 光学、多光谱、SAR、多时相等 | 10,000+ 人工核验指令，8 类 | GEOBench-VLM (ICCV 2025) | https://the-ai-alliance.github.io/GEO-Bench-VLM/ | 项目页称最强模型选择题约 40% 量级 |
| VRSBench | 字幕、视觉定位、开放 VQA | 光学 | 29,614 图；52,472 指称；123,221 QA | VRSBench (NeurIPS 2024 D&B) | https://vrsbench.github.io/ ；https://github.com/lx709/VRSBench | 静态综合 VL 基准 |
| DisasterM3 | 灾害损毁评估与响应 VLM 数据 | 灾害遥感 | 以 NeurIPS 2025 论文为准 | DisasterM3 (NeurIPS 2025 D&B) | 未在交接清单单列已核仓 | 被 DORA 作为影像来源之一 |
| LRS-VQA | 超大遥感影像 VQA | 超大光学影像 | 7,333 QA，最长边至 27,328 像素 | Luo et al., ICCV 2025 | 未确认独立数据页 | 分辨率挑战；也被部分 agent 论文使用 |
| EO-Gym-Data | 交互式 EO agent 轨迹 | 多模态（xView、DOTA、FAIR1M、xBD、Landsat/Sentinel-2 等） | 9,078 轨迹、34,604 步；环境 >66 万文件、35 工具 | EO-Gym (arXiv:2605.01250) | https://huggingface.co/datasets/paperuploadacount/EO-Gym （账户名异常，下载前再核镜像） | Pass@3 等；摘要称 4B 主设置 0.49→0.74 |
| OpenEarth-Bench | 开放环境全流程（规划与工具创造） | 多源 EO | 596 条案例、7 个应用域 | OpenEarth-Agent (Zhao et al.) | https://github.com/walking-shadow/OpenEarth-Agent | 与 Earth-Bench 交叉评测 |
| UnivEARTH | 真实 GEE 代码取证是否题 | 15+ 卫星仪器 | 408 题、7 类主题 | Kao et al., arXiv:2504.12110 | https://iandrover.github.io/2025_univearth/ | 零样本最高约 40%，reflexion 后约 60%；大量代码无法运行 |
| OpenEarthAgent corpus | 工具增强推理轨迹（训练+评测） | 光学/SAR、GIS、NDVI/NBR/NDBI | 14,538 / 1,169，约 107K 步 | OpenEarthAgent (Shabbir et al.) | https://github.com/mbzuai-oryx/OpenEarthAgent | 步骤级工具/参数与最终答案 |
| GeoCode | 地理空间代码/函数调用 | GEE 及其他库 | 28 库、2313 函数调用 | GeoAgent (Chen et al.) | https://github.com/Yusin2Chen/GeoAgent | 代码执行与任务完成 |
| RSVQA-LR/HR | 遥感 VQA | 低分/高分光学，答案来自 OSM 等 | 见项目页 | RSVQA (TGRS 2020) | https://rsvqa.sylvainlobry.com/ | 领域经典静态 VQA |
| EarthVQA | 关系推理型 RS VQA | 光学（与 LoveDA 相关） | 以论文/仓库为准 | EarthVQA (AAAI 2024) | https://github.com/Junjue-Wang/EarthVQA | 静态对照基准 |
| MMRS-1M | 多传感器图文/指令数据 | 光学/SAR/红外等，34 个数据集转化 | >100 万对 | EarthGPT (TGRS 2024) | https://github.com/wivizhang/EarthGPT | 多传感器 VLM 训练数据 |
| FIT-RS | 细粒度遥感指令微调 | 光学等 | 以 SkySenseGPT 论文为准 | SkySenseGPT (arXiv:2406.10100) | 交接清单未确认正式刊与仓 | 指令数据，非 agent 轨迹 |
| RSICap / RSIEval | 高质量字幕与评测 | 光学 | 以 RSGPT 论文为准 | RSGPT (ISPRS JPRS 2025) | 未单列已核数据页 | 早期高质量评测 |
| SkyEye-968k | 多任务 RS 指令微调 | 光学等，含视频字幕方向 | 常见表述 968k | SkyEyeGPT (ISPRS JPRS 2025) | 未强制列未核仓 | 指令数据 |
| LHRS-Instruct / LHRS-Bench | VGI 增强指令与评测 | 光学 + VGI | 以 LHRS-Bot 论文为准 | LHRS-Bot (ECCV 2024) | 未强制列仓 | 早期指令资源 |
| EarthDial-Instruct | 多传感器多时相对话指令 | RGB/SAR/多光谱等 | >11.11M 指令对；44 个下游集 | EarthDial (CVPR 2025) | https://github.com/hiyamdebary/EarthDial | 分类、检测、字幕、VQA、定位、变化检测等 |
| RS-VL3M | 多平台多模态图文 | 卫星+无人机；光学/SAR/红外 | >300 万图文对 | RingMo-Agent (TPAMI) | 未发现可核官方仓 | 介于 VLM 与 agent 之间 |
| RescueADI 数据集 | 自适应灾害解译 | 灾害遥感 | 摘要/机构页称 4,044 图 | RescueADI (TGRS 2025) | 本次未核到独立仓 | 灾害 agent 数据 |
| Terra-CoT / TerraScope-Bench | 像素接地推理（答案+掩膜） | 光学/SAR，可多时相 | 以 TerraScope 论文为准 | TerraScope (CVPR 2026) | 未确认仓 | 明确对比外部工具路线 |
| RS-CoT-20k | 遥感思维链数据 | 多任务 RS | 20k 量级（按论文名） | GeoCoT (CVPR 2026) | 论文称代码将公开 | 推理型 MLLM 数据 |
| LEVIR-MCI | 交互式综合变化解释 | 双时相光学等 | 以 Change-Agent 论文为准 | Change-Agent (TGRS 2024) | https://github.com/Chen-Yang-Liu/Change-Agent | 变化检测 agent 数据 |

## 0.4 已打包 PDF 文件名

目录：`/workspace/rs-mm-agentic-survey/pdfs/`（不含 `_raw` 缓存）。命名：`YYYY-Venue-ShortTitle-FirstAuthor.pdf`。预印本会址写作 `arXiv`。

- `2020-TGRS-RSVQA-Lobry.pdf`（5,409,151 bytes）
- `2024-AAAI-EarthVQA-Wang.pdf`（6,477,518 bytes）
- `2024-CVPR-GeoChat-Kuckreja.pdf`（2,529,446 bytes）
- `2024-CVPR-SkySense-Guo.pdf`（9,119,101 bytes）
- `2024-CVPRW-GeoLLM-Engine-Singh.pdf`（4,750,334 bytes）
- `2024-ECCV-LHRS-Bot-Muhtar.pdf`（24,290,580 bytes）
- `2024-IGARSS-RS-ChatGPT-Guo.pdf`（473,107 bytes）
- `2024-NeurIPS-VRSBench-Li.pdf`（1,194,421 bytes）
- `2024-TGRS-Change-Agent-Liu.pdf`（17,430,738 bytes）
- `2024-TGRS-EarthGPT-Zhang.pdf`（10,298,888 bytes）
- `2024-TGRS-RemoteCLIP-Liu.pdf`（14,105,741 bytes）
- `2024-arXiv-EvaluatingToolAgents-Singh.pdf`（9,446,036 bytes）
- `2024-arXiv-GeoAgent-Chen.pdf`（1,377,319 bytes）
- `2024-arXiv-LHRS-Bot-Nova-Li.pdf`（21,961,056 bytes）
- `2024-arXiv-RS-Agent-Xu.pdf`（6,398,134 bytes）
- `2024-arXiv-RS-MoE-Lin.pdf`（2,530,787 bytes）
- `2024-arXiv-SkySenseGPT-Luo.pdf`（17,917,353 bytes）
- `2025-COMPASS-Geo-OLM-Stamoulis.pdf`（4,093,336 bytes）
- `2025-CVPR-EarthDial-Soni.pdf`（2,589,639 bytes）
- `2025-ICCV-GEOBench-VLM-Danish.pdf`（2,921,743 bytes）
- `2025-ICCV-LRS-VQA-Luo.pdf`（6,113,945 bytes）
- `2025-ICLR-TEOChat-Irvin.pdf`（10,504,150 bytes）
- `2025-ICML-GeoPixel-Shabbir.pdf`（28,501,335 bytes）
- `2025-IGARSS-GeoLLM-Squad-Lee.pdf`（1,972,976 bytes）
- `2025-ISPRS-RSGPT-Hu.pdf`（3,112,730 bytes）
- `2025-ISPRS-SkyEyeGPT-Zhan.pdf`（24,503,893 bytes）
- `2025-NeurIPS-CHOICE-An.pdf`（4,191,384 bytes）
- `2025-NeurIPS-DisasterM3-Wang.pdf`（9,041,247 bytes）
- `2025-NeurIPS-LISAT.pdf`（14,716,299 bytes）
- `2025-TGRS-RescueADI-Liu.pdf`（1,421,882 bytes）
- `2025-arXiv-FUSAR-KLIP-Yang.pdf`（51,100,843 bytes）
- `2025-arXiv-Falcon-Yao.pdf`（7,350,857 bytes）
- `2025-arXiv-ThinkGeo-Shabbir.pdf`（6,845,567 bytes）
- `2025-arXiv-UnivEARTH-Kao.pdf`（1,060,582 bytes）
- `2025-arXiv-VICoT-Agent-Wang.pdf`（11,663,447 bytes）
- `2026-AAAI-RemoteReasoner-Yao.pdf`（1,648,992 bytes）
- `2026-CVPR-AskingLikeSocrates-Shao.pdf`（4,411,042 bytes）
- `2026-CVPR-FUSAR-GPT-Zhang.pdf`（18,251,075 bytes）
- `2026-CVPR-GeoCoT-Li.pdf`（3,051,059 bytes）
- `2026-CVPR-GeoMMBench-GeoMMAgent-Xiao.pdf`（2,010,741 bytes）
- `2026-CVPR-TerraScope-Shu.pdf`（10,785,352 bytes）
- `2026-CVPR-ZoomEarth-Liu.pdf`（5,056,315 bytes）
- `2026-EMNLP-SimCRAFT-Wang.pdf`（3,065,857 bytes）
- `2026-ICLR-Earth-Agent-Feng.pdf`（13,513,347 bytes）
- `2026-ISPRS-RiskAware-Gao.pdf`（952,276 bytes）
- `2026-ISPRS-SpaceAirGround-Liu.pdf`（1,329,866 bytes）
- `2026-NeurIPS-DORA-Wang.pdf`（3,740,695 bytes）
- `2026-TPAMI-RingMo-Agent-Hu.pdf`（9,832,952 bytes）
- `2026-WACVW-AgenticAI-RS-Talemi.pdf`（11,907,008 bytes）
- `2026-WACVW-RAVEN-Maitra.pdf`（3,868,470 bytes）
- `2026-arXiv-EO-Gym-Ma.pdf`（3,741,124 bytes）
- `2026-arXiv-HiRS-Agent-Mu.pdf`（2,186,377 bytes）
- `2026-arXiv-OpenEarth-Agent-Zhao.pdf`（3,286,615 bytes）
- `2026-arXiv-OpenEarthAgent-Shabbir.pdf`（4,954,473 bytes）
- `2026-arXiv-RS-Claw-Evolution-Ouyang.pdf`（4,779,093 bytes）
- `2026-arXiv-RS-Claw-Liu.pdf`（1,842,247 bytes）
- `2026-arXiv-WeaveAgent-Pang.pdf`（5,866,579 bytes）

---

## 以下为权威交接清单全文（已并入本综述；PDF 文件名见第 0.4 节）

# 多模态 + Agentic 遥感 / 地球观测：硕士开题文献筛查

**对象用户：** 夏浩翔（航天学院背景）  
**日期戳：** 2026-11-10（Asia/Shanghai）  
**深度：** abstract / 公开元数据级；不编造论文、作者、会址、指标或链接  
**版本优先：** 能核到同行评议正式版则优先于旧预印本  
**结论先行：** 2024-11 至 2026-11 交汇处已从「遥感 VLM 对话」迅速转到「工具调用 / 多步规划 / MCP 工具生态 / 可执行评测」。核心 agent 主会论文仍相对精；ICLR 2026 的 Earth-Agent、CVPR 2026 的 GeoMMAgent、NeurIPS 2026 的 DORA、EMNLP 2026 的 SimCRAFT、IGARSS 2025 的 GeoLLM-Squad 构成可核验的主轴。大量 2026 年工作仍为预印本。名称碰撞显著：`OpenEarthAgent`（工具调用，Shabbir 等）与 `OpenEarth-Agent`（工具创造，Zhao 等）不是同一篇。

---

## 1. 调研范围与检索词

### 1.1 纳入 / 排除
- **纳入：** 多模态（光学 / 文本 / SAR / 多光谱 / 高光谱等）**并且**具有 agentic 要素（工具调用、多步规划、LLM/VLM agent、function calling、MCP 类工具路由、在 EO 数据上的规划/具身），并与遥感 / Earth Observation / 卫星影像任务结合。航天相关（星载 EO、多传感器、灾害应急）优先。
- **时间：** 主窗口 **2024-11 至 2026-11**。2023–2024 初的该线基础工作放入 **F. 附录**，并标明。期刊 2025–2026 正式刊出、但预印本更早的工作，按正式会址年份放入主表，并注明预印本时间。
- **排除：** 编造文献或链接；把「仅多模态 RS、无工具/规划」硬塞进 agent 核心（这些放入相邻组 A/D）；仓库若无法打开则不列。Workshop 仅收录对该线有综述/框架意义者，并标明工作坊。
- **会址标注规则：** 已在 CVF / ICLR proceedings / PMLR / ACL Anthology / IEEE Xplore / 期刊官网核到的写正式会址；仅预印本或 OpenReview 撤稿写 **预印本 / 会址待确认** 或 **已撤稿**。

### 1.2 主要检索词（WebSearch + WebFetch，多路并行）
- `LLM / VLM / MLLM / agent / tool use / function calling / planning / MCP` + `remote sensing / Earth observation / satellite / SAR / multispectral`
- 专名：Earth-Agent, RS-Agent, GeoAgent, GeoLLM-Engine, GeoLLM-Squad, ThinkGeo, OpenEarthAgent, OpenEarth-Agent, EO-Gym, UnivEARTH, VICoT, Geo-OLM, ExpertsRS, DORA, RescueADI, Change-Agent, EarthGPT, GeoChat, EarthDial, TEOChat, RingMo-Agent, FUSAR-GPT, RemoteReasoner, SimCRAFT, GeoMMAgent 等（专名由检索发现，不事先虚构）
- 会刊：`CVPR/ICCV/ECCV/NeurIPS/ICLR/ICML/AAAI/ACM MM/ACL/EMNLP 2025 2026 remote sensing VLM agent`；`TGRS / ISPRS / RSE 2025 2026 large language model remote sensing agent`
- 基准：EarthVQA, RSVQA, VRSBench, GEOBench-VLM, Earth-Bench, ThinkGeo, CHOICE, DisasterM3, DORA, UnivEARTH, EO-Gym-Data 等（仅收录能核到的）

### 1.3 组织丝（按实际检索调整）
- **A.** 遥感 / EO 多模态基础模型（VLM/MLLM）：后续 agent 的感知底座（**多数本身不是 agent**）
- **B.** 在 EO 数据上做工具调用 / 多步规划的 LLM/VLM agent（**核心**）
- **C.** RS/EO 的 agent 评测基准与协议
- **D.** SAR / 多光谱 / 多传感器 + 语言或 agent
- **E.** 下游 EO 任务上的 agentic 流水线（变化检测、灾害、VQA、规划等）
- **F.** 附录：2023–2024 初基础工作
- 综述 / 工作坊单独列出，不计入核心算法主会。

---

## 2. 分丝现状短述

**B 核心（agent）已成形，但协议碎片化。** 早期单 agent 把 LLM 当控制器、调用检测/分割/分类工具（RS-Agent、RS-ChatGPT、Change-Agent）。2025–2026 转向：(i) **可执行工具注册表 + 轨迹监督/评测**（ThinkGeo、Earth-Agent、OpenEarthAgent、EO-Gym）；(ii) **多 agent 分工**（GeoLLM-Squad、ExpertsRS、GeoMMAgent）；(iii) **MCP 标准化工具接口**（Earth-Agent 104 工具、DORA 108 工具、VICoT）；(iv) **从调用已有工具到创造工具**（OpenEarth-Agent）；(v) **交互式取证**：在空间/时间/模态间主动取数（EO-Gym），以及面向真实 GEE 目录的代码 agent（UnivEARTH）。公开实验反复显示：工具选对不等于参数/轨迹对，最终答案正确率仍明显低于轨迹指标。

**A 底座很密，但不要与 agent 混排。** GeoChat / EarthGPT / EarthDial / TEOChat / RingMo-Agent / FUSAR-GPT 等提供多传感器对话与推理能力，是 agent 的视觉前端或对比基线。它们通常是单轮或模型内推理，**默认不能替代 tool-using agent**。EarthDial（CVPR 2025）与 RingMo-Agent（TPAMI）因覆盖 SAR/多光谱，对航天场景特别重要。

**C 基准正在从 VQA 迁到轨迹级。** RSVQA / EarthVQA / VRSBench / GEOBench-VLM / CHOICE 评估静态 VLM；ThinkGeo、Earth-Bench、OpenEarthAgent corpus、EO-Gym-Data、DORA、UnivEARTH、OpenEarth-Bench 评估工具序列。互相不可硬比：工具集、是否允许规划提示、是否 verified 检测、光学 vs 光谱，协议差很大。

**D 多传感器是明显缺口。** 多个 VLM 已支持 SAR/多光谱（EarthGPT、EarthDial、FUSAR-GPT、RingMo-Agent、SPEXT），但 **SAR 上的 tool-augmented agent 评测仍然很薄**。ThinkGeo 含 50 条 SAR 任务，补充材料显示即使强模型最终答案也很低。Earth-Agent 强调光谱/产品而不只是 RGB。EO-Gym 把光学–SAR 切换写成一等公民动作。

**E 下游。** 变化检测（Change-Agent）、灾害（RescueADI、DisasterM3、DORA）、城市/农业/气候工作流（GeoLLM-Squad、Geo-OLM）、情报报告式多轮视觉工具链（VICoT）已有工作。DORA 明确指出：灾害响应不只是损毁评估，还要路网、人口、疏散与报告，现有 RS agent 基准很少覆盖端到端作业。

---

## 3. 按丝分类的文献列表

说明：摘要级贡献概述；指标只写摘要/公开页中出现且可核对的数字，**不作跨文横向排名**。仓库仅列本次 HTTP 200 核到的地址。

### B. 核心：EO 上的工具调用 / 规划 Agent

| 题目 | 作者（短） | 年份 | 会址 / arXiv | 贡献概要 | PDF/OA | 仓库 | 数据 / 任务 |
|---|---|---|---|---|---|---|---|
| Earth-Agent: Unlocking the Full Landscape of Earth Observation with Agents | Feng, Lv, Ye, et al. | 2026 | **ICLR 2026**；arXiv:2509.23141 | 将 RGB 与光谱/产品统一进 MCP 工具生态（摘要称 104 个工具、五类工具包），以 ReAct 做多步定量时空推理，并提出同时评估轨迹与最终结果的 Earth-Bench。 | [arXiv](https://arxiv.org/abs/2509.23141)；[ICLR PDF](https://proceedings.iclr.cc/paper_files/paper/2026/file/5b4a459db23e6db9be2a128380953d96-Paper-Conference.pdf) | [opendatalab/Earth-Agent](https://github.com/opendatalab/Earth-Agent)；数据集 [HF Earth-Bench](https://huggingface.co/datasets/Sssunset/Earth-Bench) | Earth-Bench：248 题、13,729 图；Spectrum / Products / RGB；GEE、NASA Earthdata、AID、DOTA 等 |
| GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing | Xiao, Cheng, Xu, et al. | 2026 | **CVPR 2026** | 提出覆盖多学科、多传感器、多任务的 GeoMMBench；并给出检索–感知–推理的多 agent，用领域 RS 模型与工具增强独立 LLM。 | [CVF HTML](https://openaccess.thecvf.com/content/CVPR2026/html/Xiao_GeoMMBench_and_GeoMMAgent_Toward_Expert-Level_Multimodal_Intelligence_in_Geoscience_and_CVPR_2026_paper.html)；[PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Xiao_GeoMMBench_and_GeoMMAgent_Toward_Expert-Level_Multimodal_Intelligence_in_Geoscience_and_CVPR_2026_paper.pdf) | 项目页 [geo-mm-agi.github.io](https://geo-mm-agi.github.io/)（论文未在摘要中给出单一仓库句；未单列未核仓库） | GeoMMBench；评估 36 个开源/闭源模型 |
| Multi-Agent Geospatial Copilots for Remote Sensing Workflows（GeoLLM-Squad） | Liao, Yu, Li, et al. | 2025 | **IGARSS 2025**；arXiv:2501.16254 | 在 AutoGen + GeoLLM-Engine 上把编排与任务求解分离，交给城市/农业/森林/气候/卫星视觉等子 agent。摘要称相对基线 agentic correctness 约 +17%。 | [arXiv](https://arxiv.org/abs/2501.16254)；[IEEE](https://doi.org/10.1109/igarss55030.2025.11243915)（可能需订阅） | 未在摘要中发现独立新仓库；框架基于开源 AutoGen 与 GeoLLM-Engine | MODIS / GHS / Hansen GFC 等产品；xView、FAIR、fMoW 等；约 2k 生成任务 |
| Geo-OLM: Enabling Sustainable Earth Observation Studies with Cost-Efficient Open Language Models & State-Driven Workflows | Stamoulis & Marculescu | 2025 | **ACM COMPASS 2025**；arXiv:2504.04319 | 用开源小模型 + 状态驱动工作流降低 EO 研究的成本，强调可持续部署。 | [arXiv](https://arxiv.org/abs/2504.04319)；[ACM DL](https://dl.acm.org/doi/full/10.1145/3715335.3735494) | [dstamoulis/geo-olms](https://github.com/dstamoulis/geo-olms) | EO 工作流 / 开放语言模型 |
| An LLM-based multi-agent system for remote sensing analysis（ExpertsRS） | Sun et al. | 2026 | **Big Earth Data**（2026-01-08 在线；收稿 2025-06-02） | 面向非专家的 Data–Tools–Brain 多 agent（AutoGen + DeepSeek-V3 原型 ExpertsRS），把含糊查询转成可执行分析流程。 | [Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178)（可能需订阅；摘要可公开读） | 未发现导航仓库 | 遥感分析工作流（非单一公开 benchmark 名） |
| SimCRAFT: Distilling Remote Sensing Agents via Synthetic Trajectories and Contextual Retrieval-Augmented Fine-Tuning | Wang, Yao, Yang, et al. | 2026 | **EMNLP 2026**；arXiv:2608.30277 | 用合成轨迹与检索增强微调，把多 agent RS 工作流规划蒸馏到较小模型。 | [arXiv](https://arxiv.org/abs/2608.30277)；[ACL Anthology](https://aclanthology.org/2026.emnlp-main.2674/) | 摘要未确认独立仓库 | 合成 RS agent 轨迹 |
| OpenEarthAgent: A Unified Framework for Tool-Augmented Geospatial Agents | Shabbir, Sheikh, Munir, et al. | 2026 | arXiv:2602.17665；有 **ECCV 2026 poster** 页面线索，建议同时保留预印本并与主会论文集交叉核对 | 统一可执行工具注册表 + 轨迹监督微调（Qwen3-4B）；语料含光学/SAR、GIS 与 NDVI/NBR/NDBI。对比表强调自身同时具备 GIS、光谱与变化检测及推理监督数据。 | [arXiv](https://arxiv.org/abs/2602.17665) | [mbzuai-oryx/OpenEarthAgent](https://github.com/mbzuai-oryx/OpenEarthAgent) | 14,538 训练 / 1,169 评测，约 107K 推理步 |
| OpenEarth-Agent: From Tool Calling to Tool Creation for Open-Environment Earth Observation | Zhao, Liu, Zhang, et al. | 2026 | arXiv:2603.22148；**会址待确认**（与上一篇名称易混） | 强调开放环境下 **创造工具** 而非只调用预定义工具：数据探测、DAG 规划、按节点生成 Python 工具并迭代校验。提出 OpenEarth-Bench（596 条全流程案例、7 个应用域）。跨基准称仅用 6 个预训练模型工具可接近调用 104 工具的 Earth-Agent。 | [arXiv](https://arxiv.org/abs/2603.22148) | [walking-shadow/OpenEarth-Agent](https://github.com/walking-shadow/OpenEarth-Agent)（论文写 “will be available”，本次访问为 200） | OpenEarth-Bench；Earth-Bench 交叉评测 |
| EO-Gym: A Multimodal, Interactive Environment for Earth Observation Agents | Ma, Li, Li, et al. | 2026 | arXiv:2605.01250；**会址待确认** | Gymnasium 风格本地 EO 工作空间：>66 万多模态文件，35 个工具；支持空间平移/缩放、历史观测拉取、光学–SAR 切换。EO-Gym-4B 在主设置下将 Pass@3 从 0.49 提到 0.74。 | [arXiv](https://arxiv.org/abs/2605.01250) | 论文给出 [HF: paperuploadacount/EO-Gym](https://huggingface.co/datasets/paperuploadacount/EO-Gym)（账户名异常，使用时再核镜像） | EO-Gym-Data：9,078 轨迹、34,604 步；xView、DOTA、FAIR1M、xBD、Landsat/Sentinel-2 等 |
| Towards LLM Agents for Earth Observation（UnivEARTH） | Kao, Zhao, et al. | 2025 | arXiv:2504.12110；**会址待确认** | 从 NASA Earth Observatory 文章构建 408 道需用 **GEE 代码取证** 的是否题；零样本最高约 40% 正确且大量代码无法运行，reflexion 后约 60%，仍接近随机上限之上不远。强调真实目录/传感器 ID 幻觉，而非只测预定义工具。 | [arXiv](https://arxiv.org/abs/2504.12110) | 项目页 [iandrover.github.io/2025_univearth](https://iandrover.github.io/2025_univearth/) | UnivEARTH；15+ 卫星仪器；GEE |
| VICoT-Agent: A Vision-Interleaved Chain-of-Thought Framework… | Wang, Luo, Liu, et al. | 2025 | arXiv:2511.20085；**会址待确认** | 把视觉工具动态插入思维链，MCP 工具集 + 推理栈蒸馏到 Qwen3-14B，面向边侧/低显存；工具含开集检测、去云雨、超分、RAG 等。相对 Plan-Execute，摘要称 token −65%、时延 −48%。 | [arXiv](https://arxiv.org/abs/2511.20085) | 未发现导航仓库 | RSVQA、MME-RealWorld-RS、LRS-VQA 等；自建 VICoT-HRSC |
| RS-Agent: Automating Remote Sensing Tasks through Intelligent Agent | Xu, Yu, Mu, et al. | 预印 2024-06；正文有 **Science China Information Sciences 2025** 卷线索 | arXiv:2406.07089；期刊页**待与官网交叉确认**，故不完全按已录用主会处理 | LLM 中控 + 工具箱 + Solution Space（任务感知检索）+ Knowledge Space（DualRAG）；支持光学与 SAR 工具编排。规划准确率摘要称超 95%。 | [arXiv](https://arxiv.org/abs/2406.07089) | [IntelliSensing/RS-Agent](https://github.com/IntelliSensing/RS-Agent) | RSSDIVCS、RSVQA、DOTA 等；18 类任务实验 |
| An LLM Agent for Automatic Geospatial Data Analysis（GeoAgent） | Chen, Wang, Lobry, Kurtz | 2024-10 预印（窗口边缘，可与附录对照） | arXiv:2410.18792；**会址待确认** | 代码解释器 + 静态分析 + RAG，嵌入 MCTS，生成可执行地理空间 Python；并提出 GeoCode 基准（单轮/多轮、28 库、2313 函数调用）。 | [arXiv](https://arxiv.org/abs/2410.18792) | [Yusin2Chen/GeoAgent](https://github.com/Yusin2Chen/GeoAgent)（200；论文原写 will be available） | GeoCode（含 GEE 与其它库） |

**2026 预印本、方法相关但会址未确认（质量保留、不升格为主会）：**

| 题目 | 作者线索 | arXiv | 要点 | 仓库 |
|---|---|---|---|---|
| RS-Claw: Progressive Active Tool Exploration via Hierarchical Skill Trees for Remote Sensing Agents | 见 arXiv 页 | [2605.13391](https://arxiv.org/abs/2605.13391) | 用层级技能树缓解工具规模过大时的探索问题 | 未在本次核到稳定仓库 |
| RS-Claw-Evolution: Environment-Feedback-Driven Evolution for Lightweight Remote Sensing Agents… | 见 arXiv 页 | [2609.22258](https://arxiv.org/abs/2609.22258) | 环境反馈驱动的轻量 RS agent 演化 | 未确认 |
| WeaveAgent: A Two-Stage Tool-Routing Agent for Ultra-High-Resolution Remote Sensing Imagery | 见 arXiv 页 | [2609.31234](https://arxiv.org/abs/2609.31234) | 超高分辨率影像的两阶段工具路由 | 未确认 |
| HiRS-Agent: A Hierarchical Multi-Agent System for Reliable Long-Horizon Remote Sensing Task Solving | 见 arXiv 页 | [2608.30672](https://arxiv.org/abs/2608.30672) | 分层多 agent 做长程 RS 任务 | 未确认 |

**GeoAssistant**（OpenReview: [xvRpSz6rr6](https://openreview.net/forum?id=xvRpSz6rr6)）：工具增强的地学视觉语言助手，支持光学/SAR。检索显示 **ICLR 2026 已撤稿**，不以录用论文引用。

---

### C. 基准与 Agent 评测

| 题目 | 作者（短） | 年份 | 会址 | 贡献概要 | PDF/OA | 仓库 | 数据 / 任务 |
|---|---|---|---|---|---|---|---|
| ThinkGeo: Evaluating Tool-Augmented Agents for Remote Sensing Tasks | Shabbir, Munir, Dudhane, et al. | 2025 | arXiv:2505.23752；**ICLR 2026 OpenReview 显示已撤稿**；有 CVPR 2026 MONTI workshop 线索，**不以 CVPR 主会计** | 首个大规模面向 RS 的 tool-augmented agent 基准：ReAct、逐步+端到端指标；含光学与 SAR。分析显示工具准确率与规划一致性差距大，最终答案准确率远低于步骤指标。 | [arXiv](https://arxiv.org/abs/2505.23752) | [mbzuai-oryx/ThinkGeo](https://github.com/mbzuai-oryx/ThinkGeo) | 486 任务、1,778 专家步骤、14 工具；DOTA、xBD、FloodNet、SSDD 等 |
| Can LLM Agents Respond to Disasters? …（DORA） | Wang, Xuan, Qi, et al. | 2026 | **NeurIPS 2026**（会议海报页可核）；arXiv:2605.11633 | 端到端灾害响应 agent 基准：515 专家任务、45 场真实灾害、108 个 MCP 工具；覆盖感知、空间关系、作业规划、时间演化、多模态报告。13 个前沿模型上，最长流水线与黄金轨迹差距可到约 56%。 | [arXiv](https://arxiv.org/abs/2605.11633)；[NeurIPS poster](https://neurips.cc/virtual/2026/poster/139774) | [Junjue-Wang/DORA](https://github.com/Junjue-Wang/DORA) | 光学/SAR/多光谱、DEM、OSM/WorldPop 等；xBD、DisasterM3、BRIGHT 等 |
| CHOICE: Benchmarking the Remote Sensing Capabilities of Large Vision-Language Models | An, Sun, Gui, He 等（以论文页为准） | 2025 | **NeurIPS 2025** D&B；arXiv:2411.18145 | 评测 LVLM 的遥感感知与推理（含多图、多时相），偏 VLM 而非 tool agent。 | [NeurIPS PDF](https://proceedings.neurips.cc/paper_files/paper/2025/file/befe25a01cf4dbe9635e85f835d31250-Paper-Datasets_and_Benchmarks_Track.pdf)；[arXiv](https://arxiv.org/abs/2411.18145) | 未在本次检索中确认唯一官方仓 | 摘要称约 10,507 任务 |
| GEOBench-VLM: Benchmarking Vision-Language Models for Geospatial Tasks | Danish et al. | 2025 | **ICCV 2025** | 面向地学任务的 VLM 基准（场景理解、计数、定位、分割、时间分析等），偏静态评测。 | [CVF HTML](https://openaccess.thecvf.com/content/ICCV2025/html/Danish_GEOBench-VLM_Benchmarking_Vision-Language_Models_for_Geospatial_Tasks_ICCV_2025_paper.html) | 未在摘要中确认 | 10,000+ 指令级任务（摘要/会议页） |
| VRSBench: A Versatile Vision-Language Benchmark… | Li, Ding, Elhoseiny | 2024 | **NeurIPS 2024** D&B（2024-12，落在主窗口） | 遥感图文理解综合基准：字幕、视觉定位、开放 VQA。 | [NeurIPS PDF](https://proceedings.neurips.cc/paper_files/paper/2024/file/05b7f821234f66b78f99e7803fffa78a-Paper-Datasets_and_Benchmarks_Track.pdf)；[arXiv](https://arxiv.org/abs/2406.12384) | [lx709/VRSBench](https://github.com/lx709/VRSBench) | 约 29k 图像量级（论文页） |
| DisasterM3: A Remote Sensing Vision-Language Dataset for Disaster Damage Assessment and Response | Wang, Xuan, et al. | 2025 | **NeurIPS 2025** D&B | 灾害损毁评估与响应的遥感 VLM 数据与评测，被 DORA 作为影像来源之一引用。 | [NeurIPS abstract](https://proceedings.neurips.cc/paper_files/paper/2025/hash/ec80d18205e39d42a27192d5f3ddd688-Abstract-Datasets_and_Benchmarks_Track.html) | 未在本次单列核仓 | 灾害多模态 VQA / 评估 |
| LRS-VQA / When Large Vision-Language Model Meets Large Remote Sensing Imagery… | Luo, Zhang, Yang, et al. | 2025 | **ICCV 2025** | 面向超大/十亿像素级 RS 影像的文本引导 token 剪枝，并构建 LRS-VQA（7,333 QA，最长边至 27,328 像素）。是分辨率挑战，不是 tool agent。 | [CVF HTML](https://openaccess.thecvf.com/content/ICCV2025/html/Luo_When_Large_Vision-Language_Model_Meets_Large_Remote_Sensing_Imagery_Coarse-to-Fine_ICCV_2025_paper.html) | 未确认 | LRS-VQA |

Earth-Bench、EO-Gym-Data、OpenEarth-Bench、UnivEARTH 已在对应方法文中列出，不重复占行。

---

### A. 相邻组：RS / EO 多模态基础模型（后续 agent 的底座；本身通常非 agent）

| 题目 | 作者（短） | 年份 | 会址 | 贡献概要 | PDF/OA | 仓库 | 数据 / 任务 |
|---|---|---|---|---|---|---|---|
| EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues | Soni, Dudhane, Debary, et al. | 2025 | **CVPR 2025**；arXiv:2412.15190 | 对话式 EO VLM，支持多光谱、多时相、多分辨率及 RGB/SAR 等；11.11M 指令对；44 个下游数据集。 | [CVF PDF](https://openaccess.thecvf.com/content/CVPR2025/papers/Soni_EarthDial_Turning_Multi-sensory_Earth_Observations_to_Interactive_Dialogues_CVPR_2025_paper.pdf)；[arXiv](https://arxiv.org/abs/2412.15190) | [hiyamdebary/EarthDial](https://github.com/hiyamdebary/EarthDial) | EarthDial-Instruct；分类、检测、字幕、VQA、推理、定位、变化检测等 |
| TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data | Irvin, Liu, Chen, et al. | 2025 | **ICLR 2025**；arXiv:2410.06234 | 面向时间序列 EO 的视觉语言助手，强调变化与时序推理。 | [ICLR PDF](https://proceedings.iclr.cc/paper_files/paper/2025/file/ac3af725ae398b6184faae0828bdbd6c-Paper-Conference.pdf)；[arXiv](https://arxiv.org/abs/2410.06234) | [ermongroup/teochat](https://github.com/ermongroup/teochat) | 时序 EO / 变化 |
| SkyEyeGPT: Unifying remote sensing vision-language tasks via instruction tuning… | Zhan, Xiong, Yuan | 2025 | **ISPRS JPRS 2025** | 指令微调统一多种 RS 视觉语言任务，并含视频字幕方向。 | [DOI](https://doi.org/10.1016/j.isprsjprs.2025.01.020) | 预印本仓常见为作者主页/arXiv:2401.09712；未在此强制列未核 GitHub | SkyEye-968k 等 |
| RSGPT: A remote sensing vision language model and benchmark | Hu, Yuan, Wen, et al. | 2025 | **ISPRS JPRS 2025**（预印本 2023） | 较早的 RS VLM + 高质量标注基准，后续大量工作以其为基线。 | [DOI](https://doi.org/10.1016/j.isprsjprs.2025.03.028) | 预印本 arXiv:2307.15266 | RSICap 等 |
| RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning | Hu, Wang, Feng, et al. | 2025/26 | **IEEE TPAMI**，DOI: 10.1109/tpami.2026.3718699（与 arXiv:2507.20776 对应；期刊卷期以 Xplore 页为准） | 卫星+无人机，光学/SAR/红外；RS-VL3M（>300 万图文对）。含外部视觉定位工具 + RL 优化轨迹解码，用于长程导航类推理（CityNav 等），介于 VLM 与 agent 之间。 | [arXiv](https://arxiv.org/abs/2507.20776)；[IEEE](https://doi.org/10.1109/tpami.2026.3718699) | 未在摘要中给出单一 GitHub；**未发现可核官方仓则不列** | RS-VL3M；感知+关系推理+任务调度/动作决策等 |
| GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing | Shabbir et al. | 2025 | **ICML 2025** | 高分辨率 RS 的像素级定位与掩膜生成。 | [PMLR](https://proceedings.mlr.press/v267/shabbir25a.html) | 未在此强制列 | 像素级 grounding |
| RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow | 见 arXiv/AAAI 页 | 2026 | **AAAI 2026**；arXiv:2507.19280 | 用 MLLM + RL 与任务变换，统一对象/区域/像素级地学推理工作流（偏模型内推理，不一定是外部工具 agent）。 | [arXiv](https://arxiv.org/abs/2507.19280)；[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/38175) | [1e12Leon/RemoteReasoner](https://github.com/1e12Leon/RemoteReasoner) | 多粒度地学推理 |
| TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation | Shu et al. | 2026 | **CVPR 2026** | 「用像素思考」：在推理链中交错生成掩膜；支持光学/SAR 自适应融合与多时相。明确对比先前依赖外部工具的 EO VLM。 | [CVF PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Shu_TerraScope_Pixel-Grounded_Visual_Reasoning_for_Earth_Observation_CVPR_2026_paper.pdf) | 未确认 | Terra-CoT、TerraScope-Bench |
| Asking like Socrates: Socrates helps VLMs understand remote sensing images（RS-EoT） | Shao et al. | 2026 | **CVPR 2026** | 针对 RS「伪推理/Glance Effect」，用自博弈多 agent 合成推理轨迹，再分阶段 RL，强调证据寻找而非只叙事。 | [CVF PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Shao_Asking_like_Socrates_Socrates_helps_VLMs_understand_remote_sensing_images_CVPR_2026_paper.pdf) | 项目 [geoxlab.github.io/Asking_like_Socrates](https://geoxlab.github.io/Asking_like_Socrates/) | RS VQA / grounding |
| GeoCoT: Towards Reliable Remote Sensing Reasoning with Manifold Perspective | Li et al. | 2026 | **CVPR 2026** | 流形驱动 MoE + CoT，及 RSV-GRPO；构建 RS-CoT-20k。是推理型 MLLM，不是工具 agent。 | [CVF HTML](https://openaccess.thecvf.com/content/CVPR2026/html/Li_GeoCoT_Towards_Reliable_Remote_Sensing_Reasoning_with_Manifold_Perspective_CVPR_2026_paper.html) | 论文称代码将公开 | 多任务 RS；RS-CoT-20k |
| ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks | Liu et al. | 2026 | **CVPR 2026** | 超高分辨率地学 VL 任务的主动感知（缩放/聚焦），接近「视觉工具式」交互，但主要是模型策略。 | [CVF PDF](https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_ZoomEarth_Active_Perception_for_Ultra-High-Resolution_Geospatial_Vision-Language_Tasks_CVPR_2026_paper.pdf) | [earth-insights/ZoomEarth](https://github.com/earth-insights/ZoomEarth) | 超高分辨率地学 VL |
| Falcon: A Remote Sensing Vision-Language Foundation Model (Technical Report) | Wang et al. | 2025 | arXiv:2503.11070；**技术报告，会址待确认** | 较小统一 RS VLM，覆盖图像/区域/像素级多种任务。 | [arXiv](https://arxiv.org/abs/2503.11070) | [TianHuiLab/Falcon](https://github.com/TianHuiLab/Falcon) | 多任务 RS VL |
| LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing… | 见 arXiv 页 | 2024-11 | arXiv:2411.09301；**会址待确认** | LHRS-Bot 改进版，增强 RS 视觉语言解释。 | [arXiv](https://arxiv.org/abs/2411.09301) | 未强制列 | RS 指令跟随 |
| RS-MoE: Mixture of Experts for Remote Sensing Image Captioning and Visual Question Answering | 见 arXiv 页 | 2024-11 | arXiv:2411.01595；**会址待确认** | 指令路由 + 轻量专家，用于字幕与 VQA。 | [arXiv](https://arxiv.org/abs/2411.01595) | 未确认 | 字幕 / VQA |
| SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts | 见 AAAI 页 | 2026? | **AAAI**（[ojs 37653](https://ojs.aaai.org/index.php/AAAI/article/view/37653)）；具体届次以期刊页为准 | 混合专家增强多任务、多粒度地学解释。 | 上列 OJS | 未确认 | 地学解释 |

LISAt / LISAT（**NeurIPS 2025** D&B）：语言指令驱动的卫星影像分割助手，偏分割助手而非工具规划 agent。[NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2025/hash/a38a009bb015775b7685b5ef3c206310-Abstract-Datasets_and_Benchmarks_Track.html)

---

### D. SAR / 多光谱 / 多传感器 + 语言或 Agent

| 题目 | 作者（短） | 年份 | 会址 | 贡献概要 | PDF/OA | 仓库 | 数据 / 任务 |
|---|---|---|---|---|---|---|---|
| FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery | Zhang et al. | 2026 | **CVPR 2026** | SAR 专用 VLM，嵌入时空特征、两阶段解耦。 | [CVF HTML](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_FUSAR-GPT_A_Spatiotemporal_Feature-Embedded_and_Two-Stage_Decoupled_Visual_Language_Model_CVPR_2026_paper.html) | 未在摘要确认 | SAR 图文 |
| FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing | 见 arXiv 页 | 2025 | arXiv:2509.23927；**会址待确认** | 面向 SAR 的多模态基础模型，含地理元数据与推理向标注。 | [arXiv](https://arxiv.org/abs/2509.23927) | [yangyifremad/FUSAR-KLIP](https://github.com/yangyifremad/FUSAR-KLIP) | SAR 多模态 |
| SPEXT: A Decoupled Multi-Spectral Foundation Model for Earth Observation and Vision-Language Grounding | 见会议页 | 2026 | **NeurIPS 2026** poster | 解耦多光谱基础模型，用于 EO 与视觉语言定位。 | [NeurIPS poster](https://neurips.cc/virtual/2026/poster/153724) | 未确认 | 多光谱 EO / grounding |
| EarthGPT: A Universal Multi-modal Large Language Model for Multi-sensor Image Comprehension… | Zhang, Cai, Zhang, Zhuang, Mao | 2024 | **IEEE TGRS 2024**；arXiv:2401.16822（基础工作，因多传感器被大量 2025–26 agent 引用，此处与附录双见） | 统一光学 / SAR / 红外的 RS MLLM；构建 MMRS-1M（>100 万对，34 个数据集转化）。 | [arXiv](https://arxiv.org/abs/2401.16822)；IEEE TGRS 正式版 | [wivizhang/EarthGPT](https://github.com/wivizhang/EarthGPT) | MMRS-1M |

ThinkGeo、Earth-Agent、EO-Gym、EarthDial、RingMo-Agent、RS-Agent 均显式涉及 SAR 或光谱，见 B/A 表。

---

### E. 下游 EO 任务上的 Agentic 流水线

| 题目 | 作者（短） | 年份 | 会址 | 贡献概要 | PDF/OA | 仓库 | 数据 / 任务 |
|---|---|---|---|---|---|---|---|
| Change-Agent: Toward Interactive Comprehensive Remote Sensing Change Interpretation and Analysis | Liu, Chen, Zhang, et al. | 2024 | **IEEE TGRS 2024**；DOI: 10.1109/TGRS.2024.3425815（刊出在窗口附近，预印本 2024-03，可与附录对照） | 多层变化解释模型 + LLM 规划调用 Python 工具（计数、原因分析、变化预测等）。 | [arXiv](https://arxiv.org/abs/2403.19646)；[IEEE](https://doi.org/10.1109/tgrs.2024.3425815) | [Chen-Yang-Liu/Change-Agent](https://github.com/Chen-Yang-Liu/Change-Agent) | LEVIR-MCI 等 |
| RescueADI: Adaptive Disaster Interpretation in Remote Sensing Images with Autonomous Agents | Liu, Zhao, Yuan, Jiang | 2025 | **IEEE TGRS 2025**；arXiv:2410.13384 | LLM agent 规划并执行一系列感知任务，再识别结果以回答复杂灾害问题；工具含分割面积计算、A* 路径等。 | [arXiv](https://arxiv.org/abs/2410.13384)；[IEEE](https://ieeexplore.ieee.org/document/10849780) | 未在本次核到独立仓 | RescueADI 数据集：4,044 图等（摘要/机构页） |
| Risk-Aware LLM Agents for Geospatial Data Retrieval… | Gao, Cumming, Li, Xu, Clausi | 2026 | **ISPRS Archives XLIX-B3-2026** | 自然语言查询云端地理空间目录；Guardrail / QA / Recommender 三 agent；对抗多轮下的 API 操纵安全。 | [OA PDF](https://isprs-archives.copernicus.org/articles/XLIX-B3-2026/1419/2026/isprs-archives-XLIX-B3-2026-1419-2026.pdf) | 未发现 | 目录检索 / API 生成 |
| Integration and Intelligent Monitoring Technology System of Space-Air-Ground Remote Sensing… | Liu, You, Jiang, et al. | 2026 | **ISPRS Archives XLIX-B1-2026** | 航天应用向综述+系统：空天遥感监测 agent，自然语言解析、任务链与多算法执行；湖南废弃矿生态修复案例。偏系统集成，算法创新有限。 | [OA PDF](https://isprs-archives.copernicus.org/articles/XLIX-B1-2026/369/2026/isprs-archives-XLIX-B1-2026-369-2026.pdf) | 不适用 | 应用案例 |

DORA、GeoLLM-Squad、VICoT（情报报告）、Socrates（数据合成 agent）亦属下游交叉，见上表。

**工作坊（仅作地图，不升格主会）：**
- Talemi et al., *Agentic AI in Remote Sensing: Foundations, Taxonomy, and Emerging Systems*，**WACV 2026 Workshop (GeoCV)**。[CVF PDF](https://openaccess.thecvf.com/content/WACV2026W/GeoCV/papers/Talemi_Agentic_AI_in_Remote_Sensing_Foundations_Taxonomy_and_Emerging_Systems_WACVW_2026_paper.pdf)
- Maitra et al., *RAVEN: A Rapid Agentic Vision Framework for Emergency Response in Vulnerable Settlements*，**WACV 2026W GeoCV**。[CVF PDF](https://openaccess.thecvf.com/content/WACV2026W/GeoCV/papers/Maitra_RAVEN_A_Rapid_Agentic_Vision_Framework_for_Emergency_Response_in_WACVW_2026_paper.pdf)

---

### F. 附录：2023–2024 初基础工作（该线的直接前驱）

| 题目 | 作者（短） | 年份 | 会址 | 贡献概要 | PDF/OA | 仓库 | 备注 |
|---|---|---|---|---|---|---|---|
| GeoChat: Grounded Large Vision-Language Model for Remote Sensing | Kuckreja, Danish, Naseer, et al. | 2024 | **CVPR 2024**；arXiv:2311.15826 | 首个面向 RS 的接地对话 VLM：区域输入、坐标输出、多任务指令数据。后续几乎所有 RS-MLLM/agent 的对比基线。 | [arXiv](https://arxiv.org/abs/2311.15826)；CVPR 正式版 | [mbzuai-oryx/geochat](https://github.com/mbzuai-oryx/geochat) | 318k 指令；AID/UCMerced/RSVQA 等 |
| RemoteCLIP: A Vision Language Foundation Model for Remote Sensing | Liu et al. | 2024 | **IEEE TGRS 2024** | RS 对比图文基础模型，为开放词汇与检索提供底座。 | [DOI](https://doi.org/10.1109/tgrs.2024.3390838) | 常见开源实现多，以论文页为准 | 对比学习 / 零样本 |
| LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model | Muhtar, Li, Gu, Zhang, Xiao | 2024 | **ECCV 2024**；arXiv:2402.02544 | 用 VGI（如 OSM）增强的 RS MLLM。 | [arXiv](https://arxiv.org/abs/2402.02544) | 未强制列 | LHRS-Instruct / LHRS-Bench |
| GeoLLM-Engine: A Realistic Environment for Building Geospatial Copilots | Singh, Fore, Stamoulis | 2024 | **CVPR 2024 Workshop (EarthVision)** | 真实感地理空间 Copilot 环境，多轮工具 API，后为 GeoLLM-Squad 底座。 | [CVPRW PDF](https://openaccess.thecvf.com/content/CVPR2024W/EarthVision/papers/Singh_GeoLLM-Engine_A_Realistic_Environment_for_Building_Geospatial_Copilots_CVPRW_2024_paper.pdf)；[arXiv](https://arxiv.org/abs/2404.15500) | 未在本次单列核仓 | 卫星视觉等工作流 |
| Evaluating Tool-Augmented Agents in Remote Sensing Platforms | Singh, Fore, Stamoulis | 2024 | arXiv:2405.00709；**会址按预印本** | 早期系统评测 RS 平台上的工具增强 agent。 | [arXiv](https://arxiv.org/abs/2405.00709) | 未确认 | RS 平台工具评测 |
| Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models | Guo, Su, Wu, Du, Zhang, Li | 2024 | **IGARSS 2024** | ChatGPT 串联预训练视觉模型，是后续 agent 常比的早期系统。 | IEEE IGARSS 2024；预印本 arXiv:2401.09083 | 未强制列 | 检测/分类/字幕等 |
| SkySense: A Multi-Modal Remote Sensing Foundation Model… | Guo et al. | 2024 | **CVPR 2024** | 多模态 RS 视觉基础模型（偏视觉 FM，不是对话 agent）。 | [CVF PDF](https://openaccess.thecvf.com/content/CVPR2024/papers/Guo_SkySense_A_Multi-Modal_Remote_Sensing_Foundation_Model_Towards_Universal_Interpretation_CVPR_2024_paper.pdf) | 未强制列 | 多模态 EO 影像 |
| EarthVQA: Towards Queryable Earth via Relational Reasoning-Based Remote Sensing Visual Question Answering | Wang, Zheng, Chen, Ma, Zhong | 2024 | **AAAI 2024** | 关系推理型 RS VQA，后常被 agent 论文当作静态 VQA 对照。 | [DOI](https://doi.org/10.1609/aaai.v38i6.28357) | 未强制列 | EarthVQA |
| RSVQA: Visual Question Answering for Remote Sensing Data | Lobry, Marcos, Murray, Tuia | 2020 | **IEEE TGRS 2020** | 领域经典 VQA 基准（超出时间窗，仅作评测祖先）。 | 正式刊 | — | RSVQA-LR/HR |
| RS-LLaVA | Bazi et al. | 2024 | *Remote Sensing* 16(9):1477 | 联合字幕与问答的 RS LLaVA 变体。 | [MDPI](https://www.mdpi.com/2072-4292/16/9/1477) | 未强制列 | 字幕 / VQA |
| SkySenseGPT | Luo et al. | 2024-06 | arXiv:2406.10100；**至本次仍以预印本为主** | 细粒度指令数据与关系推理向 RS MLLM。 | [arXiv](https://arxiv.org/abs/2406.10100) | 未确认正式刊 | FIT-RS 等 |

---

## 4. 适合两年航天硕士的 3–5 个开题切入点

以下缺口均能在上文文献中直接找到表述，不另发明题。两年硕士宜避免从零训练千万级指令的巨型 VLM，宜做**可评测的工具生态、模态策略或轻量化**，并尽量用已开源基准复现。

**切入点 1：光谱 / 定量反演工具链上的 EO Agent（对准 Earth-Agent 的 Spectrum 难点）**  
- **文献缺口：** Earth-Agent 指出既有 EO agent 多困在 RGB 感知；其分模态结果显示 Spectrum 子集更难（原始观测、多图、专业反演）。UnivEARTH 则显示真实 GEE 目录上的传感器/产品 ID 幻觉与空集合错误是主因。  
- **方法方向：** 在开源 Earth-Agent / Earth-Bench 工具协议上，专做 Index + Inversion 工具的参数接地（波段、缩放因子、无效值掩膜），加入目录检索或校验器；报告轨迹指标与最终物理量误差，而不是只报 VQA。  
- **可行性：** 工具级改进与评测，不需要自建大 VLM；与航天定量遥感（LST、水汽、植被指数）直接对齐。

**切入点 2：光学–SAR 交叉与「何时切模态」的工具规划**  
- **文献缺口：** ThinkGeo 补充材料：SAR 上即使 GPT-4 系列最终答案仍很低（摘要级描述为 <6% 量级）。EO-Gym 把 Cross-Modal Switching 写成一等公民，并发现通才模型在时间/跨模态工作流上弱。EarthDial、FUSAR-GPT、RingMo-Agent 提供 SAR 感知底座，但 **SAR 专用 tool-use 基准仍稀**。  
- **方法方向：** 以 EO-Gym / ThinkGeo-SAR / DORA 的光学–SAR 任务为评测，做「云/夜/应急时的模态选择 + 对齐裁剪 + 检测工具」策略，而不是再训一个 SAR 字幕模型。  
- **可行性：** 航天多源载荷（光学+SAR）是学院自然场景；可用已有开源工具与本地索引，计算量可控。

**切入点 3：长程、参数级可靠的灾害响应 Agent（对准 DORA）**  
- **文献缺口：** DORA 显示失败主要在损毁语义接地、传感器模态错配、流水线组合；给黄金工具顺序后最终准确率只升约 1–4%；轨迹变长时与黄金轨迹差距可扩大到约 56%。RescueADI、DisasterM3 提供感知与数据前置。  
- **方法方向：** 不追求「再做一个 108 工具库」，而做 **参数/掩膜版本约束、中间校验与可重放轨迹**（例如损坏等级索引、GSD、上下游掩膜绑定），在 DORA 的 T3–T5（作业规划、时间演化、报告）上报告改进。  
- **可行性：** 基准与工具已开源；适合把系统可靠性写成硕士主贡献。

**切入点 4：面向星上/边侧的轻量 RS Agent（蒸馏、技能树、成本）**  
- **文献缺口：** VICoT 明确提出边侧部署与推理栈蒸馏；Geo-OLM 强调开源小模型与成本；SimCRAFT 做轨迹蒸馏；RS-Claw 讨论工具过多时的分层技能。Earth-Agent 也指出通用 agent 难以吞下成百上千张影像。  
- **方法方向：** 教师轨迹（Earth-Agent / OpenEarthAgent / VICoT）蒸馏到 3B–7B 级模型，约束工具子集（Skill vs All，如 EO-Gym），报告成功率、非法调用率与时延/显存。  
- **可行性：** 两年内可完成数据整理、蒸馏与消融；对航天平台算力约束有明确应用叙事。

**切入点 5（备选）：开放目录上的「工具创造 vs 工具调用」与安全**  
- **文献缺口：** OpenEarth-Agent 指出预定义工具在开放数据上会硬编码传感器参数、忽略无效值；UnivEARTH 指出闭式工具基准与真实 GEE 目录有落差；ISPRS 2026 的 Risk-Aware 工作指出检索 agent 的对抗与 API 操纵风险。  
- **方法方向：** 小规模「探测元数据 → 生成/改写一条指数或反演脚本 → 物理范围校验」的闭环，并加入简单护栏；用 OpenEarth-Bench 子集或 UnivEARTH 的 Landsat/MODIS 题评测。  
- **可行性：** 范围必须收窄（单一产品族），否则两年内容易做成不可复现的提示工程。

---

## 5. 缺口与不确定

1. **会址未确认或已撤稿：** ThinkGeo（ICLR 2026 撤稿）、GeoAssistant（撤稿）、VICoT、EO-Gym、UnivEARTH、OpenEarth-Agent（Zhao）、RS-Claw / WeaveAgent / HiRS-Agent、FUSAR-KLIP、Falcon、LHRS-Bot-Nova、RS-MoE、SkySenseGPT 等，引用时必须写预印本，不能写成已录用顶会。OpenEarthAgent（Shabbir）的 ECCV 2026 线索需与正式论文集再核一次。  
2. **名称碰撞：** `OpenEarthAgent` vs `OpenEarth-Agent`；`Earth-Agent` vs 早期个别博客/项目也用 EarthAgent；`GeoAgent`（Chen 等，代码生成）vs 其它 GeoAgent/GeoGPT；`RS-Agent` 还曾被用于图像生成 agent（IGARSS 2024 另一文，本筛查未展开）。  
3. **RingMo-Agent 期刊年份：** DOI 含 2026，arxiv 为 2025-07；请以 IEEE Xplore 卷期页为准。RS-Agent 的 Science China 2025 线索未独立打开期刊官网全文。  
4. **仓库与数据托管：** EO-Gym 的 Hugging Face 账户名为 `paperuploadacount`，属异常命名，建议下载前再核官方镜像。部分论文写 “code will be available”，本次仅列出已 200 的仓。  
5. **协议不可比：** 不要把 EarthDial 的 VQA 准确率与 Earth-Agent 的 Tool-Exact-Match、EO-Gym 的 Pass@3、DORA 的最终答案准确率排成一张「SOTA 榜」。  
6. **相邻非 agent 工作很多：** GeoCoT、TerraScope、ZoomEarth、CHOICE、GEOBench-VLM 等对开题有用，但若开题写成「agentic」，须避免把它们算进核心方法贡献。  
7. **RSE 主刊、ACM MM 在该精确交汇上的命中偏少**（本次未把未核到的条目写进表）。ISPRS Archives 有系统/安全论文，算法深度通常弱于 ICLR/CVPR/NeurIPS。  
8. **本报告为 abstract/元数据级**，未精读全部 PDF 实验设定；数字若用于开题开题书，建议对照正文表格再核。  
9. **未写入 Notion**（按协作 Bot 要求）。SendToAgent 工具在本执行环境中不可用，本文件供父代理转交 Bot 与用户。

---

*检索与核链完成于 2026-11-10，Asia/Shanghai。*
