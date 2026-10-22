# 查重（查新）流程

目的：在开题前 1 小时内判断一个 idea 是 🟢 空白、🟡 有近邻、🔴 已被占。结果记入 `docs/idea-board.md`。

## 1. 把 idea 拆成三要素
- **对象**：人群 / 职业 / 场景（音乐治疗师、器乐学生、MPA）
- **技术**：AI、生成式 AI、VR、可穿戴、App、EEG、远程
- **论文类型**：范围综述、系统综述、文献计量、问卷、实验、概念

## 2. 两轮检索
**第一轮（宽）**：`<对象> <技术> (scoping review OR systematic review OR bibliometric) 2024 2025 2026`
**第二轮（窄）**：把第一轮发现的最近邻论文的题名关键词、作者再搜一次，并搜注册库：PROSPERO、OSF、ClinicalTrials.gov。

每个 idea 至少 2 次搜索，发现近邻后至少再追 1 次。中文选题补搜知网关键词。

## 3. 判定规则
| 判定 | 条件 | 动作 |
|---|---|---|
| 🔴 已被占 | 近 2 年有同类型、同对象、同技术的论文发表于同行评审期刊 | 放弃，或改论文类型 / 对象 |
| 🟡 有近邻 | 有相邻论文但类型、对象或角度不同；或只有会议摘要、预印本、学位论文、方案 | 写明差异点，2 个月内投出 |
| 🟢 空白 | 两轮检索均未发现同类型论文，只有零散原始研究 | 立即预注册占位（OSF / PROSPERO），再开题 |

## 4. 记录格式（粘贴到 idea-board）
```
### <编号> <判定> <题目>
- 近邻：<论文 1（年份、期刊、样本/篇数）>；<论文 2>
- 空白：<一句话>
- 建议角度：<一句话>
- 目标期刊：<3 本>
- 下一步：<注册 / 检索 / 伦理>
```

## 5. 工具
- 本仓库 skill：`/novelty-check <idea>` 自动跑上述两轮并输出记录格式。
- 当前环境只能用网页搜索。若要用 OpenAlex、Crossref、PubMed、Semantic Scholar 的 API 做更可靠的查重，需在环境设置的 Network access 里加入以下域名：
  `api.openalex.org`、`api.crossref.org`、`eutils.ncbi.nlm.nih.gov`、`api.semanticscholar.org`、`export.arxiv.org`。
  加入后可改用 `/search-lit` 与 `/verify-refs`。

## 6. 复查节奏
- 🟢 的 idea 开题后每月复查一次，直到投稿。
- 🟡 的 idea 两周复查一次。
- 投稿前最后一次复查，并在引言中引用所有近邻论文说明差异。
