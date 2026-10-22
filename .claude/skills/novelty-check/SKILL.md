---
name: novelty-check
description: 对一个论文 idea 做快速查重查新（查重、查新、novelty check、has this been done、是否已有人做过、看板更新）。拆解对象 / 技术 / 论文类型，跑两轮网页检索与注册库检索，按 🟢🟡🔴 判定并输出可粘贴到 docs/idea-board.md 的记录。适用于科技 × 音乐治疗 / 音乐教育 / 音乐表演方向。
---

# novelty-check

输入：一个 idea（一句话即可）。输出：判定 + 近邻证据 + 差异化建议，格式见下。

## 步骤

1. **拆解**：写出 对象 / 技术 / 论文类型 三要素。缺哪个就按最可能的补上并注明。
2. **第一轮检索（宽）**，并行发 3 条 WebSearch（extended 模式）：
   - `<对象> <技术> scoping review OR systematic review 2024 2025 2026`
   - `<对象> <技术> bibliometric OR survey OR randomized 2025 2026`
   - 中文：`<对象> <技术> 综述 OR 调查 2025 2026`
3. **第二轮检索（窄）**：对第一轮找到的每篇最近邻，用其题名关键词 + 作者再搜一次；并搜 `PROSPERO <关键词>`、`OSF registries <关键词>`、`clinicaltrials.gov <关键词>`。
4. **判定**：
   - 🔴 近 2 年同类型 + 同对象 + 同技术的同行评审论文已发表
   - 🟡 有相邻论文但类型 / 对象 / 角度不同，或只有摘要、预印本、学位论文、方案
   - 🟢 两轮均未发现同类型论文
5. **输出**（直接可粘贴到 `docs/idea-board.md`）：

```
### <编号> <🟢/🟡/🔴> <题目>
- 近邻：<论文（年份、期刊、样本/篇数、链接）>；…
- 空白：<一句话>
- 建议角度：<一句话>
- 目标期刊：<3 本，参考 docs/target-journals.md>
- 下一步：<预注册 / 检索 / 伦理>
```

6. 若判定为 🟢，提醒用户立即在 OSF 或 PROSPERO 预注册占位。
7. 把记录追加到 `docs/idea-board.md` 对应位置，并在优先队列表中增减行。

## 注意
- 网页搜索覆盖不全，🟢 要注明"开题前需在 PubMed / Scopus / PROSPERO 复核"。
- 学术 API 若可用（见 `docs/novelty-check.md` 第 5 节），优先用 `/search-lit` 做检索。
- 不编造近邻论文；找不到就写"未发现"。所有近邻都附链接。
