# 方向评估：脑神经 × 音乐 × 计算机科学

评估日期：2026-11-03。结论先行：**有搞头，但要选对子方向。** 这个交叉里有一条线既深、又不需要招募、又正好缺人做：把现代音乐 AI 模型当"计算模型生物"，用公开神经数据检验它们与人脑的对齐，并用音乐专业度和治疗性状态作为调节变量。另外两条热线（EEG 重建音乐、闭环脑机音乐接口）一条太挤、一条需要伦理，不适合做核心。

## 七个子方向的热度与空白

| 子方向 | 近两年状态 | 竞争 | 空白 | 伦理 | 适合度 |
|---|---|---|---|---|---|
| 1. 音乐基础模型与大脑对齐（encoding / RSA） | *Nature Communications* 2025 用 MusicLM 的 MuLan 嵌入预测 fMRI；Brain2Music 2023 | 中，顶刊已占 fMRI | **MERT、MusicGen、Jukebox 嵌入对 EEG 的逐层编码无人做**；专业度（钢琴家 vs 非音乐家）如何调节对齐无人做 | 无（公开数据） | ★★★★★ |
| 2. 音乐期望模型 vs 神经反应（IDyOM vs Transformer） | eLife 2022 Music Transformer ≥ IDyOM；2025 arXiv 用扩散模型从音频估惊异度并预测 EEG | 中 | Anticipatory Music Transformer 等新模型未测；**专业度 × 模型类型**交互未做；多声部自然音乐上的对比少 | 无 | ★★★★ |
| 3. EEG 基础模型在音乐任务上的表现 | EEG-FM-Bench、OmniEEG-Bench 覆盖 54 个数据集，**无一音乐任务** | 低 | 全空白 | 无 | ★★★★ |
| 4. EEG 重建 / 解码音乐 | IEEE TMM 2026、arXiv 2026 通道导向 Transformer、潜扩散；跨被试仍近偶然 | **高，大组主导** | 泄漏感知评估、跨被试上限分析 | 无 | ★★（只做评估，不做模型） |
| 5. 闭环脑机音乐接口 / 情绪神经反馈 | 2025–2026 多个系统（极简 BCMI n=22、Neurophone、NeuroHarmonium、fMRI 神经反馈 2026）；2025 Frontiers 系统综述 | 中 | 生成式 AI 驱动的闭环系统、标准化评估协议 | **需要** | ★★★（系统设计 / 立场论文可做，实验留到后期） |
| 6. 消费级 EEG 解码音乐注意 / 投入度用于教育 | 2025 arXiv 四电极跨被试解码注意；2025 Technologies 综述给出框架 | 低 | 教学场景实证 | 需要 | ★★ |
| 7. 开放数据基准与可复现性 | 通用 EEG 基准多，音乐专用无 | 低 | 全空白 | 无 | ★★★★（Hub N 核心） |

## 为什么 1 + 2 + 3 + 7 是最优组合
- 四条线共用同一批公开数据（Di Liberto、OpenMIIR、MUSIN-G、NMED-T、MET、ds003720）和同一条预处理流水线。
- 每条线都能绑定一个音乐教育或治疗问题：专业度如何改变大脑与模型的对齐（教育）、治疗性状态下的对齐是否变化（治疗）。审稿人不会把它当纯方法比较。
- 顶刊已用 fMRI 做了 MusicLM；EEG 版本、更多模型、专业度调节是自然的后续，Q2 期刊会收。
- CS 社区做重建比拼模型，大组垄断；做"模型与脑的对齐"比拼问题设计，小团队有优势。

## 新增 spokes（并入 Hub N）
| 编号 | 题目 | 数据 | 判定 | 目标期刊 | 可发概率 |
|---|---|---|---|---|---|
| N-S9 | 音乐基础模型逐层嵌入对 EEG 的编码：MERT、MusicGen、Jukebox 与声学基线的对比，以及钢琴家 vs 非音乐家的对齐差异 | Di Liberto、NMED-T、MUSIN-G | 🟢 | Frontiers in Neuroscience / Journal of Neural Engineering / NeuroImage: Reports | 60–70% |
| N-S10 | 音频惊异度（扩散模型）vs 符号惊异度（IDyOM、Music Transformer）对自然音乐 EEG 的解释力，专业度调节 | Di Liberto、NMED-T | 🟢 / 🟡 | Cognitive Neurodynamics / Brain Sciences / Psychology of Music | 55–65% |
| N-S11 | 生成式 AI 驱动的闭环音乐神经反馈：设计空间、评估协议与音乐治疗适用性的立场论文 | 文献 | 🟡 | Frontiers in Human Neuroscience / Music & Science | 50–60% |
| N-S12 | EEG 重建音乐研究的评估协议审计：泄漏、跨被试与偶然水平报告（扩展 N-S1 到全部 EEG 音乐解码文献） | 文献 | 🟢 | Journal of Neuroscience Methods / Frontiers in Neuroinformatics | 65–75% |

## 期刊落点（CS 味更重时）
- Q2：Journal of Neural Engineering、Biomedical Signal Processing and Control、Neurocomputing、IEEE Access、Frontiers in Neuroscience、Cognitive Computation
- Q2–Q3：Brain Sciences、Frontiers in Human Neuroscience、Journal of Neuroscience Methods、Sensors
- 会议（不计 JCR 但有声望）：ISMIR、ICASSP、EMBC

## 门槛
- 需要会跑 PyTorch 与 MNE；提取 MERT / MusicGen 嵌入需一块 GPU（云租即可）
- 需要一位 EEG 方向合作者把关预处理
- 本会话环境无法下载数据集与模型权重，需在你本机或云机器执行

## 不建议
- 以 EEG 重建音乐为核心论文：大组垄断，跨被试近偶然，审稿人只看指标
- 以闭环系统实验为第一篇：需要伦理、设备与受试者，周期长
