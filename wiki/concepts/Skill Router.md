---
type: concept
created: 2026-06-17
updated: 2026-06-17
sources: [2026-06-17-AgentSkill过多4招提升命中]
tags: [Agent, Skill, Skill Router, 路由, Routing, 检索, LLM, 命中率, RAG]
---

# Skill Router

## 定义

**Skill Router（技能路由器）**是Agent系统中负责将用户请求映射到最合适Skill的组件。当Skill数量达到几百上千个时，Skill Router本身就演变成了一个检索系统，甚至需要专门训练模型来解决路由问题。

## 演化路径

| Skill数量 | 路由方式 | 复杂度 |
|----------|----------|--------|
| < 10个 | 直接匹配 / 简单规则 | 低 |
| 10-50个 | 语义匹配 / 关键词 | 中 |
| 50-200个 | 分层路由 / Skill Tree | 中高 |
| > 200个 | 召回重排 / 专门训练Router | 高 |

## 与检索系统的同构性

> 当Skill数量达到几百上千以后，Skill Router本身就已经变成了一个检索系统。

- **索引对象**：Skill的Name和Description
- **查询对象**：用户请求
- **匹配方式**：语义相似度 / 向量检索
- **精排方式**：LLM判断

## 研究方向

很多研究工作专门训练Skill Router来解决大规模Skill路由问题：
- 基于Embedding的语义路由
- 基于分类器的硬路由
- 基于LLM的软路由
- 混合路由策略

## 关联

- 相关概念：[[Skill路由]]、[[召回重排]]、[[RAG]]、[[Embedding]]、[[Skill Tree]]、[[分层路由]]
- 相关来源：[[2026-06-17-AgentSkill过多4招提升命中]]

## 开放问题

- Skill Router的最佳架构是什么？
- 如何评估Skill Router的准确率？
- 动态Skill生态下，Router如何实时更新？
