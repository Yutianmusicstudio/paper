# 研究纲领：一个深核心 + 一圈好发的边缘工作

## 为什么这样做
单篇论文靠选题新颖，长期产出靠纲领。一个核心方向（hub）决定你的学术身份，围绕它的边缘论文（spokes）用快周期设计反复发表，互相引用，积累成系列。好处有三：检索与文献库复用、审稿人与编辑逐渐认识你、每篇新稿的引言都有自己的前作可引。要避免的是 salami slicing，即把一份数据切成多篇。这里的 spokes 是不同数据源、不同方法回答同一主题下的不同问题，属正当的研究纲领。

## 两个候选 hub（现有 idea 已能映射）

### Hub A：技术介导的音乐表演焦虑评估与管理
Technology-mediated assessment and management of music performance anxiety (MPA)

- **核心（深，1–3 年）**：建立并验证一套数字化 MPA 评估与自助干预工具包：生态瞬时评估 + 可穿戴生理指标 + 自适应音乐或 VR 暴露模块，先导试验 → 小样本 RCT。这是博士论文或基金级别的工作。
- **已查重的 spokes**：

| 面向 | 编号 | 题目 | 判定 | 周期 |
|---|---|---|---|---|
| 测量 | H10 | MPA 量表 COSMIN 综述 | 🟢 | 3–4 月 |
| 测量 | A4 | 生理指标 / 可穿戴与 MPA 系统综述 | 🟢 | 3–4 月 |
| 地图 | F10 | MPA 研究 40 年文献计量 | 🟢 | 2 月 |
| 干预证据 | N6 | 技术介导 MPA 干预范围综述 | 🟢 | 3–4 月 |
| 信息环境 | F2 | 聊天机器人 MPA 回答质量 | 🟢 已开题 | 2 月 |
| 信息环境 | F3 | 短视频平台 MPA 内容质量 | 🟢 | 2 月 |
| 机制 | N1 | AI 生成 vs 人类音乐对状态焦虑的在线实验 | 🟢 | 4–5 月 |
| 干预先导 | B1 | VR 暴露可行性研究 | 🟡 | 6–9 月 |

- **稳定落点期刊**：Medical Problems of Performing Artists（Q3，稳）、Psychology of Music（Q2）、Frontiers in Psychology Performance Science（Q2）、Musicae Scientiae。
- **优点**：spokes 最多、期刊最稳、不依赖临床机构；乐手群体易触达。

### Hub B：人工智能进入音乐治疗实践
Artificial intelligence in music therapy practice: evidence, competence and governance

- **核心（深）**：建立"负责任的 AI 整合"框架并以实证支撑：治疗师接受度调查 → 能力基准 → 框架 → 培训干预评估。
- **已查重的 spokes**：A1′ 临床实践范围综述 🟡、A3′ 治疗师接受度调查 🟢、C1 框架 🟢、F1 LLM 资格考试 🟢 已开题、F6 课程文件分析 🟢、F5 招聘广告分析 🟢、H3/H4 试验地图与报告质量（部分）🟢。
- **落点期刊**：Journal of Music Therapy（Q2）、Nordic Journal of Music Therapy、The Arts in Psychotherapy、JMIR 系列。
- **优点**：时效性强、引用增长快。**缺点**：窗口在收窄，竞争者多，调查类需伦理与招募。

## 四个核心工作也不需要伦理的 hub（2026-10-26 新增，已初步查重）

不需伦理的深核心只有四类来源：公开数据集上的计算研究、AI 输出的评估研究、文献与注册库的 meta 研究、以共同作者为评分者的专家评价。下面四个 hub 都满足。

### Hub C：面向教学的钢琴演奏计算评估
Computational, pedagogy-aligned assessment of piano performance

- **锚点**：钢琴表演 × 音乐教育 × AI / MIR
- **核心（深，1–2 年，零伦理）**：在公开数据集上建立"教师视角可解释"的钢琴演奏评估模型并验证：以 PercePiano（*Scientific Reports* 2024，1,202 段、19 个感知维度、专家标注）与 NeuroPiano（2024，学生练习曲录音 + 教师文字反馈与评分）为基准，输出按教学维度（节奏、触键、踏板、乐句、力度）分解的评分与可读反馈，并做跨曲目、跨水平的泛化与偏差分析。近邻：ISMIR 2024 "Piano Judges" 基准（音频编码器视角）、DLEPT 2026（Transformer 对比专家参考）。差异点：教学可解释性、与教师评语的对齐、公平性分析，而非只追求准确率。
- **spokes（全部零伦理）**：
  | 面向 | 题目 | 判定 | 周期 |
  |---|---|---|---|
  | 证据综合 | AI 自动演奏评估系统的效度与信度系统综述（H6） | 🟡 | 3–4 月 |
  | 数据审计 | 钢琴演奏评估公开数据集的"数据表"审计：标注质量、许可、人口学覆盖 | 🟢 待复核 | 2–3 月 |
  | 工具评价 | LLM 对学生演奏的文字反馈 vs NeuroPiano 教师反馈：自动与专家对比 | 🟢 待复核 | 3 月 |
  | 工具评价 | LLM 乐理分级考试阶梯与多模态输入（F1b） | 🟡 | 2–3 月 |
  | 信息环境 | 钢琴学习 App 用户评价挖掘（H1 子集） | 🟢 | 3 月 |
  | 开放科学 | 钢琴演奏评估研究的可复现性审计（代码、数据、模型可得性） | 🟢 待复核 | 2 月 |
  | 公平 | 评估模型在不同曲目、风格、演奏水平上的偏差分析 | 🟢 待复核 | 核心副产物 |
- **期刊**：Journal of New Music Research、IEEE Access、Applied Sciences、Computers and Education: Artificial Intelligence、Education and Information Technologies、Music & Science。
- **要求**：Python 与 GPU（PercePiano 规模小，普通 GPU 即可）；代码可由助手产出。

### Hub D：大语言模型作为音乐治疗与音乐教育的知识主体：评估科学
LLMs as knowledge agents in music therapy and music education: an evaluation science

- **锚点**：音乐治疗 × 音乐教育 × LLM
- **核心（深，1 年，零伦理）**：建立并公开首个音乐治疗 LLM 基准 MusicTherapyBench：专家编写的能力域题库（F1 的题库是第一版）+ 会诊式任务（评估摘要、疗程计划、文档撰写）+ 专家评分量规；跨模型、跨版本持续评测并发布排行榜。近邻：CounselBench（ICLR 2026，心理咨询）、HealthBench、2026 音乐理解问答基准（非临床）；音乐治疗专属基准为零。
- **spokes（零伦理，评分者为共同作者）**：F1 资格考试 🟢 已开题；F2 聊天机器人 MPA 回答 🟢 已开题；F3 短视频；LLM 生成疗程计划质量专家评价 🟢 待复核；LLM 撰写音乐治疗文献综述的引用幻觉率审计 🟢 待复核；LLM 对练习损伤与乐手健康问题的回答质量；F6 课程文件分析；F1b 乐理阶梯。
- **期刊**：JMIR Medical Education、JMIR Formative Research、Journal of Music Therapy、Nordic Journal of Music Therapy、Computers and Education: Artificial Intelligence。
- **要求**：2–3 名持证音乐治疗师共同作者；API 费用数百美元。

### Hub E：生成式 AI 与"治疗性音乐"的计算音乐学
Computational musicology of therapeutic music in the age of generative AI

- **锚点**：音乐治疗 × 生成式音乐 × 音频分析
- **核心（深，1 年，完全零伦理，无需评分者）**：建立"提示到治疗特征保真度"基准：用音乐治疗的既有参数（ISO 原则、约 60–80 BPM、低唤醒、可预测性、调式）构造提示，让 Suno、Udio、MusicGen 等生成针对焦虑、睡眠、痴呆、表演前准备的音乐，用 Essentia / librosa 提取特征，对照人类治疗性音乐语料与 Spotify 相关歌单（Scarratt 等 2023 已做睡眠歌单 22 万首，焦虑与表演前歌单未做），量化生成器是否"听懂"治疗性提示、同一提示的变异度、跨文化同质化。近邻：仅有商业评测博客与 2024 Prolific 感知实验；学术零。
- **spokes（零伦理）**：焦虑 / 专注 / 表演前歌单音频特征分析 🟢 待复核；生成器服务条款与临床使用政策分析 🟢 待复核；AI 生成"治疗歌曲"歌词内容分析；生成音乐文化同质性分析；A1′ 范围综述 🟡；生成式音乐治疗系统综述更新。
- **期刊**：Music & Science、Frontiers in Psychology、Applied Sciences、PLOS ONE、Musicae Scientiae、Journal of New Music Research。
- **注意**：Spotify 音频特征 API 2024 年 11 月起对新应用停用，特征需本地提取；生成器版权条款需核对。
- **要求**：Python、音频特征工具；生成器订阅费。

### Hub F：音乐干预与音乐教育研究的证据基础设施
Evidence infrastructure for music intervention and music education research

- **锚点**：音乐治疗 × 音乐教育 × meta 研究
- **核心（深，零伦理）**：建立并维护"音乐干预证据活地图"：注册库 + 文献的持续更新系统映射，用机器学习辅助筛选并验证其准确率。近邻：各医学领域活地图成熟，音乐领域无。
- **spokes**：H3 注册库分析、H4 报告质量、H10 量表综述、F7 开放科学审计、F10 文献计量，全部 🟢。
- **期刊**：Journal of Music Therapy、Research Synthesis Methods、Frontiers in Psychology、Systematic Reviews。

### 四个 hub 的比较
| | Hub C 钢琴评估 | Hub D LLM 评估 | Hub E 生成音乐 | Hub F meta 研究 |
|---|---|---|---|---|
| 核心零伦理 | 是 | 是（评分者为共同作者） | 是，连评分者都不需要 | 是 |
| 深度与辨识度 | 高 | 高，时效最强 | 高，几乎无人做 | 中，方法学身份 |
| spokes 数量 | 7 | 8 | 6 | 5 |
| 技术门槛 | Python + 小 GPU | API 调用 | 音频特征提取 | 数据清洗 |
| 外部依赖 | 公开数据集 | 2–3 名持证治疗师 | 生成器订阅 | 无 |
| 稳定落点 | JNMR、IEEE Access、EAIT | JMIR 系列、JMT | Music & Science、Frontiers | JMT、Frontiers |
| 最大风险 | MIR 社区竞争快 | 模型迭代快 | 版权条款、API 变动 | 被视为"不够实证" |

## 推荐
在四个零伦理 hub 中：锚在钢琴表演选 **Hub C**；锚在音乐治疗选 **Hub E**（成本最低、竞争最少）或 **Hub D**（时效最强）。Hub F 可作任一 hub 的副线。

原两个 hub 的判断保留如下。
**以 Hub A 为主纲领，Hub B 为副线。** 理由：Hub A 的八个 spokes 全部查重通过、六个不需伦理、落点期刊 Q3 稳收；核心工作可以逐步升级而不影响边缘产出。Hub B 保留 F1 和 A3′ 两篇，作为第二身份。

## Spoke 生成矩阵（`/idea-sweep` 使用）
对 hub 主题，按下面三轴枚举未覆盖的格子，每格生成一个 idea 并查重：

**面向（facet）**：测量 · 地图（计量 / 注册库）· 证据综合（综述 / 伞状）· 报告与开放科学审计 · 信息环境（聊天机器人 / 视频 / App）· 人群认知（调查 / 访谈）· 工具评价（App / 平台 / 模型基准）· 机制实验（在线 / 实验室）· 干预先导 · 概念与政策

**数据源 / 对象**：已发表文献 · 注册库 · 应用商店 · 社交媒体 · AI 模型输出 · 课程与政策文件 · 招聘广告 · 乐手 · 教师 · 治疗师 · 学生 · 特殊人群

**技术**：AI / LLM · 生成式音乐 · 可穿戴与生理 · VR / AR · App / 远程 · 机器人 · 无技术（基线）

未覆盖格子优先；每个 spoke 必须能在 2–5 个月内投稿，且与核心共享文献库或数据。
