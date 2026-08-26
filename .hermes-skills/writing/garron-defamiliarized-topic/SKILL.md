---
name: garron-defamiliarized-topic
version: 1.0.0
author: Garron
description: "自媒体陌生化选题 subskill。将热点、个人素材和 garron-topic-engine 候选转成少量高潜力陌生化选题。"
metadata:
  hermes:
    tags: [writing, topic, defamiliarization, social-media]
    related_skills: [garron-topic-engine, garron-defamiliarization, garron-insights-deepdive]
---

# 自媒体陌生化选题器

目标：找到“正在发生 × 受众在意 × 有真实材料 × 存在机制同构”的选题。

## 输入优先级
1. `aihotpicks` 实时热点候选；
2. `garron-topic-engine` 的个人素材 / flomo / 选题池候选；
3. 实时 Web 搜索；
4. 用户手动提供的新闻、热点、评论区问题或主题。

热点必须记录日期与来源；热点排序不直接继承。

## Gate
每个候选检查：
- 时效；
- 受众相关；
- 是否有真实经历、专业经验、数据、案例或长期观察；
- 是否存在可解释的底层机制；
- 是否能落到具体场景、冲突、数字或决策。

只有热度高，其他弱：不推荐。

## 机制与陌生化
1. 先写一句已经被说烂的“熟悉命题”。
2. 再写 `A → B → C` 底层机制。
3. 调用 `garron-defamiliarization` 扫描至少 5 个 Lens。
4. 至少两个现实映射点成立，才允许保留 Lens。

## Topic Score
- 时效性 20
- 受众相关 20
- 真实资产 20
- 陌生化潜力 20
- 可讲述性 15
- 可验证性 5

风险扣分：纯蹭热点 -20；需要虚构故事 -30；理论映射牵强 -25；高风险事实不确定 -30；与长期定位冲突 -15。

默认只推荐总分 ≥70 的 3–5 个题。

## 输出
每题包含：
- 热点母题
- 为什么值得做
- 熟悉说法
- 陌生 Lens 与机制映射
- 稳妥版 / 传播版 / 强钩子版选题
- 前 3–5 秒 Hook
- 可调用的真实材料
- `Hook → Reality → Mechanism → Story → Insight → Boundary`
- 风险边界

最后明确：如果今天只做一条，做 #X，并解释原因。

## Anti-Slop
- 不随机挑学科硬套；
- 不把类比写成因果；
- 不创造伪学术概念；
- 不虚构研究、数据或第一人称经历；
- 不批量生产几十个同质标题；
- 高风险领域以事实准确优先。

## Handoff
选题确认后，将原命题、底层机制、推荐 Lens、真实素材、平台、受众、Hook 交给 `garron-insights-deepdive` 继续追问和结构设计。
