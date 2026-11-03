# Hub N 规划：开放神经数据上的音乐学习与音乐干预计算神经科学

Open-data computational neuroscience of music learning and music-based intervention

制定：2026-11-03。周期 24 个月。全部基于公开去标识神经数据集的二次分析，不招募受试者；多数机构只需伦理委员会出具"非人类受试者研究"认定函，开题前申请一次即可。

## 1. 为什么这个 hub 比前面的"评价类"更深
前面几批的主体是审计、信息质量、文献综述，贡献在"整理"。这个 hub 的贡献在"发现与方法"：用神经数据回答音乐教育与音乐治疗各自最核心的一个问题。
- 音乐教育：训练如何改变大脑对音乐的预测与想象（expectation、audiation）？能否从 EEG 读出一个人的音乐训练水平？
- 音乐治疗：音乐诱发的情绪与状态变化在脑电上有没有可靠、可跨数据集复制的标记？哪些标记临床可以信？
两个问题都有现成公开数据，且现有文献要么只把数据当分类基准（OpenMIIR），要么只分析过一次（Di Liberto），要么刚发布没人用（MET）。

## 2. 已核实的公开数据资产
| 数据集 | 内容 | 许可 | 现状 | 对本 hub 的用途 |
|---|---|---|---|---|
| OpenMIIR（Stober 2015） | 10 人，64 导，12 段音乐分三组：有歌词 / 同曲无歌词 / 纯器乐；感知 + 3 种想象条件，每条件 5 次重复 | PDDL 公有领域 | 被当作解码基准十年；2026 预印本证明跨被试泛化很弱；**歌词条件对想象可解码性的影响从未报告** | 想象（audiation）研究；歌词脚手架效应 |
| Di Liberto 2020（eLife，Dryad） | 10 非音乐家 + 10 专业钢琴家，64 导，巴赫单声部旋律，30 试次 | CC0 | 2024 年一篇用 IDyOM 做了跨频带再分析；**无 Transformer 期望模型分析，无"从 EEG 预测专业度"分析** | 专业度神经标记；期望编码 |
| MET（Cheang，澳门大学，2026） | 20 人 × 20 次听乐，128 导（DataPort 版 8 导，OpenNeuro ds008701 版 66 导），每次含**听前 / 听中 / 听后**三段 + SAM 情绪评分 | 待核对（OpenNeuro 默认 CC0） | 2026 年刚发布，**几乎无人复用** | 音乐诱发状态变化；ISO 原则计算检验 |
| OSF 音乐情绪调节 EEG（2024） | 15 人，32 导，静息 → 悲伤自传回忆 → 听音乐，附情绪与应对评分 | 待核对 | 几乎无复用 | 最接近音乐治疗范式的公开数据 |
| MUSIN-G（ds003774） | 20 人（非音乐家），12 首跨流派，熟悉度与喜爱度评分 | CC0 | 2026 一篇用于喜爱度回归 | 多数据集复制的第三个来源 |
| ds002725 | 21 人 EEG-fMRI 同步，情感音乐 | CC0 | 少量复用 | 多数据集复制 |
| NMED-T / NMED-H | 20 人 / 12 人，自然音乐 | 学术使用 | 用于曲目识别 | 基准任务 |
| ds003720 + Brain2Music | 5 人 fMRI，GTZAN 十流派 | CC0 | 重建研究 | 可选 |
| DEAP | 32 人，音乐视频 | 学术使用 | 被过度使用 | 仅作对照 |

未发现公开的钢琴演奏 EEG / fNIRS 数据集；2025 年一篇钢琴专业 vs 非专业 fNIRS 研究未公开数据。

## 3. 论文地图

### 核心（深）
| 编号 | 题目 | 类型 | 目标期刊 | 投稿月 | 可发概率 |
|---|---|---|---|---|---|
| N-CORE-1 | MusicEEG-Bench: a leakage-aware, cross-dataset benchmark for decoding music perception, imagery, affect and expertise from open EEG | 基准 + 方法 | Journal of Neural Engineering（备选 Frontiers in Neuroscience、IEEE TNSRE） | 第 14 月 | 55–65% |
| N-CORE-2 | Do EEG markers of music-induced affect replicate across open datasets? A pre-registered multi-dataset study | 多数据集复制 | Psychophysiology 或 Frontiers in Human Neuroscience | 第 9 月 | 65–75% |

### 边缘（全部公开数据，已初步查重）
| 编号 | 题目 | 数据 | 类型 | 目标期刊 | 投稿月 | 可发概率 | 判定 |
|---|---|---|---|---|---|---|---|
| N-S1 | OpenMIIR 十年：解码研究的评估协议、泄漏与可复现性系统审计 | 文献 | meta 研究 | Frontiers in Neuroinformatics / Journal of Neuroscience Methods | 第 3 月 | 70–80% | 🟢 |
| N-S2 | 开放音乐神经数据集的 FAIR 与复用审计：许可、BIDS 合规、文档、引用复用率 | 数据集元数据 | 审计 | Scientific Data（Comment）/ Frontiers in Neuroinformatics | 第 4 月 | 65–75% | 🟢（数据集综述已有，复用审计无） |
| N-S3 | 歌词是否为音乐想象提供脚手架：OpenMIIR 有词 / 无词 / 器乐条件下想象可解码性的泄漏感知再分析，以 audiation 理论解读 | OpenMIIR | 二次分析 | Psychology of Music / Music & Science / Brain Sciences | 第 6 月 | 60–70% | 🟢 |
| N-S4 | 从神经期望追踪读出音乐专业度：Transformer 惊异度 vs IDyOM 对钢琴家与非音乐家 EEG 的解释力与分类 | Di Liberto | 二次分析 | Frontiers in Neuroscience / Cognitive Neurodynamics / Brain Sciences | 第 8 月 | 60–70% | 🟢（Transformer 角度）/ 🟡（专业度效应已知） |
| N-S5 | 音乐诱发的状态转换：MET 听前 / 听中 / 听后三段的 EEG 变化与乐曲特征的关系，ISO 原则的计算检验 | MET + 音频特征 | 二次分析 | Frontiers in Human Neuroscience / Brain Sciences / Music & Science | 第 11 月 | 60–70% | 🟢 |
| N-S6 | 悲伤诱导后的音乐情绪调节：OSF 数据集的再分析与 MET 的交叉验证 | OSF + MET | 二次分析 | The Arts in Psychotherapy / Frontiers in Psychology | 第 13 月 | 55–65% | 🟢 待复核 |
| N-S7 | EEG 基础模型（LaBraM 等）在音乐任务上的零样本与微调表现 | 多数据集 | 方法 | Journal of Neural Engineering / Biomedical Signal Processing and Control | 第 16 月 | 55–65% | 🟢 待复核 |
| N-S8 | 公开数据二次分析在音乐神经科学中的伦理与报告规范：立场论文 | 文献 | 概念 | Music & Science / Frontiers in Neuroscience | 第 18 月 | 50–60% | 🟡 |

两年合计：核心 2 篇 + 边缘 8 篇；第一年投出 5 篇。

## 4. 四个阶段
### 阶段 0（第 0–1 月）：环境与认定
- 向伦理委员会申请"公开去标识数据二次分析，非人类受试者研究"认定函（一次覆盖全 hub）
- 本地或云端 Python 环境：MNE、MNE-BIDS、mne-bids-pipeline、scikit-learn、PyTorch；下载并校验所有数据集，记录版本与哈希
- 建 GitHub 仓库 `musiceeg-bench/`：统一预处理、留一被试交叉验证、置换检验、跨数据集迁移的模板

### 阶段 1（第 1–6 月）：审计 + 第一篇二次分析
- N-S1 文献审计（第 1–3 月）：检索所有引用 OpenMIIR 的论文，编码评估协议（随机切分 vs 留一被试）、是否报告偶然水平与置换检验、代码可得性、报告准确率；这既是论文，也是基准设计依据
- N-S2 数据集 FAIR 审计（第 2–4 月）
- N-S3 OpenMIIR 歌词条件再分析（第 3–6 月）：复用 2026 预印本公开的泄漏感知流水线，加入条件对比

### 阶段 2（第 6–12 月）：专业度与情绪两条线
- N-S4 Di Liberto 再分析（第 6–8 月）：用公开的音乐 Transformer 计算逐音惊异度与熵，与 IDyOM 对比；TRF 编码；LOSO 分类钢琴家 vs 非音乐家并报告置换检验
- N-CORE-2 多数据集情绪标记复制（第 6–9 月）：预注册假设（额叶 alpha 不对称、alpha / theta 功率、beta 等）；在 MET、OSF、ds002725、MUSIN-G 上统一流程检验，报告每个标记的跨数据集一致性
- N-S5 MET 状态转换（第 9–11 月）

### 阶段 3（第 12–24 月）：基准与扩展
- N-CORE-1 基准（第 12–14 月）：整合前面所有流水线，定义四类任务、统一指标、排行榜
- N-S6、N-S7、N-S8（第 13–18 月）
- 第 20–24 月：以基准与结果申请基金，进入需伦理的自采数据阶段（如钢琴学习者纵向 EEG）

## 5. 共用资产
| 资产 | 首次产生于 | 复用于 |
|---|---|---|
| 统一预处理与 BIDS 转换脚本 | 阶段 0 | 所有 |
| 留一被试 + 置换检验评估模板 | N-S3 | N-S4、N-S5、N-CORE |
| 音乐 Transformer 惊异度提取 | N-S4 | N-S5、N-CORE |
| 音频特征提取（tempo、mode、energy、roughness） | N-S5 | N-CORE-2、Hub E |
| 情绪标记计算库 | N-CORE-2 | N-S5、N-S6 |
| 审计编码表 | N-S1、N-S2 | N-S8 |

## 6. 资源与门槛
- 技能：Python 信号处理与机器学习；助手可写全部代码，你需要能跑并核对
- 算力：常规分析 CPU 即可；N-S7 与基础模型微调需一块 GPU（云端按小时租用可行）
- 合作者：强烈建议一位有 EEG 经验的共同作者（神经科学或 BCI 方向），审稿人会看方法细节
- 经费：数据免费；GPU 租用数百美元；OA 费视期刊
- 网络：本会话环境无法下载数据集，需在你本机或可联网的云机器上跑；可通过 Remote Control 让助手直接在你电脑的文件夹里工作

## 7. 风险与对策
| 风险 | 对策 |
|---|---|
| 样本小（10–20 人），效应弱 | 全部用置换检验与留一被试；把"不泛化"本身当结果写，2026 预印本已示范 |
| 审稿人质疑二次分析新意 | 每篇绑定一个音乐教育或治疗理论问题（audiation、expectation、ISO），不做纯方法比较 |
| 数据集许可与伦理 | 开题前核对每个数据集许可；取得非人类受试者认定函；论文写明 |
| MET 的 OpenNeuro 版本与 DataPort 版本通道数不同 | 用 OpenNeuro 66 导版本；方法中写明 |
| 工具链学习成本 | 从 N-S1、N-S2 两篇不需信号处理的审计起步，并行学 MNE |

## 8. 里程碑
| 月 | 里程碑 |
|---|---|
| 1 | 认定函；数据集下载校验；仓库骨架 |
| 3 | N-S1 投稿 |
| 6 | N-S2、N-S3 投稿 |
| 9 | N-CORE-2 投稿（预注册在第 6 月） |
| 12 | N-S4、N-S5 投稿；预计 2 篇录用 |
| 14 | N-CORE-1 投稿 |
| 24 | 累计 10 篇投出，预计 5–7 篇录用；基金申请 |
