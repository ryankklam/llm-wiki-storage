---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
---

# Tool Use

## 定义

**Tool Use（工具使用）**是 Agent 的基础能力层，指 LLM 调用外部工具（如文件读写、代码执行、API 调用等）的能力。在 AI 编程项目中，rules.md / CLAUDE.md 可以约束 AI 使用工具的范围和方式。

## 核心特征

### 与 rules.md 的关系
- Tool Use 是 Agent 的基础能力
- 允许使用哪些工具、如何使用，应在 rules.md 中明确
- 禁止项优先：先告诉 AI 不能用什么工具

### Tool Use 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

Tool Use 的可用工具列表与 Skill 路由面临相同的挑战：

- 当可用工具/Skill 数量过多时，模型需要在大量选项中选择
- 工具描述（类似 Skill Description）的清晰度直接影响选择准确率
- 可以通过分层组织工具（如 Skill Tree）、增加负样本描述、召回加重排等策略来优化
- Anthropic 的 Progressive Disclosure 思想同样适用于 Tool Use：先展示工具摘要，再决定是否加载完整参数 Schema

## 关联

- 相关概念：[[Function Calling]]、[[Agent范式]]、[[rules.md]]、[[AI项目规范]]、[[Skill路由]]、[[Skill]]、[[渐进式加载]]

## 开放问题

- 如何在 rules.md 中平衡工具使用的自由度与约束？
- 工具描述的最佳实践是否与 Skill Description 一致？
