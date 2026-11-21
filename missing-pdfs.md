# 未能打包的 PDF

日期：2026-11-10（Asia/Shanghai）
原则：只使用开放获取来源（arXiv、CVF、ICLR/NeurIPS/PMLR/ACL Anthology、ISPRS Archives 等）。不下载 IEEE/Springer/Elsevier/Taylor & Francis 付费墙全文。

## 完全没有打进压缩包的条目

| 论文 | 会址 | 原因 | 可访问页面 |
|---|---|---|---|
| An LLM-based multi-agent system for remote sensing analysis（ExpertsRS），Sun et al. | Big Earth Data, 2026 | Taylor & Francis 可能需订阅；未发现开放预印本 PDF | https://www.tandfonline.com/doi/full/10.1080/20964471.2025.2600178 |
| SPEXT: A Decoupled Multi-Spectral Foundation Model… | NeurIPS 2026 | 交接清单仅给出海报页，无论文 PDF 或 arXiv | https://neurips.cc/virtual/2026/poster/153724 |

## 已补入的官方开放获取 PDF

RS-LLaVA（Bazi et al.，*Remote Sensing* 16(9):1477）的 MDPI 官方开放获取 PDF 已打包为 `pdfs/2024-RemoteSensing-RS-LLaVA-Bazi.pdf`（CC BY 4.0）。文章页：https://www.mdpi.com/2072-4292/16/9/1477 ；DOI：https://doi.org/10.3390/rs16091477

## 已用开放预印本/会议 OA 替代、未打包出版社付费墙正式版

这些条目**已经**以 arXiv 或会议开放 PDF 打入压缩包，不视为缺失全文；仅说明出版社正式版未下载。

- EarthGPT、RemoteCLIP、Change-Agent、RescueADI：IEEE TGRS 正式版可能需订阅；已打包对应 arXiv。
- RingMo-Agent：IEEE TPAMI DOI 10.1109/tpami.2026.3718699 可能需订阅；已打包 arXiv:2507.20776。
- SkyEyeGPT、RSGPT：ISPRS JPRS DOI 可能需订阅；已打包 arXiv。
- GeoLLM-Squad：IEEE IGARSS 2025 DOI 可能需订阅；已打包 arXiv:2501.16254。
- RS-ChatGPT：IEEE IGARSS 2024 正式版可能需订阅；已打包 arXiv:2401.09083。
- RSVQA：IEEE TGRS 2020 正式版可能需订阅；已打包预印本 arXiv:2003.07333。
- GeoPixel：ICML 2025 正式入口为 PMLR https://proceedings.mlr.press/v267/shabbir25a.html ；本环境未能下载 PMLR PDF，已改用 arXiv:2501.13925。
- RemoteReasoner、EarthVQA：AAAI 正式页可核会址，OJS download 接口返回 HTML；已改用对应 arXiv。
- SkyMoE：AAAI OJS 37653 正式 PDF 仍未打包。已打包的是 arXiv 预印本 2512.02517（`pdfs/2026-arXiv-SkyMoE-Liu.pdf`），不是出版社付费墙正式版。arXiv：https://arxiv.org/abs/2512.02517 ；AAAI 页：https://ojs.aaai.org/index.php/AAAI/article/view/37653

## 撤稿（不作为录用论文引用，亦未单独追求 PDF）

- GeoAssistant，OpenReview https://openreview.net/forum?id=xvRpSz6rr6 ，交接清单写明 ICLR 2026 已撤稿。
- ThinkGeo 的 ICLR 2026 投稿已撤稿；本包收录的是 arXiv:2505.23752 预印本，且不以 ICLR 或 CVPR 主会论文引用。
