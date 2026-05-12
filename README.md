# ClawVault

你的个人知识库，由 OpenClaw / Hermes 助手维护。

它不是单纯的 Obsidian 仓库，而是一个面向长期复利的「第二大脑 + 写作操作系统」：

- 用 Daily Notes 捕捉真实生活与工作现场；
- 用 Projects / Areas 管理长期议题；
- 用 Resources 沉淀方法论；
- 用 `.hermes-skills/` 把方法论转化为可被 AI 调用的工作流；
- 用 Templates 把每天、每周、每篇文章变成可复盘的闭环。

---

## 📂 结构

- **Daily Notes/**：每日日记，按日期命名
- **Projects/**：进行中的项目，每个项目独立笔记
- **Areas/**：责任领域（职业、健康、家庭等）
- **Resources/**：参考资料、模板、方法库、写作系统索引
- **Archives/**：归档旧笔记
- **Templates/**：模板文件
- **.hermes-skills/**：Hermes / Agent 可调用的技能与方法论

---

## ✍️ 写作系统

ClawVault 已沉淀一套完整写作链路：

```text
选题引擎
  → 洞察挖掘
    → 写作风格系统
      → 去 AI 味
        → 存档 + 复盘
```

对应文件：

| 阶段 | 文件 | 作用 |
|---|---|---|
| 选题 | `.hermes-skills/writing/garron-topic-engine/SKILL.md` | 从经历、flomo、热点中发现可写话题并评分 |
| 洞察 | `.hermes-skills/writing/garron-insights-deepdive/SKILL.md` | 用苏格拉底式追问挖出真正论点 |
| 写作 | `.hermes-skills/writing/garron-writing-style/SKILL.md` | 规定文章类型、结构、语气、节奏和自检标准 |
| 去 AI 味 | `.hermes-skills/writing/garron-de-ai-writer/SKILL.md` | 初稿完成后做禁用词、句式、信息密度和语感清理 |
| 复盘 | `Templates/Writing Review.md` | 记录每篇文章的效果、反馈和下一轮迭代 |

建议从 `Resources/写作系统索引.md` 开始看，它是这套写作方法论的入口地图。

---

## 🔄 日常工作流

### 每日

1. 用 `Templates/Daily Note.md` 记录：完成、目标、待办、日志、随想、学习、健康、反思。
2. 把有情绪、有问题、有冲突的碎片标记为潜在选题。
3. 不急着写文章，先保留现场感。

### 每周

1. 用 `Templates/Weekly Review.md` 回顾本周目标、完成、亮点、挑战、下周计划。
2. 从 Daily Notes 里挑出 3-5 个可发展素材。
3. 用 `garron-topic-engine` 给选题打分。

### 写文章

1. 如果不知道写什么：先用 `garron-topic-engine`。
2. 如果有主题但没想透：用 `garron-insights-deepdive`。
3. 如果论点和素材已经清楚：用 `garron-writing-style`。
4. 初稿完成后：必须用 `garron-de-ai-writer` 过一遍。
5. 发布或存档后：用 `Templates/Writing Review.md` 复盘。

---

## 🚀 开始使用

1. 打开 Obsidian 桌面版
2. 选择 `Open folder as vault`
3. 浏览到 `~/Desktop/ClawVault` 并打开
4. 从 `Daily Notes/` 记录当天素材
5. 从 `Resources/写作系统索引.md` 进入写作系统

所有笔记支持双链 `[[...]]`，可以自由链接。

---

## 🧭 Agent 使用原则

Agent 不应该直接替 Garron 决定观点。

它的职责是：

- 帮助发现素材；
- 追问真实体验；
- 挑战模糊论点；
- 提供结构和备选表达；
- 检查 AI 味和逻辑漏洞；
- 把结果存档成可复用资产。

最终创意决策由人完成。

由 Claw 维护 🦾
