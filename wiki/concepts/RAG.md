---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# RAG

## 定义

**RAG（Retrieval-Augmented Generation，检索增强生成）**是 AI 系统中结合外部知识检索与文本生成的技术。在 AI 编程项目中，rules.md / CLAUDE.md 可以约束 RAG 的使用方式、数据来源和检索策略。

## 核心特征

### 与 rules.md 的关系
- RAG 的证据会占用 Context Window 空间
- 在 rules.md 中应明确 RAG 的使用优先级
- 数据来源的可信度约束应在规则中明确

## 关联

- 相关概念：[[Context Window]]、[[Prompt工程]]、[[rules.md]]、[[AI项目规范]]

## 开放问题

- 如何在 rules.md 中规范 RAG 的使用策略？
