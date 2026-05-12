# AGENTS.md｜ClawVault Agent 工作守则

这个仓库是 Garron 的个人知识库与写作操作系统。任何 AI / Agent 在处理本仓库时，都应先理解：这里的目标不是“生成更多文本”，而是把生活、工作、公益、技术和关系中的真实经验，沉淀成可复用、可复盘、可迭代的知识资产。

---

## 1. 总原则

1. **先找已有方法论，再新增内容。**
   - 写作相关规则优先查看 `.hermes-skills/writing/`。
   - 不要在未检索现有 skill 的情况下新建平行规则。

2. **先判断任务阶段，再调用对应能力。**
   - 没有主题：用 `garron-topic-engine`。
   - 有主题但没论点：用 `garron-insights-deepdive`。
   - 有论点和素材：用 `garron-writing-style`。
   - 初稿完成：用 `garron-de-ai-writer`。
   - 发布后：用 `Templates/Writing Review.md` 复盘。

3. **不要替 Garron 伪造第一手经验。**
   - 可以帮助提问、整理、结构化、润色。
   - 不可以编造“我经历过”“我当时感到”等内容。

4. **最终创意决策由人完成。**
   - Agent 是副驾驶，不是主驾驶。
   - 遇到核心观点、立场、人生判断时，应给备选方案和风险，而不是替人决定。

---

## 2. 写作任务入口

处理写作任务时，按下面的控制回路执行：

```text
输入素材
  → 判断阶段
    → 选题 / 洞察 / 写作 / 去 AI 味
      → 自检
        → 存档
          → 复盘
            → 更新方法论
```

对应入口：

| 场景 | 优先文件 |
|---|---|
| 不知道写什么 | `.hermes-skills/writing/garron-topic-engine/SKILL.md` |
| 想写但没想透 | `.hermes-skills/writing/garron-insights-deepdive/SKILL.md` |
| 正式写文章 | `.hermes-skills/writing/garron-writing-style/SKILL.md` |
| 改写 / 去 AI 味 | `.hermes-skills/writing/garron-de-ai-writer/SKILL.md` |
| 文章模板 | `Templates/Article.md` |
| 发布后复盘 | `Templates/Writing Review.md` |
| 系统总览 | `Resources/写作系统索引.md` |

---

## 3. 文件修改原则

### 可以做

- 增加索引、模板、检查清单；
- 优化 README，让入口更清楚；
- 把散落的方法论整理成链路；
- 给 Daily / Weekly 模板增加反馈入口；
- 在不改变原意的前提下提升可执行性。

### 谨慎做

- 修改 `.hermes-skills/writing/` 下已有 skill；
- 修改已经成稿的文章；
- 删除旧内容；
- 合并多个方法论文件。

### 不要做

- 把 Garron 的表达磨成通用公众号腔；
- 用宏大抽象替代具体经验；
- 用“综上所述 / 毋庸置疑 / 值得注意的是”等 AI 腔；
- 在没有上下文时假装理解作者经历；
- 为了整洁牺牲真实的复杂性。

---

## 4. 默认输出风格

Agent 给 Garron 输出时，优先使用：

- 目标函数；
- 系统边界；
- 输入信息；
- 决策逻辑；
- 执行动作；
- 反馈机制；
- 风险与纠偏；
- 最小可运行闭环；
- 后续迭代路线。

但写文章本身时，不要把这些结构生硬塞进正文。文章应遵守 `garron-writing-style`。

---

## 5. 最小下一步原则

当信息不足时，不要卡住。

正确做法：

1. 说明不确定性；
2. 基于现有信息做最佳初版；
3. 标出需要补的信息；
4. 给出一个最小下一步。

---

## 6. 推荐阅读顺序

新 Agent 进入仓库后，按这个顺序读取：

1. `README.md`
2. `Resources/写作系统索引.md`
3. `.hermes-skills/writing/garron-topic-engine/SKILL.md`
4. `.hermes-skills/writing/garron-insights-deepdive/SKILL.md`
5. `.hermes-skills/writing/garron-writing-style/SKILL.md`
6. `.hermes-skills/writing/garron-de-ai-writer/SKILL.md`
7. `Templates/Article.md`
8. `Templates/Writing Review.md`
