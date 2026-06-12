---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# Tool Use

## 定义

**Tool Use（工具使用）**是 Agent 的基础能力层，指 LLM 调用外部工具（如文件读写、代码执行、API 调用等）的能力。在 AI 编程项目中，rules.md / CLAUDE.md 可以约束 AI 使用工具的范围和方式。

## 核心特征

### 与 rules.md 的关系
- Tool Use 是 Agent 的基础能力
- 允许使用哪些工具、如何使用，应在 rules.md 中明确
- 禁止项优先：先告诉 AI 不能用什么工具

## 关联

- 相关概念：[[Function Calling]]、[[Agent范式]]、[[rules.md]]、[[AI项目规范]]

## 开放问题

- 如何在 rules.md 中平衡工具使用的自由度与约束？
