---
title: 写作系统总入口
category: 写作管理
tags: [写作系统, 来源审计, Agent]
status: active
updated: 2026-05-18
---

# 写作系统总入口

这个目录用于整理 ClawVault 的写作系统，核心原则是：

> 先分清来源，再谈风格。

过去的问题是，仓库里同时存在三类内容：

1. Garron 真实写过的文章和朋友圈；
2. AI 对真实文本的蒸馏、归纳和规则化；
3. AI 为测试流程生成的草稿、示例和模板。

如果不分层，Agent 很容易把第 2 / 3 类误当成 Garron 的原始文风，最后写出“像 AI 以为的 Garron”，而不是 Garron。

---

## 1. 使用顺序

处理写作任务时，按这个顺序读取：

```text
来源审计
  → 真实原文
    → AI 蒸馏资产
      → anti-pattern
        → 生成 / 改写
          → 复盘回填
```

不要反过来。尤其不要只读风格规则，不读真实原文。

---

## 2. 文件分层

### A. 真实原文层

这些是最可信的风格来源。

| 类型 | 文件 |
|---|---|
| 文章 | `审美是创作者的诅咒.md` |
| 文章 | `加密通讯.md` |
| 文章 | `当AI学会替你动手/01-效率的幻觉.md` |
| 文章 | `当AI学会替你动手/03-手感的消亡.md` |
| 文章 | `当康复被写进国家标准.md` |
| 朋友圈原文 | `Resources/life-flow-samples.md` 中标注为“原文”的部分 |

### B. AI 蒸馏资产层

这些不是 Garron 原文，而是对原文的分析、标签、规则和使用说明。

| 文件 | 作用 |
|---|---|
| `Resources/风格样本库.md` | AI 蒸馏后的推进机制和句子机制 |
| `Resources/life-flow-samples.md` | 生活流样本，含用户原文和 AI 分析 |
| `Resources/style-calibration.md` | 风格指纹和校准规则 |
| `Resources/开头结尾样本库.md` | 开头 / 结尾结构库 |
| `Resources/禁用表达清单.md` | 低级 AI 味清理规则 |
| `Resources/anti-patterns.md` | 高级 AI 味和伪风格识别 |

### C. 工作流与模板层

这些是执行工具，不是风格来源。

| 文件 | 作用 |
|---|---|
| `Templates/Article.md` | 文章生产模板 |
| `Templates/Writing Review.md` | 文章复盘模板 |
| `Templates/Daily Note.md` | 每日素材记录 |
| `Templates/Weekly Review.md` | 每周素材汇总 |
| `.hermes-skills/writing/*` | Hermes 技能定义 |
| `AGENTS.md` | Agent 工作守则 |

### D. 任务队列层

这些是选题、候选任务和状态管理，不是原文。

| 文件 | 作用 |
|---|---|
| `选题池.md` | 选题任务队列 |

---

## 3. 关键规则

### 3.1 原文优先级最高

当 AI 蒸馏资产和真实原文冲突时，以真实原文为准。

### 3.2 分析不能冒充风格

`为什么有效`、`可复用结构`、`不能滥用` 这类内容都是 AI 分析，不是 Garron 文风。

Agent 不能模仿这些分析段落的语气。

### 3.3 测试稿不能入库为样本

AI 生成的测试初稿、示范段落、模拟朋友圈，不能直接进入“真实样本”。

除非 Garron 明确说：

> 这版我发了，而且反馈很好。

才可以作为高可信样本。

### 3.4 朋友圈与长文分开调用

朋友圈 / 旅行 / 日常观察，优先调用：

1. `Resources/life-flow-samples.md`
2. `Resources/style-calibration.md`
3. `Resources/anti-patterns.md`

长文 / 思辨 / 公共评论，优先调用：

1. 真实文章原文
2. `Resources/风格样本库.md`
3. `.hermes-skills/writing/garron-writing-style/SKILL.md`

---

## 4. 当前清理任务

- [x] 建立来源审计入口
- [x] 明确真实原文层 / AI 蒸馏层 / 工作流模板层 / 任务队列层
- [ ] 给样本库加 provenance 标注
- [ ] 给 AGENTS.md 增加来源审计规则
- [ ] 给 README.md 增加写作系统分层说明
- [ ] 把可能被误认为原文的 AI 分析内容标明为 AI-derived
