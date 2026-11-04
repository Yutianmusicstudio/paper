# 数据交接 — mpa-bibliometric (F10)

日期：2026-11-03/04。检索与导出均已完成，文件在本目录下。

## 文件

| 文件 | 内容 | 条数 |
|---|---|---|
| `data/wos/wos_mpa_001-500.txt` | WoS Core Collection，Plain Text，Full Record and Cited References，记录 1–500 | 500 |
| `data/wos/wos_mpa_501-511.txt` | 同上，记录 501–511 | 11 |
| `data/scopus/scopus_mpa_all.csv` | Scopus CSV，45 列全字段（含 Abstract、References、Funding） | 513 |
| `protocol/search-protocol.md` | 两库检索式、导出设置、计数、纳排标准、新颖性核查 | — |

## 关键数字

- WoS 511（Article 389、Review 37、Early Access 21；其余 57 条为会议摘要、会议论文、书评、社论、勘误等）；年份 1962–2026；432 条有摘要，474 条有 CR
- Scopus 513（Article 421、Review 36、Book chapter 24、Conference paper 14、其余 18）；年份 1940–2026；513 条有摘要，491 条有 References
- DOI 重合 370；合并去重后粗估 600–630 条
- 比大纲预估（初检 600–1,000、纳入 400–700）偏低，纳入估计 450–520

## 开工前必须处理的事

1. **新颖性**：Rumiantsev (2026) *Social Sciences & Humanities Open*, doi:10.1016/j.ssaho.2026.103189，WoS 2,159 篇音乐表演研究计量，摘要明确写 MPA 与 wellbeing 为主导主题。大纲"查重 🟢（10-26）"已过时；`paper2/catalog-review` 对 F10 的评级是 🟡，建议并入 H10 或 A-AGENDA。若单独成篇，RQ3 内容编码必须是主体，标题与引言第一段要改。
2. **时间起点**：WoS 最早 1962，Scopus 最早 1940；标题"1985–2026"要么改，要么在方法里说明截断理由。
3. **编码可行性**：WoS 79 条无摘要；量表名很多摘要不写，RQ3 的测量工具编码需查全文。
4. **双人编码**：若第二编码者是 AI，须在方法与声明中写明；多数期刊不接受 AI 为编码者。
5. **路线**：作者未定。若走 Elsevier 零成本线，SSAHO（Q2，GT Read & Publish 覆盖）比 The Arts in Psychotherapy 范围更对口。
