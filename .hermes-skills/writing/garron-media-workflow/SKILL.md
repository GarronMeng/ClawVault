---
name: garron-media-workflow
version: 1.0.0
author: Garron
description: "STS 自媒体工作流。用于‘今天做什么内容’‘找热点选题’‘把热点做成我的内容’‘陌生化选题’。串联 aihotpicks / 实时热点、garron-topic-engine、garron-defamiliarized-topic、garron-insights-deepdive、garron-writing-style 和 garron-de-ai-writer。"
metadata:
  hermes:
    tags: [writing, social-media, topic, workflow, defamiliarization]
    related_skills: [garron-topic-engine, garron-defamiliarized-topic, garron-defamiliarization, garron-insights-deepdive, garron-writing-style, garron-de-ai-writer]
---

# STS 自媒体工作流

核心目标：把“今天大家在聊什么”变成“今天最值得讲什么，以及为什么这个角度值得由我来讲”。

```text
Hot Signal
  → Creator Fit
    → Familiar Proposition
      → Mechanism
        → Lens
          → Defamiliarized Topic
            → Real Asset
              → Insight Deepdive
                → Writing
                  → De-AI Review
```

## 1. 热点入口

优先使用 `aihotpicks` 获取实时热点候选。

如果当前 Agent 无法调用 `aihotpicks`，不要停工：使用实时 Web 搜索建立候选池，并保留 topic / source / date / trend signal / context。

热点只是输入，不直接决定最终选题。

## 2. 个人素材入口

同时调用 `garron-topic-engine` 检查：
- 最近 flomo / Daily Notes；
- 工作和公益经历；
- 最近对话、争论、失败和反常观察；
- `选题池.md` 中等待时机的题。

## 3. 陌生化选题

把热点候选与个人素材候选一起交给 `garron-defamiliarized-topic`。

只保留同时满足：
- 有时间窗口；
- 受众相关；
- 有真实材料；
- 有底层机制；
- 有可信陌生 Lens。

默认输出 3–5 个题，不批量堆标题。

## 4. 陌生化

对入选候选调用 `garron-defamiliarization`：

`熟悉命题 → A→B→C 机制 → Lens Scan → 同构测试 → 陌生表达 → 白话回译 → 真实材料 → 边界`

## 5. 深挖与成稿

用户选题后：
1. `garron-insights-deepdive`：追问、找论点、压力测试；
2. `garron-writing-style`：按目标平台和文章类型成稿；
3. `garron-de-ai-writer`：清理 AI 味与套路表达。

## 6. 默认输出

如果用户只说“今天做什么内容”，先交付：
- 今日最值得做的 3–5 个题；
- 每题的热点母题 / 熟悉说法 / 陌生 Lens / Hook / 真实材料入口 / 边界；
- 明确指出“今天只做一条”的首选。

不要未经确认直接生成大量完整稿件。

## 7. 快速触发语

- “跑一下今天的 STS 自媒体选题。”
- “今天只选一个最值得拍的题。”
- “把这几个热点做陌生化选题。”
- “不用热点，从我最近经历里找陌生化选题。”
- “把 #2 做成 90 秒短视频。”

## 8. 质量底线

- 热度 ≠ 选题；
- 陌生词 ≠ 陌生化；
- 类比 ≠ 因果；
- 不虚构个人经历、研究或数据；
- 医疗、金融、政治等高风险领域，事实边界优先于传播效果。
