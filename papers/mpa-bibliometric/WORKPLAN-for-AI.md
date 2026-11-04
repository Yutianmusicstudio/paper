# F10 工作包：交给执行 AI 的完整任务说明

论文：**What has music performance anxiety research measured, designed and studied? A bibliometric and content analysis of six decades of literature**
日期：2026-11-04。本文件自成一体，执行者不需要本仓库的其他文件；若能访问仓库，`outline.md` 与 `protocol/` 是补充背景。

---

## 0. 一句话任务
对约 500 篇音乐表演焦虑（MPA）期刊文献做两件事：用 Bibliometrix 跑标准文献计量作背景，再逐篇编码测量工具、研究设计、人群与技术介入作主体，写成一篇 5,000–6,000 词的英文论文，投 MDPI *Behavioral Sciences*（备选见第 8 节）。

## 1. 你会拿到的输入
| 文件 | 内容 |
|---|---|
| `data/wos/wos_mpa_001-500.txt` | Web of Science 核心合集，Plain Text，Full Record and Cited References，记录 1–500 |
| `data/wos/wos_mpa_501-511.txt` | 同上，记录 501–511 |
| `data/scopus/scopus_mpa_all.csv` | Scopus 全字段 CSV，513 行 45 列 |
| `protocol/search-protocol.md` | 两库检索式、导出设置、计数、纳排标准 |

检索式（WoS）：`TS=("music performance anxiety" OR "musical performance anxiety" OR (("performance anxiety" OR "stage fright") NEAR/3 (music* OR musician* OR instrumentalist* OR singer* OR vocalist* OR pianist* OR orchestra* OR conservator*)))`，检索日 2026-11-03。Scopus 等价式见协议。

## 2. 硬约束（违反任何一条论文作废）
1. **不编造任何参考文献或数据。** 每条引用必须有 DOI 或可检索的完整信息；不确定的标 `[VERIFY]` 留给作者核。
2. **第二编码者必须是人。** 你做全量初编码并为每条编码写出依据句；作者安排一名人类独立编码随机 20%，由你计算 kappa。方法中写明"AI 辅助初编码，人工独立复核 20%"。
3. **引言第一段必须引用并区分** Rumiantsev (2026), *Social Sciences & Humanities Open*, doi:10.1016/j.ssaho.2026.103189（音乐表演研究整体计量，MPA 为主导主题）。本文差异点：只看 MPA，且逐篇编码测量工具 / 设计 / 人群 / 技术。DOI 需作者再核一次。
4. **数据不得切成多篇。** 本数据集只支撑本文一篇。
5. 稿件英文、美式拼写；与作者沟通用中文。
6. 所有脚本、编码表、原始输出保存在论文目录，随论文作补充材料公开。

## 3. 第一步：合并、去重、纳排（预计 1 天）
```r
# R ≥ 4.3
install.packages(c("bibliometrix","tidyverse","janitor","irr","writexl"))
library(bibliometrix); library(tidyverse)
wos1 <- convert2df("data/wos/wos_mpa_001-500.txt", dbsource="wos", format="plaintext")
wos2 <- convert2df("data/wos/wos_mpa_501-511.txt", dbsource="wos", format="plaintext")
wos  <- rbind(wos1, wos2)                       # 期望 511 行
sco  <- convert2df("data/scopus/scopus_mpa_all.csv", dbsource="scopus", format="csv")  # 期望 513 行
M    <- mergeDbSources(wos, sco, remove.duplicated=TRUE)   # 期望约 600–630 行
```
- 记录每一步行数，画 PRISMA 式流程图（检索 → 去重 → 题录筛选 → 纳入）。
- 题录级排除规则：非期刊文献（会议摘要、书章、书评、社论、勘误、信件）；非音乐情境的表演焦虑（体育、公开演讲、性功能）；仅在参考文献或作者单位中命中。导出 `data/screening_log.xlsx`，每条排除写原因。
- 预期纳入 450–520 篇。时间跨度按实际（WoS 最早 1962），题目用 six decades。
- 注意：Scopus 与 WoS 合并后关键词字段（DE / ID）与引用字段（CR）格式不一，Bibliometrix 的共被引分析只用 WoS 子集；在方法里写明。

## 4. 第二步：文献计量背景分析（预计 1 天）
```r
res <- biblioAnalysis(M); summary(res, k=20)
# 年度产出与增长率；来源与 Bradford 核心区；作者 Lotka；国家合作
NetMatrix <- biblioNetwork(M, analysis="co-occurrences", network="keywords", sep=";")
networkPlot(NetMatrix, n=50, Title="Keyword co-occurrence", type="fruchterman")
thematicMap(M, field="DE", n=250, minfreq=5)
thematicEvolution(M, field="DE", years=c(2005, 2015), n=250, minFreq=5)   # 三期：≤2005 / 2006–2015 / 2016–2026
```
输出图：F1 年度产出；F2 国家合作地图；F3 关键词共现网络；F4 主题演化桑基图；F5 主题地图。保存 300 dpi PNG 至 `figs/`。
这部分只占结果的三分之一，写作时与 Rumiantsev 2026 对照，突出 MPA 子领域的特点，不要堆指标。

## 5. 第三步：内容编码（主体，预计 5–7 天）

### 5.1 编码表（`data/coding_sheet.xlsx`，一行一篇）
| 字段 | 取值 | 说明 |
|---|---|---|
| id, doi, year, journal, title | 自动 | 来自 M |
| design | cross-sectional survey / intervention RCT / intervention non-randomized / single-arm or pilot / qualitative / mixed / case study / measurement-validation / review-systematic / review-narrative / theoretical / other | 单选 |
| population | students-tertiary / students-school / professional / amateur / mixed / teachers / children-adolescents / other | 可多选 |
| n | 整数或 NA | 样本量 |
| instrument_mpa | K-MPAI-26 / K-MPAI-40 / K-MPAI-short / PAI / MPAI-A / PAQ / PRCP / STAI / other-named / none / unclear | 可多选；写出原文量表名 |
| instrument_physio | HRV / HR / cortisol / EDA-SCL / EEG / fNIRS / respiration / other / none | 可多选 |
| technology | VR-AR / biofeedback / app-online / AI / wearable / telehealth / none | 可多选 |
| intervention_type | CBT / exposure / mindfulness-relaxation / biofeedback / beta-blocker-pharma / music-therapy / education-program / other / NA | 仅干预研究 |
| evidence_sentence | 文本 | 支撑编码的原文句，必须有 |
| full_text_checked | yes / no | 摘要不足时是否查了全文 |
| coder | AI / human | |

### 5.2 流程
1. 先用题录与摘要编码全部纳入文献；摘要缺失或未写量表名的（预计 150–250 篇）标 `full_text_checked=no`，交作者用 Georgia Tech 图书馆权限取全文，再补编码。
2. 从纳入文献中随机抽 20%（固定随机种子 20261104），生成 `data/coding_sheet_human.xlsx` 给人类第二编码者，不含你的编码。
3. 回收后用 `irr::kappa2` 分字段算 Cohen's kappa，目标 ≥ 0.80；低于 0.70 的字段修订编码手册后重编该字段。
4. 分歧由第一作者裁决，记录在 `data/adjudication_log.xlsx`。

### 5.3 分析
- 各字段频数与比例，总体及分三期；堆叠条形图 F6（测量工具 × 时期）、F7（设计 × 时期）、F8（技术介入 × 时期）
- 交叉表：生理指标研究中并用标准量表的比例；技术介入研究中使用验证量表的比例；干预研究中的设计分布
- 每个结果配一句"这意味着什么"的解读草稿，供讨论使用

## 6. 第四步：写作（预计 4–5 天）
结构按 MDPI *Behavioral Sciences*：Abstract（≤ 200 词，结构化）· 1 Introduction · 2 Materials and Methods · 3 Results · 4 Discussion · 5 Conclusions · Author Contributions · Funding · Data Availability · Conflicts of Interest · AI 使用声明 · References（MDPI 数字编号格式）。
- Introduction 第一段引 Rumiantsev 2026 并说明差异；第二段引 2025–2026 年 MPA 干预综述对"测量不标准化、设计薄弱"的批评（Nicholl & Abbott 2026 *Psychology of Music*；MDPI *Behavioral Sciences* 2025 年 MPA 干预系统综述）；第三段提出三个 RQ。
- Methods 报告规范：BIBLIO 清单（Montazeri et al. 2023）作补充材料；PRISMA 式流程图；编码手册与 kappa。
- Results 先编码（主体），后计量（背景）。
- Discussion 三段：主要发现与 Rumiantsev 及干预综述对照；对研究者与教育者的实践含义（选量表、设计）；局限（数据库覆盖、英文偏倚、编码依赖摘要与全文可得性、AI 辅助编码）。
- Conclusions ≤ 150 词。
- 预计表 3 张、图 8 张；MDPI 无硬性上限。

## 7. 第五步：质控（预计 2 天）
1. 逐条核对参考文献 DOI（CrossRef）；无法核实的标 `[VERIFY]` 交作者。
2. 按 BIBLIO 清单与 PRISMA 2020 逐项自查。
3. 以审稿人视角自审：Rumiantsev 重叠、AI 编码、无摘要文献处理、Scopus / WoS 字段差异，这四点必须在正文有回应。
4. 去 AI 腔与语言校对（美式拼写、缩写一致、数字格式）。
5. 生成投稿包：manuscript.docx、figures、supplementary（编码手册、编码表、BIBLIO 清单、PRISMA 图、R 脚本）、cover letter、推荐审稿人 3–5 名（发过 MPA 研究或文献计量的学者，不含本文引用过的合作者）。

## 8. 期刊路线（作者定，默认 A）
| 路线 | 期刊 | 费用（2026-11 核实） | 首次决定 | 注意 |
|---|---|---|---|---|
| A | *Behavioral Sciences*（MDPI），Q2–Q3 | 约 2,200 CHF，Georgia Tech 无 MDPI 折扣 | 约 3 周 | 2025 年刊过 MPA 系统综述；MPA 干预特刊已截止，走常规栏目；投稿前给编辑发摘要询问 |
| B | *The Arts in Psychotherapy*（Elsevier 混合），Q2–Q3 | 0，Georgia Tech 的 Elsevier Read & Publish 只覆盖混合刊 | 6–10 周 | 范围偏艺术治疗，先询问 |
| 不建议 | *Social Sciences & Humanities Open* | 全开放获取刊，不在 GT 协议内，需付费 | — | Rumiantsev 刚发在此，重叠质疑最可能 |

## 9. 时间表
| 天 | 任务 |
|---|---|
| 1 | 合并去重、纳排、PRISMA 流程图 |
| 2 | 计量分析与 F1–F5 |
| 3–7 | 全量初编码；生成人类 20% 样本；列出需全文的清单交作者 |
| 8–9 | 补全文编码；kappa；编码分析与 F6–F8 |
| 10–14 | 全文写作 |
| 15–16 | 质控、投稿包 |

## 10. 需要作者本人做的事（请在对应时点提醒）
- 第 3 天：取需全文文献的 PDF（150–250 篇）
- 第 3 天：把 `coding_sheet_human.xlsx` 交给人类第二编码者，约 3–4 小时工作量
- 第 10 天前：决定路线 A 或 B；A 需准备约 1.8 万元
- 第 15 天：签作者贡献（CRediT）、利益冲突、AI 使用声明
- 投稿前：再核一次 Rumiantsev 2026 的 DOI 与卷期

## 11. 已知风险与应对
| 风险 | 应对 |
|---|---|
| 审稿人认为与 Rumiantsev 重叠 | 引言与讨论各一段对照；结果以编码为主体，计量只占三分之一 |
| 无摘要文献多，编码不全 | 报告 full_text_checked 比例；无法获取全文的编码为 unclear 并报告数量 |
| kappa 不达标 | 修订编码手册后重编该字段，报告两轮结果 |
| 审稿人质疑 AI 编码 | 方法与声明如实写；人工 20% 复核 + kappa 是业内可接受的做法 |
| 初审退稿 | 投稿前询问编辑；备选路线 B |
