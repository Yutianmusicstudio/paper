# 稿件大纲：Can large language models pass a music therapy board-style examination? Accuracy, consistency and error patterns across the CBMT competency domains

- **Slug**：llm-music-therapy-exam（看板编号 F1，主论文；乐理阶梯部分拆为配套论文 F1b）
- **类型**：LLM 基准评估（cross-sectional evaluation study，无人类受试者）
- **目标期刊**：1) JMIR Medical Education 2) Journal of Music Therapy 3) Nordic Journal of Music Therapy
- **字数上限**：JMIR Medical Education 无硬性上限，建议 4,000–6,000 词；表 ≤ 5
- **报告规范**：METRICS 清单（Sallam et al., 2024，LLM 健康评估研究）+ TRIPOD-LLM（2025）适用条目；预注册分析计划
- **预注册**：OSF Registries
- **伦理**：不需要（无人类参与者；题库作者与评分者均为共同作者）
- **查重状态**：🟡（2026-10-26；Pond & Fujinaga 2025 会议论文测过 RCM Level 6 乐理；音乐治疗资格考试维度无任何研究；期刊论文空缺）

## 研究缺口（≤ 3 句）
"大语言模型能否通过 X 资格考试"已成为医学教育的标准研究范式，覆盖从护理到放射治疗的几乎所有健康职业，但音乐治疗这一受监管的健康职业从未被测试。唯一相邻研究只测了一个级别的乐理考试，且是会议论文，用的是 2024 年的模型。音乐治疗考试同时考查音乐知识、临床推理和伦理判断，恰好能检验 LLM 在"音乐 + 临床"交叉领域的真实能力，而音乐治疗教育者和学生已在用这些工具备考，却没有证据说明其可靠性。

## 研究问题
- RQ1：主流 LLM 在覆盖 CBMT 五大能力域（安全与伦理、转介评估与治疗计划、治疗实施与终止、文档与评估、专业发展与职责）的板式题库上的准确率是多少，是否达到通过线？
- RQ2：准确率在能力域、题型（知识回忆 vs 临床情境推理）和模型之间如何差异？重复作答的一致性如何？
- RQ3：错误集中在哪些类型（音乐事实、临床判断、伦理边界、文化情境、幻觉式解释）？这对学生使用 LLM 备考和教师出题有何含义？

## 方法概要

### 题库构建（关键，决定可信度与版权安全）
- **不使用 CBMT 真题或其付费模拟题**，避免版权与考试诚信问题
- 由 2–3 名 MT-BC（共同作者）按 CBMT 2020 版考试内容大纲的域与子域比例编写 200 道单选题（四选一），每域按大纲权重分配；题型分两类：知识型 60%、临床情境型 40%
- 第三名 MT-BC 盲审每题的正确性、唯一正确答案与域归属；分歧讨论定稿；报告题库内容效度程序
- 若能获得 AMTA 或教材出版商书面许可，可补充公开出版的教材复习题作为次要题库做敏感性分析
- 题库随论文作为补充材料公开（CC BY），本身就是对教育界的贡献

### 模型与设定
- 封闭模型：OpenAI 最新 GPT 系列、Anthropic Claude 最新版、Google Gemini 最新 Pro；开源模型：一款可本地运行的主流开源模型（如 Llama 或 Qwen 当期版本）
- 每个模型记录精确版本号、API 日期；temperature 0；统一系统提示"你是参加音乐治疗资格考试的考生，只输出选项字母并给出两句解释"
- 每题独立会话，避免上下文泄漏；每题运行 3 次评估一致性
- 两种提示条件：零样本直接作答；要求先推理再作答（chain-of-thought）
- 全部调用脚本、原始输出存 `data/`，随论文公开

### 结局与分析
- 主要结局：总体准确率与 95% CI；以 CBMT 公布的合格线换算（约 70% 原始分的等价阈值，写明为近似）
- 次要：分域、分题型准确率；模型间比较（Cochran's Q + McNemar 配对）；三次运行一致性（Fleiss' kappa）；提示条件效应
- 错误分析：两名 MT-BC 对所有错题按预定义分类编码，报告 kappa；抽取典型"自信错误"案例
- 解释质量：对 40 道随机抽题，两名 MT-BC 盲评解释的正确性与教学价值（1–5 分）
- 图：各模型 × 各域准确率热图；题型 × 提示条件交互图；错误类型堆叠条形图

### 预计规模
- 200 题 × 4 模型 × 2 条件 × 3 次 = 4,800 次调用，API 成本约 20–50 美元

## 配套论文 F1b（另建目录，目标 Music Education Research）
- ABRSM 乐理 1–8 级公开历年试卷做难度阶梯；比较图像输入（乐谱截图，多模态）与文本编码（MusicXML / ABC）两种输入方式；对比 Pond & Fujinaga 2025 的单级别结果

## 预期贡献
- 实践：告诉音乐治疗学生与教师哪些域可以信任 LLM 辅助学习、哪些域会被误导；公开题库供教学使用
- 理论：首次测量 LLM 在"音乐 + 临床 + 伦理"交叉任务上的能力结构，为 A3′ 治疗师态度调查与 C1 框架提供实证锚点
- 方法：提供音乐治疗领域 LLM 评估的可复现流程与题库

## 风险与对策
- 题库效度被质疑 → 三人编写 + 盲审 + 按官方大纲权重；公开题库接受检验
- 模型迭代导致结果过时 → 写明"截至 X 日期的版本"，并公开脚本便于复测；投稿到决定通常 2–3 个月，选审稿快的期刊
- 被视为"又一篇 ChatGPT 考试论文" → 以错误分析与教学含义为重点，而非只报准确率；加入开源模型与一致性分析
- 版权 → 不碰真题；题库自建并开放

## 配套 skill 与工具
| 阶段 | 本仓库 skill | 外部工具 |
|---|---|---|
| 预注册 | — | OSF；CBMT 考试内容大纲（公开 PDF）；METRICS 清单 |
| 题库 | `/academic-writing-skills` 做题干与选项的语言一致性校对 | 共享表格；Google Forms 盲审 |
| 调用 | 会话内 `claude-api` skill 写 Anthropic 调用；其余按各家 SDK | Python 脚本（放 `data/`）；OpenAI / Google / Ollama API；固定随机种子与日志 |
| 分析与图 | 会话内 `dataviz` skill | R：`irr`（kappa）、`exact2x2`（McNemar）、ggplot2 热图 |
| 写作 | `/paper-writer`（Original Article；JMIR 结构：Background / Objective / Methods / Results / Conclusions 结构化摘要） | JMIR 作者须知与 METRICS 清单 |
| 质控 | `/check-reporting`（自建 METRICS 条目表）→ `/verify-refs` → `/self-review` → `/humanize` → `/polish-language` | — |
| 投稿 | `/find-journal` 复核；`/manage-refs` 出 Vancouver；`/sync-submission` | JMIR 投稿系统（有 APC，需确认经费） |
| 返修 | `/revise` | — |

## 时间表
| 周 | 任务 | 状态 |
|---|---|---|
| 1 | 确定 2–3 名 MT-BC 共同作者；OSF 预注册；按大纲分配出题任务 | 待开始 |
| 2–4 | 编写 200 题；第三人盲审；定稿题库 | |
| 5 | 调用脚本；试运行 20 题；冻结模型版本 | |
| 6 | 全量运行 4,800 次；存档原始输出 | |
| 7 | 自动评分；错误分类编码；解释质量盲评 | |
| 8 | 统计分析；三张图 | |
| 9 | Methods、Results 初稿 | |
| 10 | Introduction、Discussion、结构化摘要 | |
| 11 | 质控五步；语言两轮 | |
| 12 | 投稿 JMIR Medical Education；记录 submission-log | |
