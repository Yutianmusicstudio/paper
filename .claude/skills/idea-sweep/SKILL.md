---
name: idea-sweep
description: 选题挖掘循环（idea sweep、批量出 idea、自动查重、跑一夜选题、围绕 hub 找边缘论文、spoke 生成）。仿 karpathy/autoresearch 的 program.md 循环：读 docs/idea-sweep-program.md，按 facet × source × tech 矩阵枚举未覆盖格子，每格生成一个 idea，跑两轮查重，按规则打分，保留或丢弃，追加到 docs/idea-log.tsv，循环到预算用完，不中途问人。
---

# idea-sweep

## 设置（每次运行开始）
1. 读 `docs/idea-sweep-program.md`：取 hub、参数块、矩阵、已覆盖格子、评分规则。
2. 读 `docs/research-program.md` 了解 hub 的核心与现有 spokes。
3. 读 `docs/idea-log.tsv` 末尾 50 行与 `docs/idea-board.md` 标题，建立"已存在 idea"集合，避免重复。
4. 若 `docs/idea-log.tsv` 不存在，创建并写表头：
   `date	id	hub	facet	source	tech	title	verdict	ethics	months	probability	status	nearest_neighbor	note`
5. 确认参数后直接进入循环，不等人确认。

## 循环（直到本次 budget_per_run 用完）
1. **选格子**：从矩阵中挑一个当前 hub 下未覆盖、且与核心共享文献或数据的 facet × source × tech 组合。优先快文体（综述、审计、信息质量、基准、注册库、公开数据）。
2. **生成 idea**：一句话题目 + 对象 / 技术 / 论文类型三要素 + 设计 + 伦理需求 + 预计月数。
3. **查重**：按 `/novelty-check` 的两轮流程，并行发 3 条 WebSearch（宽），再对最近邻发 1–2 条（窄）。网络只放行网页搜索时，🟢 要注明"需 PubMed / PROSPERO 复核"。
4. **打分**：按程序文件的评分规则得判定与概率。
5. **记录**：无论保留或丢弃，都向 `docs/idea-log.tsv` 追加一行（制表符分隔，描述内不用逗号与制表符）。status 为 `keep` 或 `discard`。
6. **保留的**：按 `docs/idea-board.md` 的记录格式追加到看板末尾新建的"## sweep 候选（日期）"小节，并在 `docs/idea-sweep-program.md` 的"已覆盖格子"追加该格子。
7. **丢弃的**：只记日志，并在"已覆盖格子"追加，避免下次再试。
8. 回到第 1 步。

## 结束
- 预算用完后：在日志末尾不写总结行；改为在对话中输出一张表（保留的 idea、判定、概率、周期）与本次覆盖的格子数，并执行 `git add docs/ && git commit` 推送（提交信息：`idea-sweep: <日期> <保留数>/<尝试数>`）。
- 若用户要求"跑到被打断为止"，忽略 budget_per_run，持续循环；每 10 个 idea 提交一次。

## 硬规则
- 不编造近邻；每个近邻附链接；找不到就写"未发现"。
- 不在循环中途问人；遇到网络失败重试一次后记 `discard` 并注明"检索失败"。
- 一个格子只生成一个 idea；同一 idea 不重复查重。
- 不把同一数据源切成多个题目（salami）；同一数据源的不同研究问题最多保留 2 个。
- 概率是判断估计，日志与看板都要注明。
