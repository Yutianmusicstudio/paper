# 稿件大纲：Reporting quality of technology-delivered music intervention trials: a systematic audit against the revised Reporting Guidelines for Music-Based Interventions and CONSORT-EHEALTH

- **Slug**：tech-music-reporting-quality（看板编号 H4）
- **类型**：方法学系统综述 / 报告质量审计（meta-research）
- **目标期刊**：1) Integrative Medicine Research（Elsevier，RG-MBI 2025 更新版发表地） 2) JMIR Formative Research 3) Frontiers in Psychology, Health Psychology
- **字数上限**：Integrative Medicine Research 约 5,000 词正文，表图合计 ≤ 6（投稿前复核）
- **报告规范**：PRISMA 2020（方法学综述适配版）
- **预注册**：PROSPERO 优先；若因"非健康结局"被拒，转 OSF Registries
- **伦理**：不需要
- **查重状态**：🟢（2026-10-26；Robb 2018 基线综述、2024 外科预录音乐 TIDieR 综述均不针对技术介导；RG-MBI 2025 尚未被用于任何审计）

## 研究缺口（≤ 3 句）
Robb 等 2018 年审计 187 项音乐干预研究，发现不到一半报告了理论、干预者资质、治疗保真度和场景；2025 年 RG-MBI 更新为 12 项并建议与 CONSORT 系列联用，但尚无任何领域用新版做过审计。技术介导的音乐干预（远程、App、VR、可穿戴自适应、AI 生成音乐）在过去十年快速增加，其报告既要满足音乐干预的内容要素，又要满足数字健康干预的技术要素（CONSORT-EHEALTH），两套要求叠加，漏报风险最高，却从未被系统检查。读者无法复制这些干预，综述作者无法合并它们。

## 研究问题
- RQ1：2015–2026 年发表的技术介导音乐干预对照试验，对 RG-MBI 2025 的 12 项和 CONSORT-EHEALTH 技术相关条目的逐项报告率是多少？
- RQ2：报告质量随时间、期刊学科（音乐治疗 / 医学 / 数字健康 / 工程与人机交互）、试验注册、资助、技术类型如何变化？
- RQ3：哪些要素最常缺失（预期：音乐内容描述、剂量参数、保真度、技术故障与人工参与程度），对复现与证据合成意味着什么？

## 方法概要

### 纳入标准
- 随机或非随机对照试验，2015-01-01 至检索日，同行评审期刊，任何语言
- 干预：音乐为主要治疗成分
- **技术介导操作定义**（预注册）：满足任一即可——(a) 通过远程视频、App、网页、VR/AR 平台交付，干预者与参与者不在同一物理空间；(b) 音乐由算法生成、推荐或根据生理 / 行为信号实时调整；(c) 由社交机器人或虚拟代理交付
- 排除：仅用耳机播放预录音乐且无 (a)(b)(c) 特征；方案论文；会议摘要

### 检索
- PubMed、PsycINFO、Scopus、Web of Science、CINAHL、Cochrane CENTRAL、IEEE Xplore、ACM Digital Library、RILM
- 检索式骨架：`(music* OR singing OR "rhythmic auditory") AND (telehealth OR tele* OR online OR remote OR app OR smartphone OR mobile OR web-based OR "virtual reality" OR "augmented reality" OR wearable OR biofeedback OR adaptive OR "artificial intelligence" OR "machine learning" OR generat* OR robot*) AND (trial OR randomi* OR controlled)`
- 补充：H3 注册库数据集中已发表的技术介导试验反查；纳入文献引文追踪

### 评价工具
1. **RG-MBI 2025**：12 项，每项评 Reported / Partially / Not reported，按 Robb 等的释义指南判定
2. **CONSORT-EHEALTH**：选取技术相关子条目（干预的访问方式、交付模式、功能、使用参数、人工参与程度、提示与提醒、共干预、技术故障、使用数据报告等，约 12–15 个子条目），同样三级评分
3. 辅助记录：试验注册、CONSORT 流程图有无、资助、国家、期刊类别、技术类型、人群、样本量

### 流程
- 双人独立筛选与评分；分歧讨论，第三人仲裁；报告 kappa
- 评分前以 5 篇试验做校准
- 向通讯作者索取补充材料不作为评分依据（评的是已发表报告）

### 分析
- 逐项报告率与 95% CI；总报告分（RG-MBI 0–24，EHEALTH 0–30）分布
- 线性回归：总分 ~ 发表年 + 期刊类别 + 注册 + 资助 + 技术类型
- 与 Robb 2018 基线的可比项对照，判断十年有无改善
- 图：逐项报告率热图（按技术类型分面）、总分年度趋势散点、期刊类别箱线图

### 预计规模
- 初检 2,000–3,500 条，纳入 40–80 项试验

## 预期贡献
- 实践：给技术介导音乐干预研究者一份"最常漏报清单"，以及 RG-MBI + CONSORT-EHEALTH 联用的操作示范
- 理论 / 方法：首次量化数字化转向带来的报告缺口，为 RG-MBI 作者群提供新版清单的实证反馈，可能推动针对数字音乐干预的扩展条目
- 系列：与 H3（领域地图）、H10（测量工具）构成方法学三部曲；H3 数据集直接为本文提供试验来源

## 风险与对策
- PROSPERO 可能以"无健康结局"拒收 → 同时准备 OSF 注册
- 工程 / 人机交互期刊的试验常无 CONSORT 结构 → 预先定义"不适用"规则，并作敏感性分析排除
- 评分主观 → 校准集 + 释义指南 + kappa；评分表随补充材料公开
- 纳入量不足 40 → 放宽到 2010 年起，或纳入单臂可行性试验作次要分析

## 配套 skill 与工具
| 阶段 | 本仓库 skill | 外部工具 |
|---|---|---|
| 注册 | — | PROSPERO / OSF；RG-MBI 2025 清单与释义指南；CONSORT-EHEALTH 清单 |
| 检索 | `/search-lit`（API 放行后）；`/fulltext-retrieval` | 九个数据库；Zotero 去重 |
| 筛选 | 上游 `sr-screener`（可选） | Rayyan |
| 评分 | `/check-reporting`：可对每篇试验跑一次逐项初评（覆盖 CONSORT、TIDieR；RG-MBI 需自建条目表），人工核对后定分 | 评分表 Excel，kappa 用 R `irr` |
| 分析与图 | 会话内 `dataviz` skill | R ggplot2 热图 |
| 写作 | `/paper-writer`（Systematic Review 类型，PRISMA 2020） | PRISMA 流程图生成器 |
| 质控 | `/check-reporting`（对本文自己跑 PRISMA 2020）→ `/verify-refs` → `/self-review` → `/humanize` → `/polish-language` | — |
| 投稿 | `/find-journal` 复核；`/manage-refs` 出 Vancouver；`/sync-submission` | Elsevier Editorial Manager |
| 返修 | `/revise` | — |

## 时间表
| 周 | 任务 | 状态 |
|---|---|---|
| 1 | 操作定义与评分手册定稿；PROSPERO / OSF 注册 | 待开始 |
| 2 | 九库检索与导出；去重 | |
| 3–4 | 题录筛选；全文获取；全文筛选 | |
| 5 | 5 篇校准；评分手册修订 | |
| 6–8 | 双人评分全部试验；仲裁；kappa | |
| 9 | 分析；热图与趋势图 | |
| 10 | Methods、Results 初稿 | |
| 11 | Introduction、Discussion、Abstract | |
| 12 | 质控五步；语言两轮 | |
| 13 | 投稿 Integrative Medicine Research；记录 submission-log | |
