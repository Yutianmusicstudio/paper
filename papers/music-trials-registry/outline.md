# 稿件大纲：The global landscape of registered music intervention trials: design characteristics, technology-mediated delivery, completion and publication status

- **Slug**：music-trials-registry（看板编号 H3）
- **类型**：注册库横断面 meta 研究（cross-sectional analysis of trial registries）
- **目标期刊**：1) Journal of Music Therapy（OUP / AMTA） 2) Frontiers in Psychology, Health Psychology 3) Complementary Therapies in Clinical Practice
- **字数上限**：Journal of Music Therapy 建议 ≤ 8,000 词，表 ≤ 6（投稿前复核作者须知）
- **报告规范**：STROBE（横断面，适配 meta 研究）；预注册分析计划
- **预注册**：OSF Registries（开题第一周）
- **伦理**：不需要（公开注册数据）
- **查重状态**：🟢（2026-10-26；仅有 2020 GSA、2022 ACP 两个会议摘要，无全文发表，无技术介导与发表状态分析）

## 研究缺口（≤ 3 句）
音乐干预试验数量在过去十年快速增长，但没有一篇同行评审论文描述过全球注册试验的整体面貌：做了什么人群、什么设计、什么结局，多少比例用远程、App、VR 或 AI 等技术介导，多少完成并发表。2020 年 Robb 团队的会议摘要统计了 449 项注册试验，但从未扩展为全文，也未追踪完成与发表。缺少这张"地图"，领域无法判断研究资源是否错配、技术转向是否真实发生、以及是否存在发表偏倚。

## 研究问题
- RQ1：全球注册的音乐干预试验在时间、国家、资助方、人群、设计、样本量、对照和主要结局上呈何种分布？
- RQ2：技术介导的交付方式（远程、App、VR/AR、可穿戴自适应、AI 生成音乐、机器人）占比多少，随时间如何变化，与非技术试验在设计特征上有何差异？
- RQ3：试验的完成率、终止 / 撤回率、结果上传率和同行评审发表率各是多少；哪些特征预测终止与未发表？

## 方法概要

### 数据来源
- ClinicalTrials.gov（API v2 批量导出 JSON）
- WHO ICTRP 搜索门户（覆盖 ChiCTR、ANZCTR、ISRCTN、DRKS、CTRI、JPRN 等，XML 导出）
- 去重：按注册号、二级 ID、题名模糊匹配

### 检索
- 字段：intervention、title、condition、keywords
- 词：`music OR musical OR "music therapy" OR "music medicine" OR singing OR choir OR "rhythmic auditory" OR "auditory stimulation" OR songwriting OR drumming OR "sound therapy"`
- 时间：建库至检索日；手工排除"music"仅作背景词的记录（如手术室噪音研究）

### 纳入标准
- 干预试验（随机或非随机）；音乐为主要干预成分或主要对照
- 排除：观察性研究、音乐仅作刺激材料的基础研究、纯噪声 / 白噪音

### 编码变量（双人独立编码 20% 样本，kappa ≥ 0.8 后单人编码）
| 类别 | 变量 |
|---|---|
| 注册 | 注册库、注册年、国家 / 地区、资助方类型（学术 / 政府 / 产业 / 医院） |
| 人群 | 年龄组、临床类别（ICD-11 章节）、健康人群 / 患者 |
| 设计 | 随机 / 非随机、平行 / 交叉 / 单臂、盲法、计划样本量、对照类型 |
| 干预 | 音乐治疗（认证治疗师）vs 音乐医学（预录音乐）；主动 / 接受式；剂量 |
| 技术介导 | 无 / 远程视频 / App 或网页 / VR-AR / 可穿戴自适应 / AI 生成音乐 / 机器人；编码规则附操作定义 |
| 结局 | 主要结局领域（焦虑、疼痛、抑郁、认知、运动、生理指标…）；测量工具 |
| 状态 | recruiting / completed / terminated / withdrawn / unknown；终止原因 |
| 发表 | 注册库结果上传；PubMed、Scopus、Google Scholar 按注册号与题名匹配发表论文；发表年 |

### 分析
- 描述统计；注册数年度趋势（Joinpoint 或 Poisson 回归）
- 技术介导 vs 非技术：设计特征比较（χ²、Mann–Whitney）
- 完成与发表：Kaplan–Meier 注册至发表时间；Logistic 回归预测终止与未发表（资助方、样本量、国家收入组、技术介导、注册年）
- 敏感性分析：仅 ClinicalTrials.gov；仅随机试验
- 图：世界地图（注册数）、年度堆叠面积图（技术类型）、Sankey（状态 → 发表）、森林图（回归 OR）

### 预计规模
- 初检 3,000–4,000 条，去重纳入 1,500–2,500 项；2015 年后约占三分之二

## 预期贡献
- 理论：首张全球音乐干预试验地图，量化技术转向的真实幅度
- 实践：指出人群与结局的研究空白、重复，帮助资助者与研究者定位
- 方法：首次报告音乐干预领域的终止率与发表率，为发表偏倚和后续综述的证据评级提供依据；与 H4 报告质量研究、H10 测量工具综述形成"方法学三部曲"

## 风险与对策
- ICTRP 导出限额与格式不一 → 分批导出，脚本标准化字段
- 发表匹配漏检 → 三库匹配 + 注册号反查 + 对 2020 年前完成试验限定随访窗口 ≥ 4 年
- "技术介导"定义争议 → 预注册操作定义，双人编码，报告 kappa
- 网络策略：当前环境需在 Network access 放行 `clinicaltrials.gov`、`trialsearch.who.int`、`eutils.ncbi.nlm.nih.gov`

## 配套 skill 与工具
| 阶段 | 本仓库 skill | 外部工具 |
|---|---|---|
| 预注册 | — | OSF Registries（分析计划模板） |
| 数据获取 | — | ClinicalTrials.gov API v2；ICTRP XML 导出；Python pandas 清洗脚本（放 `data/`） |
| 编码 | — | Google Sheets 或 REDCap 双人编码表；kappa 用 R `irr` |
| 发表匹配 | `/search-lit`（API 放行后）；`/verify-refs` 核对匹配到的论文 | PubMed E-utilities；OpenAlex；Scopus |
| 分析与图 | 会话内 `dataviz` skill 做图配色与规范 | R（survival、ggplot2、sf）或 Python |
| 写作 | `/paper-writer`（Original Article，STROBE） | — |
| 质控 | `/check-reporting`（STROBE）→ `/verify-refs` → `/self-review` → `/humanize` → `/polish-language` | — |
| 投稿 | `/find-journal` 复核；`/manage-refs` 出 APA 7；`/sync-submission` | OUP ScholarOne |
| 返修 | `/revise` | — |

## 时间表
| 周 | 任务 | 状态 |
|---|---|---|
| 1 | OSF 预注册分析计划；放行网络域名；写导出脚本 | 待开始 |
| 2 | 两库导出、去重、初筛；冻结数据集并存 `data/` | |
| 3–4 | 编码手册定稿；双人编码 20% 校准；全量编码 | |
| 5–6 | 发表匹配三库检索；状态核对 | |
| 7 | 统计分析；四张主图 | |
| 8–9 | Methods、Results 初稿 | |
| 10 | Introduction、Discussion、Abstract | |
| 11 | `/check-reporting`、`/verify-refs`、`/self-review`、语言两轮 | |
| 12 | 投稿 Journal of Music Therapy；记录 submission-log | |
