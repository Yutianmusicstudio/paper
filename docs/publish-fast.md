# 快速发表手册（面向 JCR Q2–Q3）

综合自 `docs/resources.md` 第 4 节的来源与本领域实际情况。原则：**速度来自不返工，而不是走捷径。**

## 一、决定周期的五个变量

| 变量 | 慢 | 快 |
|---|---|---|
| 论文类型 | RCT、纵向研究 | 范围综述、文献计量、横断面问卷、可行性研究、短通讯 |
| 期刊模式 | 学会会刊，年出 4 期 | OA 连续出版（Frontiers、JMIR 系列、MDPI、Digital Health） |
| 稿件匹配 | 投稿后才看 Aims & Scope | 开题时锁定 3 本期刊，按第一志愿格式写 |
| 格式合规 | 投稿当天才看作者须知 | 先读须知，字数、引用格式、报告规范清单一次到位 |
| 返修速度 | 收到意见后搁置 | 48 小时内分类，1 周内返回逐条回复 |

经验值（来自搜索摘要，非官方承诺）：Q2 期刊整体 3–9 个月，Q3 期刊 2–6 个月；OA 期刊初审 2–3 周，首次外审决定 6–9 周；拒稿多在初审阶段，原因多为范围不符与格式不合。

## 二、16 周流程中的提速点

1. **选题（第 1 周）**：优先无需伦理的设计。范围综述与文献计量可以同周启动，问卷同周递交伦理。
2. **预注册（第 1–2 周）**：范围综述上 OSF，系统综述上 PROSPERO。审稿人看到注册号会少问一半方法问题。
3. **背景与方法先写（第 2–4 周）**：引言、方法不依赖结果，可在数据未到时完成大半。
4. **报告规范当写作提纲**：PRISMA-ScR / PRISMA 2020 / STROBE / CHERRIES 的清单项直接作为方法小节标题，用 `check-reporting` 核对。
5. **引用一次做对**：所有文献通过 `search-lit` 入库并带 DOI，初稿完成后跑 `verify-refs`。杜撰引用是 AI 时代最常见的直接拒稿原因。
6. **内审两轮**：`self-review` 模拟审稿人，`humanize` 与 `polish-language` 处理语言。许多 Q2–Q3 期刊审稿人对语言问题零容忍，但不会帮你改。
7. **投稿包一次备齐**：投稿信、报告规范清单、利益冲突、数据可用性、AI 使用声明、图表 300 dpi。缺一项就退回一轮，损失 1–2 周。
8. **拒稿即转投**：按 `outline.md` 里的备选期刊 48 小时内转投，顺手吸收已有审稿意见。

## 三、本领域的快通道期刊（投稿前复核最新 JCR）

| 用途 | 期刊 | 已知时效 |
|---|---|---|
| 范围综述、问卷、perspective | Frontiers in Psychology（Performance Science / Health Psychology 等专栏） | 初审约 16 天，外审决定约 61 天（第三方数据） |
| 可行性、先导、App 研究 | JMIR Formative Research、JMIR Serious Games、JMIR Mental Health | JMIR 系列以流程快著称，OA |
| 远程干预、数字健康 | Digital Health（SAGE） | OA |
| 教师 / 治疗师技术接受度 | Education and Information Technologies；International Journal of Human–Computer Interaction | 混合 OA |
| 音乐教育 | Music Educators Journal | 首次决定平均 28 天（SAGE 官方） |
| 艺术治疗 | The Arts in Psychotherapy | 2025 IF 1.7，单一来源称 Q2，需核实 |
| 音乐治疗 | Journal of Music Therapy | 2025 IF 2.3，Rehabilitation 46/175，推算 Q2 |
| 极快但需权衡声誉 | Healthcare、Behavioral Sciences（MDPI） | 2020 年数据首次决定中位 17.8 天 |

## 四、不要做的事

- 不投宣称"3 天发表""几乎不拒稿"的期刊；无审稿意见直接要求缴费的即为掠夺性期刊。
- 不把一项研究切成多篇低质量稿件（salami slicing），COPE 视为不端。
- 不用 AI 生成或"润色"出引用；所有引用必须 `verify-refs` 通过。
- 不在未读作者须知前写稿，格式不符会在初审被退回。
- 不为"刷快"放弃预注册与报告规范，这两项反而是缩短审稿轮次的最大杠杆。

## 五、与本仓库 skill 的对应

| 流程 | 命令 |
|---|---|
| 不知道先用哪个 | `/orchestrate` 描述任务 |
| 选刊 | `/find-journal` 粘贴摘要 |
| 检索建库 | `/search-lit`，再 `/manage-refs` |
| 起草 | `/paper-writer` 或 `/write-paper`；综述用 `/meta-analysis` |
| 投稿前 | `/check-reporting` → `/verify-refs` → `/self-review` → `/humanize` → `/polish-language` |
| 返修 | `/revise` 粘贴审稿意见 |
