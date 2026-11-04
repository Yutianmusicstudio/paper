# 检索协议 — mpa-bibliometric (F10)

检索日：2026-11-03（Georgia Tech Library 机构访问）

## 1. Web of Science Core Collection（主库）

- 入口：Advanced Search，Editions = All（以 GT 订阅为准，导出时记录实际 edition 列表）
- 时间：建库至检索日，不加 PY 限制
- 检索式（原样复制）：

```
TS=("music performance anxiety" OR "musical performance anxiety" OR (("performance anxiety" OR "stage fright") NEAR/3 (music* OR musician* OR instrumentalist* OR singer* OR vocalist* OR pianist* OR orchestra* OR conservator*)))
```

- 结果：**511 条**（全部文献类型；2026-11-03 实测）
- 限定 `#1 AND DT=(Article OR Review)` 后：**459 条**（2026-11-03 实测）
- 导出设置：Export → Plain Text（或 Tab-delimited）→ Record Content = "Full Record and Cited References"，每批 ≤ 500 条
  - 批 1：records 1–500 → `data/wos/wos_mpa_001-500.txt`（已导出 2026-11-03，500 条，3.19 MB）
  - 批 2：records 501–511 → `data/wos/wos_mpa_501-511.txt`（已导出 2026-11-03，11 条）
  - 导出的是 #1 全部 511 条（不限文献类型），以便在清洗阶段按 DT 排除并记录 PRISMA 数字

## 2. Scopus（补充 / 敏感性分析）

- 入口：Advanced search
- 等价式（NEAR/3 → W/3）：

```
TITLE-ABS-KEY("music performance anxiety" OR "musical performance anxiety" OR (("performance anxiety" OR "stage fright") W/3 (music* OR musician* OR instrumentalist* OR singer* OR vocalist* OR pianist* OR orchestra* OR conservator*)))
```

- 结果：**513 条**（2026-11-03 实测；Article 421、Review 36、Book chapter 24、Conference paper 14、Book 5；英文 497）
- 导出：CSV，勾选全部字段（Citation information + Bibliographical information + Abstract & keywords + Funding details + Other information，含 References）
- 文件：`data/scopus/scopus_mpa_all.csv`
- 状态：**已导出**（作者本人于 Safari 登录后导出，2026-11-04 02:08 UTC；原始文件名 export_cc8ad235-…csv，5.97 MB）。513 行、45 列；Abstract 513、References 491、DOI 472、Author Keywords 402、Index Keywords 161；年份 1940–2026；Document Type：Article 421、Review 36、Book chapter 24、Conference paper 14、Book 5、Erratum 3、Note 3、Editorial 3、Letter 2、Short survey 2

## 2b. 两库重合（粗估，2026-11-03）

- WoS 有 DOI 412 条，Scopus 有 DOI 472 条，DOI 完全重合 370 条
- 按 DOI 或题名匹配，Scopus 513 条中约 397 条已在 WoS 内，Scopus 独有约 116 条
- 合并去重后估计 **约 600–630 条**（正式去重以 Bibliometrix `mergeDbSources` 为准）

## 3. 纳入 / 排除（题录级，双人核对）

- 纳入：期刊论文（Article、Review，含 Early Access）；语言不限
- 排除：会议摘要、书评、勘误、社论；非音乐情境的表演焦虑（体育、公开演讲、性功能）；仅在参考文献或作者单位中命中的记录
- 记录每条排除原因；PRISMA 式流程图

## 4. 查重与新颖性（2026-11-03 核实）

- Rumiantsev (2026). Music performance research: a bibliometric analysis of trends, themes, and knowledge structures. *Social Sciences & Humanities Open*, doi:10.1016/j.ssaho.2026.103189（Crossref 核实；SSRN 预印本 10.2139/ssrn.6473520）。WoS 2,159 篇 1966–2025，共词 + 共被引 + 主题图；摘要明确写 MPA 与 wellbeing 为**主导主题**。
- 结论：纯 Bibliometrix/VOSviewer 的 MPA 计量与之重叠；本文的差异点只能是 RQ3 的内容编码（测量工具、设计、人群、技术介入）。引言第一段必须引用并区分。
- 大纲"查重 🟢（2026-10-26）"已过时；`paper2/catalog-review` 对 F10 的审查评级为 🟡，建议并入 H10 或 A-AGENDA。
