# 未入库 / 目录外 PDF 审计

> 审计日期：2026-11-21（Asia/Shanghai）。官方目录以 `papers.json` 的 **61 条**为准。

## 结论

- `papers.json` 有 61 条，其中 59 条有 `local_pdf`，2 条没有全文（ExpertsRS、SPEXT）。
- `pdfs/` 实际有 59 个 PDF，与 `papers.json` 的 `local_pdf` **一一对应**：没有“JSON 有、文件缺”，也没有“文件有、JSON 无”。
- 仓库内 `pdfs/` 之外没有发现 `.pdf` 文件。
- 因此当前**没有需要并入主目录的零散 PDF**。

## 两条“有卡片、无全文”的条目

它们仍属于官方目录，不是“目录外文献”；卡片只保留元数据与正式页链接：

| id | 状态 | 处理 |
| --- | --- | --- |
| `expertsrs` | Taylor & Francis 可能需订阅；未发现开放预印本 | 元数据卡片；不写方法细节/数字；见 [`papers/expertsrs.md`](papers/expertsrs.md) |
| `spext` | NeurIPS 2026 仅有海报页；无论文 PDF/arXiv | 元数据卡片；不写方法细节/数字；见 [`papers/spext.md`](papers/spext.md) |

## 规则

1. 不把仓库或本地工作目录里未进入 `papers.json` 的 PDF 偷偷并入主目录。
2. 若发现这类文件，先在本页登记：路径、标题/首作者（若能识别）、来源、是否开放获取、建议归类、待确认事项。
3. 只有确认进入官方目录（先更新 `papers.json`）后，才建卡片并加入 `INDEX.md` / cluster。
4. 不改 `pdfs/` 已有文件名；不打包付费墙正式版。
5. 发现“同名不同论文”（如 OpenEarthAgent vs OpenEarth-Agent）时，必须分别登记，不得合并。

## 本次审计命令（可复现）

```bash
python3 - <<'PY'
import json, os
d=json.load(open('papers.json'))
listed={p['local_pdf'] for p in d['papers'] if p.get('local_pdf')}
files={os.path.join('pdfs',f) for f in os.listdir('pdfs') if f.lower().endswith('.pdf')}
print('listed',len(listed),'files',len(files))
print('in json not file',listed-files)
print('file not json',files-listed)
PY
find . -name '*.pdf' -not -path './pdfs/*' -not -path './.git/*'
```

本次输出：`listed 59 files 59`；两个差集均为空；`find` 无结果。
