# 多模态 + Agentic 遥感开题论文包

本仓库是夏浩翔硕士开题用的**私有文献包**，收录 2024.11–2026.11 前后「多模态 / 视觉语言模型 + 工具调用或多智能体方法 + 遥感 / 地球观测」方向的开放获取论文 PDF。整理日期：2026-11-10（Asia/Shanghai）。

仓库为私有，仅供本人开题与后续研究使用。其中 PDF 均来自 arXiv、CVF Open Access、ICLR / NeurIPS / ACL 等会议开放渠道或 Copernicus 开放档案，**不是**出版社付费墙正式版的镜像，请勿公开分发或当作官方抽印本。

配套综述与数据集 / benchmark 笔记写在 Notion 草稿页：[多模态 + Agentic 遥感开题文献综述（2024.11–2026.11）](https://app.notion.com/p/4148f718d0be817b8d15fbc12388fdae?pvs=204)。

## 仓库内容

- `pdfs/`：59 篇已核对的开放获取 PDF，文件名格式为 `YYYY-Venue-ShortTitle-FirstAuthor.pdf`
- `papers.json`：机器可读目录（标题、会址、arXiv、开源地址、摘要要点）
- `missing-pdfs.md`：未能收入的 2 篇及正式版改用预印本的说明
- `SURVEY.md`：开题用简明综述与选题切入点
- `catalog/`：面向写作 agent 的多层 Markdown 文献目录（61 张论文卡片 + 6 个主题簇）

## 文献目录（catalog/）

`catalog/` 不是给人速读的综述，而是让写作 agent 用尽量少的上下文完成检索：先定位相关论文卡片，读取已核对的结论，再决定是否打开全文 PDF。

推荐检索顺序：

1. 读 [`catalog/SKILL.md`](catalog/SKILL.md)，确认何时加载、回复格式与引用纪律；
2. 读 [`catalog/CLAIM.md`](catalog/CLAIM.md)，把当前句子对齐到 P1 模态–工具规划或 P2 轨迹级后训练；
3. 从 [`catalog/INDEX.md`](catalog/INDEX.md) 按“主张 / 问题 / 方法 / 基准”四条路径定位候选卡片；
4. 只打开 1–2 个相关 [`catalog/clusters/`](catalog/clusters/) 主题簇；
5. 再打开 1–3 张 `catalog/papers/<id>.md` 卡片（先按 `INDEX.md` 或 cluster 里的 id 找）；
6. 仅当需要具体数字、评测协议、工具列表或原文表述时，才打开 `pdfs/` 中对应全文。

| 路径 | 用途 |
| --- | --- |
| [`catalog/SKILL.md`](catalog/SKILL.md) | 入口：加载时机、强制阅读顺序、检索回复格式、引用纪律 |
| [`catalog/CLAIM.md`](catalog/CLAIM.md) | 已锁定主张、P1/P2 拆解、文献能/不能支撑什么、证据缺口 |
| [`catalog/INDEX.md`](catalog/INDEX.md) | 四条检索路径 + 61 篇全目录 |
| [`catalog/clusters/`](catalog/clusters/) | 灾害应急、工具规划、后训练、感知底座、静态基准、综述基础设施 |
| [`catalog/papers/`](catalog/papers/) | 一篇一卡：元数据、bib key、PDF 路径、结论、数字、边界、何时开全文 |
| [`catalog/index.json`](catalog/index.json) | 机器可读索引（不含结论正文） |
| [`catalog/OUT_OF_CATALOG.md`](catalog/OUT_OF_CATALOG.md) | 未入库零散 PDF 审计 |

卡片约定：

- 61 条官方条目全部有卡片；59 条有 `pdfs/` 全文，ExpertsRS 与 SPEXT 只保留元数据卡片和正式页链接。
- 39 条沿用开题 `ref.bib` 的 bib key；22 条标注「尚未写入开题 `.bib`」。
- 结论后的 `[摘要]` / `[正文]` / `[papers.json 摘要要点；未核正文]` / `[目录判断]` 表示证据来源，不要把“未核正文”当成原文结论。
- 关键数字带来源位置；不同评测协议下的分数不排成对照表，论文卡片也不充当 SOTA 榜。
- 新增文献时先更新 `papers.json`，再建 `catalog/papers/<id>.md`，并同时补 `INDEX.md` 与对应 cluster；未入库的零散 PDF 只登记在 `catalog/OUT_OF_CATALOG.md`。

## 建议优先阅读

1. Earth-Agent（ICLR 2026）
2. GeoMMBench / GeoMMAgent（CVPR 2026）
3. DORA（NeurIPS 2026）
4. SimCRAFT（EMNLP 2026）
5. GeoLLM-Squad（IGARSS 2025）
6. EarthDial（CVPR 2025）
7. TEOChat（ICLR 2025）
8. ThinkGeo（仅作 arXiv:2505.23752 预印本与基准；不以 ICLR / CVPR 主会论文引用）

写作或核对引用时，不必按上面顺序通读；直接从 `catalog/SKILL.md` 进入，按需跳转卡片与全文。

## 引用时请注意

- **OpenEarthAgent**（Shabbir，工具调用）与 **OpenEarth-Agent**（Zhao，工具创造）是两篇不同的论文，不要混用。
- GeoAssistant 在交接清单中记为 ICLR 2026 已撤稿，本仓库不收录，也不作为录用论文引用。ThinkGeo 的 ICLR 2026 投稿按交接说明处理，只保留上述预印本。
- UnivEARTH、HiRS-Agent 的 arXiv 注释中出现过 ACL 2026 Findings、ACM MM 2026 等会址，尚未独立复核会议页，文件名仍标为 arXiv，不升格会址。
- 若干 IEEE / ISPRS JPRS / AAAI / PMLR 正式版当时未能下载或可能需订阅，已改用对应 arXiv 或会议开放 PDF，详见 `missing-pdfs.md`。
- SkyMoE 已收入开放获取全文。打包文件是 arXiv 预印本 2512.02517（`pdfs/2026-arXiv-SkyMoE-Liu.pdf`），不是 AAAI 出版社付费墙正式版；OJS 37653 的正式 PDF 仍未打包。
- RS-LLaVA 已收入 MDPI 官方开放获取 PDF（`pdfs/2024-RemoteSensing-RS-LLaVA-Bazi.pdf`，*Remote Sensing* 16(9):1477，CC BY 4.0）。

## 未收入全文的 2 篇

| 论文 | 说明 | 页面 |
| --- | --- | --- |
| ExpertsRS（Sun et al.，*Big Earth Data*, 2026） | Taylor & Francis 可能需订阅，未发现开放预印本 | [Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178) |
| SPEXT（NeurIPS 2026） | 当时仅有海报页，无论文 PDF / arXiv | [NeurIPS poster](https://neurips.cc/virtual/2026/poster/153724) |

## 文件清单

PDF 的完整条目、开源地址与一句话提要见 `papers.json`；面向写作 agent 的分层索引见 `catalog/INDEX.md` 与 `catalog/index.json`。本包只收文献 PDF，不含数据集本身。
