# 稿件大纲：Four decades of music performance anxiety research: a bibliometric analysis of themes, measures and study designs (1985–2026)

- **Slug**：mpa-bibliometric（看板编号 F10）
- **类型**：文献计量 + 内容编码（Bibliometrix / VOSviewer）
- **目标**：Q3 以上、高接受率、快。两条路线见下节，投稿前由作者定
- **字数**：MDPI 无硬上限，建议 5,000–6,000 词，图 6 表 3；Elsevier 期刊约 6,000 词
- **报告规范**：BIBLIO 清单（Montazeri et al., 2023，文献计量报告指南）+ PRISMA 流程图记录检索与纳入
- **预注册**：OSF（检索式、纳入标准、分析计划；一天可完成）
- **伦理**：不需要
- **查重**：🟢（2026-10-26；仅有 Medicine 2024 音乐治疗与焦虑计量、2025 手术音乐治疗计量，MPA 专题无）
- **通讯作者单位**：Georgia Institute of Technology（决定出版协议适用性）

## 路线与费用（2026-11-04 核实）

| 路线 | 期刊 | 分区参考 | 费用 | 首次决定 | 接收概率估计 | 备注 |
|---|---|---|---|---|---|---|
| A 最快 | Behavioral Sciences（MDPI） | Q2–Q3 | 约 2,200 CHF ≈ 1.8 万元；**未发现 Georgia Tech 与 MDPI 的机构折扣**，需向 ioap@mdpi.com 与 GT 图书馆确认 | 约 3 周（2020 数据 17.8 天） | 70–75% | 该刊 2025 年发过 MPA 系统综述与 MPA 管理论文，范围匹配；"Interventions for Music Performance Anxiety"特刊截止 2026-01-26 已过，走常规栏目 |
| A′ | Healthcare（MDPI） | Q2–Q3 | 约 2,200 CHF | 约 19.5 天（2023 数据） | 65–70% | 范围偏医疗，MPA 可归"表演艺术医学" |
| B 零成本 | The Arts in Psychotherapy（Elsevier 混合） | Q2–Q3 | **0**：Georgia Tech 图书馆与 Elsevier 有 2025 年起的 Read & Publish 协议，覆盖混合期刊的开放获取费；不选 OA 也免费 | 6–10 周 | 60–65% | 范围是艺术治疗，MPA 计量属边缘匹配；需投稿前询问 |
| B′ 零成本 | Medical Problems of Performing Artists | Q3 | 0 | 2–4 月 | 55–60% | 范围最匹配，但季刊慢，文献计量非主流文体 |
| C | Medicine（Wolters Kluwer） | Q3 | 约 2,000–2,500 USD ≈ 1.5–1.8 万元；GT 无协议 | 4–8 周 | 65–70% | 2024 年发过同文体同领域论文 |

**Georgia Tech 出版协议现状**：无开放获取基金；Read & Publish 覆盖 Elsevier（仅混合期刊）、Wiley（2024 加入，2026 状态待确认）、ASME、SPIE、RSC、Royal Society。未发现 MDPI、Frontiers、Wolters Kluwer 协议。核对页面：library.gatech.edu/open-access。

**推荐**：预算允许走 A，三个月内见刊；不想花钱走 B，先给编辑发询问信，三天内得回复再决定。

## 研究缺口（≤ 3 句）
音乐表演焦虑研究积累四十年、跨心理学、医学、音乐教育与表演科学，但从未有人系统描绘其知识结构：谁在做、在哪发、主题如何演化、用了什么测量工具与设计。2024 年 Medicine 的"音乐治疗与焦虑"计量只覆盖临床音乐治疗，不含表演者。多篇 2025–2026 年干预综述指出测量不标准化与设计薄弱，却缺乏全景数据支撑。

## 研究问题
- RQ1：1985–2026 年 MPA 研究的产出趋势、国家、机构、期刊、核心作者与合作网络如何？
- RQ2：关键词共现与主题演化显示出哪些研究主题的兴起与衰退（从患病率与人格到干预、生理指标与技术）？
- RQ3：（内容编码）最常用的测量工具、研究设计与人群分别是什么，随时间如何变化？

RQ3 是与纯指标堆砌拉开差距的部分，也是审稿人会认为"有实质"的部分。

## 方法概要

### 检索
- **Web of Science 核心合集**，建库至检索日，高级检索：
  `TS=("music performance anxiety" OR "musical performance anxiety" OR (("performance anxiety" OR "stage fright") NEAR/3 (music* OR musician* OR instrumentalist* OR singer* OR vocalist* OR pianist* OR orchestra* OR conservator*)))`
  文献类型：Article、Review；语言不限
  导出：Full Record and Cited References，Plain Text 或 BibTeX，每批 500 条
- **Scopus** 同步检索（TITLE-ABS-KEY 等价式），导出 CSV 全字段，用于补充与敏感性分析
- 合并去重以 WoS 为主库（Bibliometrix 对 WoS 字段支持最完整）
- 排除：会议摘要、书评、勘误、非音乐情境的表演焦虑（体育、演讲、性功能）；双人核对题录，记录排除原因，画 PRISMA 式流程图

### 分析（R，Bibliometrix 4.x；VOSviewer 作可视化交叉验证）
1. 描述：年度产出与增长率（Price 定律拟合）、文献类型、语言
2. 来源：期刊产出与 Bradford 核心区、期刊 h 指数
3. 作者与机构：产出、Lotka 定律、合作网络、国家合作地图
4. 内容：高频关键词、关键词共现网络聚类、主题地图（Callon 中心性 × 密度）、主题演化（分三期：1985–2005、2006–2015、2016–2026）、共被引参考文献网络
5. **内容编码（RQ3）**：对全部纳入文献按题录与摘要编码：测量工具（K-MPAI、PAI、MPAI-A、STAI、PAQ、生理指标…）、研究设计（横断面 / 干预 / 质性 / 综述 / 测量学）、人群（学生 / 职业 / 青少年 / 混合）、技术介入（VR、生物反馈、App、AI、无）。双人编码 20% 校准，kappa ≥ 0.8
6. 图（6 张）：年度产出；国家合作地图；关键词共现网络；主题演化桑基图；主题地图；测量工具与设计随时间堆叠图

### 预计规模
- WoS 初检 600–1,000 条，纳入 400–700 篇

## 预期贡献
- 首张 MPA 研究全景图，供后续综述与基金申请定位
- 测量工具与设计的使用频次为 H10 COSMIN 综述与 A4 生理指标综述提供引言数据
- 识别"技术介入"子主题的兴起时间与规模，衔接 N6、F2

## 写法要点（面向高接受率）
- 照 Medicine 2024 年"音乐治疗与焦虑计量"的结构与图表数量写
- 讨论不止报数字：每个主题簇对应一段"这意味着什么"
- 局限写足：数据库覆盖、英文偏倚、计量指标的局限
- 投稿前向编辑发摘要询问范围；推荐 3–5 名发过 MPA 研究或文献计量的审稿人

## 配套 skill 与工具
| 阶段 | skill | 外部工具 |
|---|---|---|
| 预注册 | — | OSF |
| 检索导出 | — | WoS、Scopus（需学校账号） |
| 分析 | 会话内 `dataviz` 管配色 | R：bibliometrix、biblioshiny；VOSviewer |
| 编码 | — | Excel 编码表；R `irr` |
| 写作 | `/paper-writer`（Original Article） | 目标期刊模板 |
| 质控 | `/check-reporting`（自建 BIBLIO 条目表）→ `/verify-refs` → `/self-review` → `/humanize` → `/polish-language` | — |
| 投稿 | `/find-journal` 复核；`/manage-refs`（MDPI 用 ACS 风格数字引用，Elsevier 用 APA）；`/sync-submission` | 期刊投稿系统 |

## 时间表
| 周 | 你 | 助手 |
|---|---|---|
| 1 | WoS + Scopus 导出；决定路线 A 或 B；若 B 发询问信 | 检索式终稿；OSF 预注册；合并去重清洗 |
| 2 | — | Bibliometrix 全套分析；6 张图；编码表与 20% 校准样本 |
| 2–3 | 参与 20% 校准编码 | 全量编码；RQ3 统计 |
| 3 | 读初稿 | 全文初稿 |
| 4 | 署名与贡献声明 | 质控五步；投稿包；投稿 |
