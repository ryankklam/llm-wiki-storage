---
type: concept
created: 2026-06-12
updated: 2026-06-19
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中, 2026-06-19-Agent记忆管理别只答向量库加RAG]
---

# RAG

## 定义

**RAG（Retrieval-Augmented Generation，检索增强生成）**是 AI 系统中结合外部知识检索与文本生成的技术。在 AI 编程项目中，rules.md / CLAUDE.md 可以约束 RAG 的使用方式、数据来源和检索策略。

## 核心特征

### 与 rules.md 的关系
- RAG 的证据会占用 Context Window 空间
- 在 rules.md 中应明确 RAG 的使用优先级
- 数据来源的可信度约束应在规则中明确

### 与 Skill 路由的同构性

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

Agent Skill 路由与 RAG 的核心思路完全一致：

| 维度 | RAG | Skill 路由 |
|------|-----|-----------|
| 召回对象 | 文档片段 | Skill Description |
| 召回方法 | Embedding / 关键词 | Embedding / 关键词 |
| 重排方法 | LLM 生成答案 | LLM 选择 Skill |
| 核心思想 | 先缩小范围，再精加工 | 先缩小范围，再精判断 |

当 Skill 数量达到几百上千以后，Skill Router 本身就变成了一个检索系统。先用 Embedding 或关键词检索召回 Top 10，再交给大模型做最终判断，这就是典型的 RAG 两阶段架构。

## 关联

- 相关概念：[[Context Window]]、[[Prompt工程]]、[[rules.md]]、[[AI项目规范]]、[[Skill路由]]、[[召回重排]]、[[Embedding]]、[[向量检索]]

## 开放问题

- 如何在 rules.md 中规范 RAG 的使用策略？
- Skill 路由能否直接复用 RAG 的成熟基础设施？
