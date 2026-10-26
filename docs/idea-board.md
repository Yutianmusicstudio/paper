# Idea 看板（已查重）

查重日期：2026-10-22。方法见 `docs/novelty-check.md`。学术 API 被网络策略拦截，本轮全部依赖网页搜索，覆盖率有限：**🟢 只代表"两轮检索未发现"，开题前仍需在 PubMed / Scopus / PROSPERO / OSF 各跑一次确认。**

判定标记：🟢 空白，可直接开题 ｜ 🟡 有近邻，必须差异化 ｜ 🔴 已被占，放弃或大改

## 优先队列（按 速度 × 空白度 × Q2–Q3 命中率）

| 序 | 编号 | 题目 | 判定 | 设计 | 伦理 | 预计投稿 |
|---|---|---|---|---|---|---|
| 1 | A4 | 可穿戴 / 心率变异性等生理指标在音乐表演焦虑研究中的应用：系统综述（可加 meta） | 🟢 | PRISMA 2020 | 否 | 3–4 个月 |
| 2 | N1 | AI 生成音乐 vs 人类创作音乐对状态焦虑的效应：在线随机实验（或先做快速综述） | 🟢 | 在线 RCT，n≈150 | 最低风险 | 4–5 个月 |
| 3 | A3′ | 音乐治疗师对 AI 的接受度、使用与伦理顾虑：国际横断面调查 | 🟢 | UTAUT2 + 开放题 | 是 | 5–6 个月 |
| 4 | A1′ | AI 在音乐治疗临床实践中的角色：PRISMA-ScR 范围综述 | 🟡 | PRISMA-ScR | 否 | 3–4 个月，窗口在收窄 |
| 5 | N3 | 高校音乐专业学生的生成式 AI 使用与学术诚信认知：横断面调查 | 🟢 | 问卷 | 是 | 4–5 个月 |
| 6 | N6 | 技术介导的音乐表演焦虑干预（VR、App、生物反馈、在线 CBT）：范围综述 | 🟢 | PRISMA-ScR | 否 | 3–4 个月 |
| 7 | C1 | 音乐治疗中负责任使用 AI 的实践框架：概念性论文 | 🟢 | 概念 / 评论 | 否 | 与 A3′ 配套 |
| 8 | A2′ | AI × 音乐 × 健康的文献计量（2015–2026） | 🟡 | Bibliometrix | 否 | 需再查重 |
| 9 | B1 | VR 暴露降低音乐表演焦虑：单臂可行性研究 | 🟡 | 前后测 | 是 | 6–9 个月 |

放弃：A2（AI 音乐教育综述 / 计量，🔴）、A5（远程音乐治疗综述，🔴）、N4（EEG / 神经反馈音乐治疗综述，🔴）。降级：B3、B4、N5。

---

## 逐条证据

### A4 🟢 生理指标与音乐表演焦虑：系统综述
- **检索到的近邻**：Nicholl & Abbott (2026) *Psychology of Music* 治疗效果 meta 分析（16 RCT，不聚焦生理指标）；2022 *Frontiers in Psychiatry* 22 名钢琴学生腕式心率监测研究；HRV 生物反馈治 MPA 的学位论文；Bellinger 等 (2023) *BMC Psychiatry* VR 试验方案以 HRV 为主要结局。
- **空白**：未发现任何以可穿戴 / 生理指标为对象的 MPA 系统综述。
- **建议角度**：纳入所有在真实或模拟演出中测量 HRV、心率、皮电、皮质醇等指标的研究，回答三个问题：用了哪些设备与指标、指标与自评焦虑的相关性、作为干预结局的敏感度。若 ≥5 篇可合并则做 meta。
- **目标期刊**：Psychology of Music；Frontiers in Psychology (Performance Science)；Medical Problems of Performing Artists；Applied Psychophysiology and Biofeedback。
- **下一步**：PROSPERO 注册；检索 PubMed、PsycINFO、Scopus、RILM。

### N1 🟢 AI 生成音乐 vs 人类创作音乐对焦虑的效应
- **近邻**：2024 Prolific 在线实验（n=152，Suno 生成 vs 人类，STAI-S 仅作探索性指标，MIT Media Lab / Myndstream）；2025 视听研究（n=88，瞳孔扩张，AI 更唤醒）；2026 *Frontiers in Psychology* 情绪识别准确率研究；Sigma INRC 2026 会议摘要的 8 项研究系统综述。
- **空白**：没有以焦虑缓解为主要结局、按接受式音乐治疗范式设计的随机实验，也没有正式发表的综述。
- **建议角度**：双盲在线 RCT，三臂（AI 生成 / 人类创作 / 静默），诱发轻度压力后测 STAI-S 与主观放松；预注册于 OSF。成本低、周期短。可先投一篇快速综述占位。
- **目标期刊**：JMIR Formative Research；Psychology of Music；Frontiers in Psychology；Music & Science。

### A3′ 🟢 音乐治疗师的 AI 接受度调查（合并原 B2）
- **近邻**：爱丁堡 2025 本科学位论文（8 人访谈，未发表）；*Revista MiSOSTENiDO* 2025 的 AI 核心胜任力框架；音乐教师 UTAUT2 研究已有多篇（🔴 那边已挤）。
- **空白**：没有任何同行评审的音乐治疗师 AI 态度 / 使用调查，也无专业协会立场声明。
- **建议角度**：面向 AMTA、BAMT、WFMT 会员的多国在线问卷，UTAUT2 + 伦理顾虑量表 + 临床任务清单（评估、即兴、文档、督导）。n ≥ 200。
- **目标期刊**：Journal of Music Therapy；Nordic Journal of Music Therapy；The Arts in Psychotherapy；JMIR Formative Research。
- **配套**：C1 概念论文用其结果做支撑，形成系列。

### A1′ 🟡 AI 在音乐治疗临床实践中的范围综述
- **近邻（都在 2025–2026 密集出现）**：*Applied Sciences* 2026 生成式 AI 音乐治疗系统专题综述（25 篇，系统视角）；2025 Springer 会议 AI 治疗性音乐生成系统综述（按模型架构分类）；*Frontiers in Psychology* 2026-01 AI 辅助音乐治疗工具叙述性综述；Sigma INRC 2026 摘要。
- **空白**：没有 PRISMA-ScR、面向临床功能（评估、干预、文档、培训）而非模型架构的范围综述。
- **风险**：窗口正在关闭，必须 2 个月内投出。
- **目标期刊**：Nordic Journal of Music Therapy；The Arts in Psychotherapy；Frontiers in Psychology。

### N3 🟢 音乐专业学生的生成式 AI 使用与学术诚信
- **近邻**：2024 arXiv 音乐学 LLM 态度问卷预印本；Bofinger 2024 澳大利亚高等音乐教育学术诚信论文（引用通用数据）；Liberty 2026 博士论文（质性）。
- **空白**：没有 2025–2026 面向音乐专业学生的同行评审调查。
- **目标期刊**：International Journal of Music Education；Music Education Research；British Journal of Music Education。

### N6 🟢 技术介导的 MPA 干预范围综述
- **近邻**：Bissonnette 2015 VR 探索研究（n=17）；Bellinger RCT 仍在招募；UiTM *JCA* 2025 VR-MPA 叙述性综述（小刊）；2024–2026 未见 App 先导研究；一项注册中的音乐学生健康 App 可行性试验（NCT07033793，非焦虑）。
- **空白**：没有把 VR、App、生物反馈、在线 CBT 合并审视的范围综述。
- **目标期刊**：Frontiers in Psychology；Medical Problems of Performing Artists；JMIR Serious Games。

### C1 🟢 负责任使用 AI 的音乐治疗实践框架
- **近邻**：*Applied Sciences* 2026 强调"人在回路"；PMC 2026 主动式 AI 音乐治疗视角文；MiSOSTENiDO 2025 胜任力框架。
- **空白**：AMTA、BAMT、WFMT 均未检索到 AI 立场声明。
- **建议**：以 A3′ 数据为基础写框架，或先作为 perspective 投 Frontiers。

### A2′ 🟡 AI × 音乐 × 健康文献计量
- Tong et al. 2026 *JAISCR* 的 AI in Music 计量覆盖创作、表演、教育，未覆盖治疗 / 健康。需再跑一轮"bibliometric music therapy artificial intelligence"确认。

### B1 🟡 VR MPA 先导研究
- Bellinger 的 46 人 RCT 结果一旦发表，单臂先导的价值下降。若做，强调低成本一体机与 HRV 并测，投 JMIR Serious Games。

### 🔴 放弃项
- **A2 AI 音乐教育综述 / 计量**：*Research Studies in Music Education* 2026 范围综述（22 篇）；*European Journal of Education* 2026 系统综述（46 篇）；*Frontiers in Psychology* 2026 自我信念系统综述；Tong 2026 计量 + 综述；Arcagok 2025 计量；Cheng 2025 *Arts Education Policy Review*。
- **A5 远程音乐治疗综述**：*The Arts in Psychotherapy* 2026 范围综述（53 篇，2009–2025）；PMC 2025 癌症 tele-music 系统综述。
- **N4 EEG / 神经反馈音乐治疗综述**：Sayal 等 2025 *Frontiers in Neuroscience* 系统综述；Perrotta 2025 *Technologies* BCI 乐手专题综述。
- **A3 原版（音乐教师 UTAUT2）**：中国职前音乐教师 848 人 UTAUT2（2026）、370 人扩展 UTAUT、器乐教师混合方法（2026）、TAM 218 人（2025）。

---

## 第二批：高可发性候选（查重日期 2026-10-26）

筛选标准：不需要伦理或只需豁免、不依赖招募、审稿人熟悉的论文类型（COSMIN 综述、meta 研究、注册库分析、公开数据挖掘、范围综述）。概率为判断估计。

| 序 | 编号 | 题目 | 判定 | 伦理 | 周期 | 可发概率 |
|---|---|---|---|---|---|---|
| 1 | H10 | 音乐表演焦虑测量工具的测量学特性：COSMIN 系统综述 | 🟢 | 否 | 3–4 月 | 75–85% |
| 2 | H3 | 全球注册的音乐干预临床试验特征、技术介导比例与发表状态：注册库横断面分析 | 🟢 | 否 | 2–3 月 | 70–80% |
| 3 | H4 | 技术介导音乐干预试验的报告质量：对照 RG-MBI 2025 与 CONSORT-EHEALTH 的 meta 研究 | 🟢 | 否 | 3–4 月 | 70–80% |
| 4 | H1 | 音乐学习 App 用户评价的主题与情感挖掘（Yousician、Simply Piano、Flowkey 等） | 🟢 | 公开数据，通常豁免 | 3–4 月 | 70–80% |
| 5 | H7 | VR / AR / MR 在音乐教育中的应用：PRISMA-ScR 范围综述 | 🟢 | 否 | 3–4 月 | 65–75% |
| 6 | H2 | 应用商店音乐类心理健康 App 的系统检索与 MARS 质量评价 | 🟡 | 否 | 3 月 | 60–70% |
| 7 | H9 | LLM 对音乐学生演奏 / 作曲反馈的质量：教师盲评研究 | 🟡 | 最低风险 | 5–6 月 | 60–70% |
| 8 | H6 | AI 自动演奏评估系统在教育情境中的效度与信度：系统综述 | 🟡 | 否 | 3–4 月 | 55–65% |
| 9 | H5 | 传感器 / 可穿戴反馈系统对器乐学习效果的影响：系统综述 | 🟡 | 否 | 3–4 月 | 55–65% |
| — | H8 | 音乐干预 × 痴呆伞状综述 | 🔴 | — | — | 放弃 |

### H10 🟢 MPA 测量工具 COSMIN 系统综述
- 近邻：西班牙语 K-MPAI 文献综述（非 COSMIN）；Nicholl & Abbott 2026 与 MDPI *Behavioral Sciences* 2025 干预综述均指出"MPA 测量缺乏标准化"但未做测量学评价；2022 Mazzarollo 五项短量表、2024 葡萄牙语 MPA 量表等单量表验证研究持续出现。
- 空白：未发现对 K-MPAI、PAI、MPAI-A、STAI 改编版等工具的 COSMIN 系统综述。
- 建议角度：按 COSMIN 流程评价所有 MPA 专用量表及其译本的结构效度、内部一致性、跨文化效度，给出"推荐 / 有潜力 / 不推荐"分级。审稿人对 COSMIN 综述接受度高、结构固定。
- 目标期刊：Psychology of Music；Frontiers in Psychology；Musicae Scientiae。
- 下一步：PROSPERO 直接检索确认无同类注册后立即注册。

### H3 🟢 音乐干预试验注册库横断面分析
- 近邻：2020 年 GSA 会议摘要（ClinicalTrials.gov + WHO ICTRP，449 项，48 国）；2022 ACP 会议摘要（老年人 603 项）；均无全文发表，也未分析技术介导与发表状态。
- 空白：无同行评审的注册库全景分析，更无技术介导（App、VR、远程、AI）比例与完成 / 发表率分析。
- 建议角度：检索 ClinicalTrials.gov 与 ICTRP 全部音乐干预试验，描述人群、设计、结局、技术介导比例、完成状态，并匹配已发表论文计算发表率。
- 目标期刊：Journal of Music Therapy；Frontiers in Psychology；Complementary Therapies in Clinical Practice；Trials。
- 下一步：OSF 预注册分析计划。

### H4 🟢 技术介导音乐干预试验报告质量 meta 研究
- 近邻：Robb 等 2018 报告质量基线综述（187 项，<50% 报告四项核心内容）；2024 外科预录音乐干预 TIDieR 综述（PROSPERO CRD42023427138）；Robb 等 2025 RG-MBI 更新版（12 项，*Integrative Medicine Research*）与 Frontiers 2025 释义指南。
- 空白：RG-MBI 2025 尚未被用于审计任何子领域；技术介导干预（App、远程、VR、AI 生成音乐）从未被系统审计报告质量。
- 建议角度：纳入 2015–2026 技术介导音乐干预试验，用 RG-MBI 2025 + CONSORT-EHEALTH 双清单评分，报告逐项符合率与时间趋势。方法学论文命中率高，且 RG-MBI 作者群是潜在审稿人。
- 目标期刊：Journal of Music Therapy；Frontiers in Psychology；JMIR Formative Research；Integrative Medicine Research。
- 下一步：PROSPERO 注册。

### H1 🟢 音乐学习 App 用户评价挖掘
- 近邻：Spotify 评价情感分析（2024，非学习类）；健康 App 评价人工标注研究（2025）；商业网站对 Yousician 等差评的非学术汇总。
- 空白：未发现任何对音乐学习 App 公开用户评价做主题建模或情感分析的学术研究。
- 建议角度：抓取 Google Play 与 App Store 上 5–8 个主流音乐学习 App 的评价，LDA / BERTopic 主题建模 + 情感分析，以自我调节学习或 Hattie 反馈框架解读学习者感知的反馈、动机与放弃原因。数据公开，多数伦理委员会判豁免。
- 目标期刊：Education and Information Technologies；International Journal of Music Education；Computers and Education: Artificial Intelligence；JMIR Formative Research。
- 下一步：确认平台条款允许学术抓取；OSF 预注册分析计划。

### H7 🟢 VR / AR / MR 音乐教育范围综述
- 近邻：Zhang & Wan Yahaya 2025 IGI Global 书章 AR 音乐教育系统综述（可见度低，仅 AR）；*Scientific Reports* 2025 VR 音乐课堂模型研究；通用教育 AR/VR 综述多篇。
- 空白：无期刊发表的 PRISMA-ScR，覆盖 VR、AR、MR 三类技术在音乐教育中的应用、学习结果与评价方法。
- 建议角度：2015–2026，按技术类型 × 教学内容（器乐、视唱练耳、合奏、音乐史）× 结果类型映射，指出证据密度与空白。
- 目标期刊：International Journal of Music Education；Music Education Research；Education and Information Technologies。
- 下一步：OSF 预注册。

### H2 🟡 音乐类心理健康 App 的 MARS 评价
- 近邻：*Frontiers in Human Neuroscience* 2026 范围综述（22 个音乐数字疗法产品，20 家公司中仅 8 家有同行评审证据，属商业扫描）；*Frontiers in Psychiatry* 2024 音乐治疗 App 证据等级综述（31 项研究）；通用心理健康 App MARS 综述（2026，77 个 App）。
- 空白：无应用商店系统检索 + MARS 评分 + 证据映射的消费级音乐 App 研究。
- 差异点：对象是商店可下载的 App 而非公司，方法是 MARS 标准化评分而非文献综述。
- 目标期刊：JMIR mHealth and uHealth；JMIR Formative Research；Digital Health。

### H9 🟡 LLM 反馈质量教师盲评
- 近邻：LLaQo（arXiv 2024，钢琴演奏反馈模型，计算机视角）；2025 声乐 LLM 反馈元认知研究；McPherson 等 2022 音乐教学反馈框架。
- 空白：无教育期刊发表的"教师盲评 LLM vs 教师反馈"研究。
- 建议角度：用公开学生演奏录音或作曲作业生成 ChatGPT / Claude / Gemini 反馈，与教师反馈混合后由 20 名以上教师按 Hattie 反馈层级盲评。教师评分者需最低风险伦理。
- 目标期刊：Music Education Research；British Journal of Music Education；Computers and Education: Artificial Intelligence。

### H6 🟡 AI 自动演奏评估效度综述
- 近邻：Moura 等 2024 *Frontiers in Psychology* 独奏演奏评估标准系统综述（评估体系与标准，非 AI 效度）；2026 arXiv 自动歌唱评估 30 年综述；2019 演奏分析综述。
- 差异点：只纳入 AI / 自动系统并评价其与人类评分者的一致性、信效度报告质量。

### H5 🟡 传感器反馈对器乐学习效果综述
- 近邻：Volta & Di Stefano 2024 *Sensors* 可穿戴研究音乐体验系统综述（23 项，覆盖面宽，设备视角）。
- 差异点：只纳入有学习结果测量的教学研究，回答"有没有用"而非"有什么设备"。

### H8 🔴 音乐 × 痴呆伞状综述
- 2023 *IJERPH* 已注册伞状综述方案；2025 Cochrane 综述；2026 两篇非药物干预伞状综述均含音乐。放弃。

---

## 第三批：快速发表候选，目标 Q3 以上（查重日期 2026-10-26）

筛选标准：公开材料或 AI 输出的内容分析、评价类研究、meta 研究；2–3 个月可投；不需要伦理；Q3 期刊常见文体。Medical Problems of Performing Artists 已确认为 SCIE Q3（2025 IF 0.87），是表演类选题的稳妥落点。

| 序 | 编号 | 题目 | 判定 | 周期 | 可发概率 | 首选期刊 |
|---|---|---|---|---|---|---|
| 1 | F2 | AI 聊天机器人对音乐表演焦虑常见问题回答的质量、可读性与安全性评价 | 🟢 | 2 月 | 70–80% | Medical Problems of Performing Artists |
| 2 | F7 | 音乐治疗与音乐教育期刊的开放科学实践审计（预注册、数据共享、利益冲突） | 🟢 | 2–3 月 | 70–80% | Journal of Music Therapy / Music & Science |
| 3 | F10 | 音乐表演焦虑研究 40 年文献计量与主题演化 | 🟢 | 2 月 | 60–70% | Medical Problems of Performing Artists / Frontiers in Psychology |
| 4 | F1 | 大语言模型在音乐治疗资格考试样题与分级乐理考试上的表现 | 🟡 | 2–3 月 | 65–75% | Journal of Music Therapy / JMIR Medical Education |
| 5 | F3 | YouTube 与 TikTok 音乐表演焦虑视频的内容质量与可靠性 | 🟢 | 2 月 | 65–75% | Medical Problems of Performing Artists / JMIR Infodemiology |
| 6 | F4 | 音乐学习与音乐治疗 App 的隐私政策与数据实践审计 | 🟢 | 2–3 月 | 65–75% | JMIR mHealth and uHealth / Digital Health |
| 7 | F6 | 音乐治疗认证课程中的技术与 AI 内容：课程文件分析 | 🟢 | 2 月 | 60–70% | Journal of Music Therapy / Nordic Journal of Music Therapy |
| 8 | F5 | 音乐治疗师与音乐教师招聘广告中的数字能力要求：内容分析 | 🟢 | 2 月 | 60–70% | International Journal of Music Education / Nordic Journal of Music Therapy |
| 9 | F9 | 主流音乐学习 App 的无障碍（WCAG）审计 | 🟡 | 2–3 月 | 55–65% | Universal Access in the Information Society |
| 10 | F8 | 音乐教育研究的 Altmetric 关注度分析 | 🟡 | 2 月 | 50–60% | Music Education Research |
| — | F11 | Suno / Udio 在治疗与课堂的评价研究 | 🟡 | 需评分者 | — | 降级 |

### F2 🟢 聊天机器人 MPA 信息质量评价
- 近邻：Whittaker & Sun 2025 *Health Informatics Journal* 对 74 项"聊天机器人回答患者问题"研究的综合（证明文体成熟）；各科室 DISCERN / PEMAT / 可读性评价研究数十篇；音乐或 MPA 领域一篇没有。
- 空白：无人评价过 ChatGPT、Gemini、Claude、Copilot 对乐手 MPA 问题（原因、药物如 β 受体阻滞剂、认知行为疗法、呼吸技巧、何时就医）回答的质量。
- 建议角度：从 Reddit、论坛和 MPA 文献提取 25–30 个常见问题，四个模型各答一次，两名表演医学专家按 DISCERN、PEMAT、准确性、安全性评分，加 Flesch 可读性；重点看药物建议与就医转介是否安全。
- 下一步：OSF 预注册问题清单与评分表。

### F7 🟢 音乐治疗与音乐教育期刊开放科学审计
- 近邻：Eerola 2024（五本音乐心理学期刊含 *Psychology of Music*，239 篇，2017–2022：5% 共享原始数据，0 预注册）；Düvel & Altemeier 2025 *Jahrbuch Musikpsychologie* 计量。
- 空白：音乐治疗期刊（JMT、NJMT、Arts in Psychotherapy、Music Therapy Perspectives）与音乐教育期刊（IJME、JRME、MER、BJME、RSME）从未被审计。
- 建议角度：2019–2025 各刊随机抽样共 400–500 篇实证论文，按 Hardwicke 透明度指标编码：预注册、数据、材料、代码、利益冲突、资助、开放获取、复制研究；与 Eerola 的音乐心理学结果对照。
- 下一步：OSF 预注册编码手册。

### F10 🟢 MPA 文献计量
- 近邻：*Medicine* 2024 音乐治疗与焦虑计量（1993–2023，临床视角）；手术音乐治疗计量 2025；MPA 本身无计量研究。
- 建议角度：WoS + Scopus，1980–2026，Bibliometrix + VOSviewer；必须加实质内容：主题演化（从患病率到干预、从心理到生理与技术）、测量工具使用频次（为 H10 铺路）、研究设计分布。避免纯指标堆砌。
- 风险：审稿人对纯计量疲劳，需与 H10 互为引用增加价值。

### F1 🟡 LLM 音乐治疗资格考试与乐理考试
- 近邻：Pond & Fujinaga 2025（SciTePress 会议，RCM Level 6 乐理，GPT-4o / Claude 3.5 / Gemini 1.5，最高 75%）；2024 arXiv 音乐推理评估；2026 arXiv GPT-4o-mini 音乐分析自动评分。
- 空白：无期刊论文；无音乐治疗资格考试（CBMT）样题研究；无跨级别、跨最新模型的教育学分析。
- 差异点：CBMT 用公开出版的备考题库（注意版权，不用真题）；乐理用 ABRSM 公开历年试卷 1–8 级做难度梯度；分析错误类型对教学的含义。医学领域此类论文年产数百篇，Q3 期刊接受度高。
- 风险：模型迭代快，投稿时需用当时最新模型并写明版本与日期。

### F3 🟢 短视频 MPA 内容质量
- 近邻：2026 *Supportive Care in Cancer* 450 条心理健康视频研究发现"音乐治疗类视频质量最低"；TikTok 焦虑症视频质量研究 2025；2011 YouTube 音乐治疗描述性研究。MPA 专题无。
- 建议角度：YouTube + TikTok 各 100 条，GQS + 改良 DISCERN + 上传者类型 + 互动指标；重点看非专业人士的药物建议。

### F4 🟢 App 隐私与数据实践审计
- 近邻：Mozilla 2022 心理健康 App 隐私报告（32 个，含冥想类）；2021 冥想 App 数据收集分析；学术研究无。
- 建议角度：与 H1 共用 App 样本，读隐私政策 + 商店数据标签 + 实际网络流量（可选），按 GDPR / COPPA 维度编码；未成年学习者数据保护是卖点。

### F6 🟢 音乐治疗课程技术内容文件分析
- 近邻：AMTA 能力标准含"利用技术"条目；NYU 等个别项目设音乐治疗技术课；无系统分析。
- 建议角度：AMTA 认证项目 + 英国 HCPC 认可项目 + 澳洲项目的公开课程手册，编码技术 / AI 课程有无、学分、内容类型，对照 2025 年 MiSOSTENiDO 的 AI 胜任力框架。

### F5 🟢 招聘广告数字能力内容分析
- 近邻：2026 *Sustainability* 音乐教师 DigCompEdu 自评调查；1980 年代音乐治疗岗位描述能力分析。招聘广告内容分析无。
- 建议角度：Indeed、LinkedIn、AMTA 与各国教育局招聘平台 12 个月滚动抓取，编码技术与 AI 要求，比较治疗师 vs 教师、国家、机构类型。

### F9 🟡 / F8 🟡
- F9：EarSketch 审计、MusiBraille 2024 研究存在，跨 App 系统审计无；领域偏窄。
- F8：2017–2022 创意艺术治疗 Altmetric 研究已有（含音乐治疗），音乐教育专题无；价值有限。

## 来源链接
- Applied Sciences 2026 生成式 AI 音乐治疗系统综述：https://doi.org/10.3390/app16094120
- Frontiers in Psychology 2026-01 AI 辅助音乐治疗工具综述：https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1741463/full
- Sigma INRC 2026 AI 生成音乐干预系统综述摘要：https://www.sigmarepository.org/inrc/2026/presentations_2026/248/
- Arts in Psychotherapy 2026 远程音乐治疗范围综述：https://www.sciencedirect.com/science/article/pii/S0197455626000195
- Nicholl & Abbott 2026 MPA 治疗 meta 分析：https://doi.org/10.1177/03057356251322655
- 2022 钢琴学生 HRV 研究：https://www.frontiersin.org/articles/10.3389/fpsyt.2022.853733/full
- Bellinger 2023 VR-MPA 试验方案：https://bmcpsychiatry.biomedcentral.com/articles/10.1186/s12888-023-05040-z
- 2024 AI vs 人类音乐在线实验：https://arxiv.org/html/2506.02856
- 2025 视听 AI 音乐生理研究：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12194076/
- 爱丁堡 2025 音乐治疗师 AI 访谈论文：https://www.2025.graduateshow.eca.ed.ac.uk/sites/default/files/2025-05/LH%20Dissertation%20ECA%20Graduate%20Show%202025.pdf
- RSME 2026 AI 音乐教育范围综述：https://journals.sagepub.com/doi/full/10.1177/1321103X261453265
- EJE 2026 高教器乐 AI 系统综述：https://onlinelibrary.wiley.com/doi/10.1111/ejed.70691
- Tong 2026 AI in Music 计量：https://reference-global.com/article/10.2478/jaiscr-2026-0010
- Sayal 2025 音乐神经反馈系统综述：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11906423/
- 2024 音乐学 LLM 态度问卷预印本：https://arxiv.org/html/2409.01864v1
- 2025 AI 练习 App 自我效能研究：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12557579/
- Moura 等 2024 独奏演奏评估标准系统综述：https://www.frontiersin.org/articles/10.3389/fpsyg.2024.1467434/full
- Volta & Di Stefano 2024 可穿戴与音乐体验系统综述：https://doi.org/10.3390/s24175783
- Robb 等 2025 RG-MBI 更新与验证：https://doi.org/10.1177/27536130251384199
- 2024 外科预录音乐干预报告质量 TIDieR 综述：https://pubmed.ncbi.nlm.nih.gov/39586427/
- 2020 音乐治疗注册试验全球概览会议摘要：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7741628/
- Frontiers Hum Neurosci 2026 音乐数字疗法范围综述：https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2026.1602004/full
- Frontiers Psychiatry 2024 音乐治疗 App 证据综述：https://www.frontiersin.org/journals/psychiatry/articles/10.3389/fpsyt.2024.1366575/pdf
- Zhang & Wan Yahaya 2025 AR 音乐教育系统综述书章：https://www.igi-global.com/chapter/a-systematic-review-of-augmented-reality-in-music-education/372161
- LLaQo 演奏反馈模型：https://arxiv.org/pdf/2409.08795
- IJERPH 2023 音乐治疗痴呆伞状综述方案：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9961781/
- MDPI Behavioral Sciences 2025 MPA 干预综述（指出测量标准化缺口）：https://www.mdpi.com/2076-328X/15/2/138
- Whittaker & Sun 2025 聊天机器人回答质量综合：https://journals.sagepub.com/doi/10.1177/14604582251388879
- Eerola 2024 音乐心理学期刊透明度研究：https://durham-repository.worktribe.com/output/3344268
- Düvel & Altemeier 2025 Jahrbuch Musikpsychologie 开放科学计量：https://jbdgm.psychopen.eu/index.php/JBDGM/article/view/229
- Pond & Fujinaga 2025 LLM 乐理考试研究：https://www.scitepress.org/PublishedPapers/2025/135061
- Medicine 2024 音乐治疗与焦虑文献计量：https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10977525/
- 2026 心理健康视频质量研究（音乐治疗类最低）：https://link.springer.com/article/10.1007/s00520-026-11078-y
- 2011 YouTube 音乐治疗视频描述性研究：https://pubmed.ncbi.nlm.nih.gov/22097103/
- Sustainability 2026 音乐教师数字能力研究：https://doi.org/10.3390/su18073640
- 创意艺术治疗 Altmetric 研究（2017–2022）：https://science.rsu.lv/en/publications/academic-and-social-impact-of-creative-arts-therapies-research-20/
- Medical Problems of Performing Artists 分区参考：https://www.journalmetrics.org/journal/medical-problems-of-performing-artists
