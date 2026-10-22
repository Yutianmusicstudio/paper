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
