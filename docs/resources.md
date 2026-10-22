# 资源索引：论文 skill、插件与参考资料

更新：2026-10-22。网络策略只放行 GitHub，所以网页类文章仅凭搜索摘要整理，投稿前请自行打开核对。

## 1. 已装进本仓库的 skill（`.claude/skills/`，打开仓库即可用）

| 阶段 | skill | 用法 | 来源 |
|---|---|---|---|
| 路由 | `orchestrate` | 描述任务，它分派到下面的 skill | medsci |
| 选刊 | `find-journal` | 给摘要，返回按范围匹配排序的期刊、AI 披露政策、拒稿后备选链 | medsci |
| 检索 | `search-lit` / `fulltext-retrieval` | PubMed、Semantic Scholar 检索，只纳入 API 可核实的文献并生成 BibTeX | medsci |
| 写作 | `paper-writer` | 建项目目录、IMRAD 分节文件、文献矩阵，按 PRISMA / STROBE / CONSORT 走流程；含 desk-rejection-prevention、journal-selection、word-count-limits 等参考 | kgraph57 |
| 写作 | `write-paper` | 8 阶段从大纲到可投稿初稿 | medsci |
| 写作 | `academic-writing-skills` | 跨学科：扩展大纲、分段起草、证据与主张强度对齐、术语一致 | WenyuChiou |
| 综述 | `meta-analysis` | PROSPERO 协议、检索、筛选、偏倚风险、合并、森林图、PRISMA 报告 | medsci |
| 样本 | `calc-sample-size` | 决策树选检验，给出可复现 R/Python 代码和伦理申请用的论证文字 | medsci |
| 引用 | `verify-refs` / `manage-refs` | 对 PubMed、CrossRef、OpenAlex 核对每条引用，标记 FABRICATED / MISMATCH | medsci |
| 合规 | `check-reporting` | 49 种报告规范逐条审计（PRISMA 2020、STROBE、CONSORT、COREQ 等） | medsci |
| 自审 | `self-review` / `paper-review` | 模拟审稿人给出 Major / Minor 意见 | medsci / WenyuChiou |
| 润色 | `humanize` / `polish-language` | 去 AI 腔（27 种模式）；非母语英语一致性校对 | medsci |
| 返修 | `revise` | 给审稿意见编号、分类，生成逐条回复与投稿信 | medsci |
| 投稿 | `sync-submission` | 投稿材料同步与核对 | medsci |
| 审稿 | `peer-review` | 替别人审稿时用 | medsci |

许可证与来源见 `.claude/skills/NOTICE.md`。

## 2. 可一键启用的 claude.ai 插件（已在对话中弹出安装卡片）

- **research-superpowers**：idea → literature → ingest → analysis → draft → peer-review → publication 全链路，支持质性 / 量化 / 混合方法。
- **Research Desk**：核实引用真伪、忠实笔记、对比论文、从自己的文献写 related work、裁判式评审。
- **Citation Needed**：对草稿中每条事实性陈述做在线核证，输出证据账本，不擅自改写。
- **wiley-scholar-gateway**：Wiley 的学术文献 MCP。
- 另有 **Liner**（学术搜索与带引用回答）、**read-paper**（中英双语精读报告）、**letX**（LaTeX 编译）、**Academic PDF Translation**。

## 3. 未装入但值得了解的 GitHub skill

| 仓库 | 亮点 | 为什么没装 |
|---|---|---|
| [Imbad0202/academic-research-skills](https://github.com/imbad0202/academic-research-skills) | `sr-screener`：按方案做题录 / 全文双盲筛选 + 仲裁，输出 PRISMA 计数、kappa、RIS；`academic-paper-reviewer` 5 席审稿团 | CC BY-NC，含 PreToolUse 钩子，48 MB。可用 `/plugin marketplace add Imbad0202/academic-research-skills` |
| [taoyunudt/literature-review-skill](https://github.com/taoyunudt/literature-review-skill) | 中文文献综述五步法与段落模板 | 无许可证 |
| [lingzhi227/agent-research-skills](https://github.com/lingzhi227/agent-research-skills) | 31 个 skill，含 novelty-assessment、rebuttal-writing、survey-generation | 无许可证，偏计算机方向 |
| [O0000-code/awesome-academic-skills](https://github.com/O0000-code/awesome-academic-skills) | 223 个学术 skill 的索引，按研究生命周期分类，标注许可证与是否联网 | 索引，不是 skill |
| [Aperivue/medsci-skills](https://github.com/Aperivue/medsci-skills) 全集 | 54 个，含 `analyze-stats`、`make-figures`、`design-study` | 只选了 16 个；全集用 `npx medsci-skills install` |
| [keemanxp/slr-prisma](https://github.com/keemanxp/slr-prisma) | PRISMA 2020 系统综述脚手架 | 许可证不明 |
| [yorkeccak/scientific-skills](https://github.com/yorkeccak/scientific-skills) | 13 个数据源的自然语言文献检索 | 需联网 API |
| [cookjohn/cnki-skills](https://github.com/cookjohn/cnki-skills) | 驱动知网检索 | 无许可证，需浏览器 |
| [momo2young/humanize-academic-writing](https://github.com/momo2young/humanize-academic-writing) | 社科文本去 AI 痕迹 | 功能与 `humanize` 重叠 |

## 4. 关于快速发表的文章（搜索摘要，未逐篇打开）

英文：
- Springer Nature Author Services：[12 essential tips for faster manuscript publication](https://authorservices.springernature.com/featured-articles/top-tips-for-faster-manuscript-publication/)
- AJE：[12 Tips for Accelerating Manuscript Publication](https://www.aje.com/arc/12-tips-accelerating-manuscript-publication)
- Smart Science Career：[How to write faster: 19 efficient ways](https://smartsciencecareer.com/how-to-write-faster/)
- Editage：[Journals and publishers that offer rapid publication](https://www.editage.com/insights/a-list-of-journals-and-publishers-that-offer-rapid-publication)
- Manusights：[Average review times across 100 journals in 2026](https://manusights.com/blog/average-review-times-100-journals-2026)（中位首次决定约 37.5 天，样本偏高影响因子期刊）
- Paul Silvia, *How to Write a Lot*（APA, 2nd ed. 2018）：固定写作时段，不等"有空再写"
- Frontiers in Psychology 第三方数据：初审约 16 天，首次外审决定约 61 天（[Pubrica](https://pubrica.com/academy/journals-templates/frontiers-in-psychology/)，未注明采集日期）
- Music Educators Journal（SAGE）：投稿到首次决定平均 28 天（[期刊主页](https://journals.sagepub.com/home/mej)）

中文：
- 艾思科蓝：[SCI 论文投稿选刊原则](https://www.ais.cn/news/featured/32872)、[发表一篇 SCI 要多久](https://www.ais.cn/news/featured/31895)
- 知乎：[SCI 论文发表最快多长时间](https://zhuanlan.zhihu.com/p/655710954)、[SCI 论文有哪些类型](https://zhuanlan.zhihu.com/p/685387037)、[哪些 SCI 期刊可以发综述](https://zhuanlan.zhihu.com/p/571008495)、[sci 期刊论文综述很难发吗](https://zhuanlan.zhihu.com/p/25583748384)
- [SCI 期刊审稿周期大揭秘：5 个真实案例 + 6 个技巧](https://www.kotoon.com/blog/sci-review-cycle-guide.html)
- [怎么快速发表 SCI？缩短发表周期的七个实战技巧](https://www.global-meetings.com/headerLine/read/2192)
- 警惕：搜索中出现的"3 天发表""几乎不拒稿的二区期刊"均为商业推广页面，可信度低。

## 5. 本领域近期的同类论文（用于定位缺口与模仿结构）

- Tong et al. (2026) *Journal of Artificial Intelligence and Soft Computing Research*：AI in Music 的文献计量 + 系统综述，覆盖创作、表演、教育。DOI 10.2478/jaiscr-2026-0010
- *Research Studies in Music Education*（2026-06 在线）：AI 在课堂音乐教学的范围综述（教学策略与学习结果）
- Mazlan et al. (2025) ICAIE 会议：AI 在音乐教育的文献计量 + 范围综述。DOI 10.1109/ICAIE64856.2025.11158139
- Arcagok et al. (2025) *Yegah Musicology Journal*：AI 音乐教育文献计量（土耳其语）
- **缺口**：搜索未见"AI × 音乐治疗"的范围综述或文献计量，对应选题库 A1 仍是空白。
