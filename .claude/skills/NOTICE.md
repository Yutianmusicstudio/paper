# 第三方 skill 来源与许可证

本目录下的 skill 复制自以下开源仓库（均为 MIT 许可证，各目录内附 LICENSE）。
升级时重新从上游复制，不要在本地修改后忘记记录。

| 目录 | 上游 | 版本/日期 | 说明 |
|---|---|---|---|
| `paper-writer/` | https://github.com/kgraph57/paper-writer-skill | 2026-10 clone | IMRAD 全流程；路径已由 `~/.claude/skills/` 改为 `.claude/skills/` |
| `academic-writing-skills/`, `paper-review/` | https://github.com/WenyuChiou/academic-writing-skills | 2026-10 clone | 跨学科写作、审稿式评审；删除了 >300 KB 的示例图片 |
| `find-journal/` `check-reporting/` `verify-refs/` `self-review/` `revise/` `humanize/` `polish-language/` `calc-sample-size/` `meta-analysis/` `search-lit/` `write-paper/` `manage-refs/` `peer-review/` `sync-submission/` `fulltext-retrieval/` `orchestrate/` | https://github.com/Aperivue/medsci-skills (v6.1.0) | 2026-10 clone | 仅选取与综述、问卷、投稿相关的 16 个；`analyze-stats` 未复制，需要时上游安装 |

未复制（许可证限制或无许可证，仅链接）：
- https://github.com/Imbad0202/academic-research-skills （CC BY-NC 4.0；含 `sr-screener` 系统综述筛选，可用 `/plugin marketplace add` 安装）
- https://github.com/taoyunudt/literature-review-skill （无许可证；中文文献综述五步法）
- https://github.com/lingzhi227/agent-research-skills （无许可证；偏计算机方向）
