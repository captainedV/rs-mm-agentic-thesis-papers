# 多模态 + Agentic 遥感开题论文包

本仓库是夏浩翔硕士开题用的**私有文献包**，收录 2024.11–2026.11 前后「多模态 / 视觉语言模型 + 工具调用或多智能体方法 + 遥感 / 地球观测」方向的开放获取论文 PDF。整理日期：2026-11-10（Asia/Shanghai）。

仓库为私有，仅供本人开题与后续研究使用。其中 PDF 均来自 arXiv、CVF Open Access、ICLR / NeurIPS / ACL 等会议开放渠道或 Copernicus 开放档案，**不是**出版社付费墙正式版的镜像，请勿公开分发或当作官方抽印本。

配套综述与数据集 / benchmark 笔记写在 Notion 草稿页：[多模态 + Agentic 遥感开题文献综述（2024.11–2026.11）](https://app.notion.com/p/4148f718d0be817b8d15fbc12388fdae?pvs=204)。

## 仓库内容

- `pdfs/`：57 篇已核对的开放获取 PDF，文件名格式为 `YYYY-Venue-ShortTitle-FirstAuthor.pdf`
- `papers.json`：机器可读目录（标题、会址、arXiv、开源地址、摘要要点）
- `missing-pdfs.md`：未能收入的 4 篇及正式版改用预印本的说明
- `SURVEY.md`：开题用简明综述与选题切入点

## 建议优先阅读

1. Earth-Agent（ICLR 2026）
2. GeoMMBench / GeoMMAgent（CVPR 2026）
3. DORA（NeurIPS 2026）
4. SimCRAFT（EMNLP 2026）
5. GeoLLM-Squad（IGARSS 2025）
6. EarthDial（CVPR 2025）
7. TEOChat（ICLR 2025）
8. ThinkGeo（仅作 arXiv:2505.23752 预印本与基准；不以 ICLR / CVPR 主会论文引用）

## 引用时请注意

- **OpenEarthAgent**（Shabbir，工具调用）与 **OpenEarth-Agent**（Zhao，工具创造）是两篇不同的论文，不要混用。
- GeoAssistant 在交接清单中记为 ICLR 2026 已撤稿，本仓库不收录，也不作为录用论文引用。ThinkGeo 的 ICLR 2026 投稿按交接说明处理，只保留上述预印本。
- UnivEARTH、HiRS-Agent 的 arXiv 注释中出现过 ACL 2026 Findings、ACM MM 2026 等会址，尚未独立复核会议页，文件名仍标为 arXiv，不升格会址。
- 若干 IEEE / ISPRS JPRS / AAAI / PMLR 正式版当时未能下载或可能需订阅，已改用对应 arXiv 或会议开放 PDF，详见 `missing-pdfs.md`。

## 未收入全文的 4 篇

| 论文 | 说明 | 页面 |
| --- | --- | --- |
| ExpertsRS（Sun et al.，*Big Earth Data*, 2026） | Taylor & Francis 可能需订阅，未发现开放预印本 | [Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178) |
| SkyMoE | AAAI OJS 下载接口当时只返回 HTML，未发现对应 arXiv | [AAAI OJS 37653](https://ojs.aaai.org/index.php/AAAI/article/view/37653) |
| SPEXT（NeurIPS 2026） | 当时仅有海报页，无论文 PDF / arXiv | [NeurIPS poster](https://neurips.cc/virtual/2026/poster/153724) |
| RS-LLaVA（Bazi et al.，*Remote Sensing* 16(9):1477, 2024） | MDPI 一般为开放获取，当时请求 PDF 返回 403 | [MDPI](https://www.mdpi.com/2072-4292/16/9/1477) |

## 文件清单

PDF 的完整条目、开源地址与一句话提要见 `papers.json`。本包只收文献 PDF，不含数据集本身。
