---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
---

# Function Calling

## 定义

**Function Calling（函数调用）**是 LLM 调用外部函数的能力，是 Agent 基础能力层的重要组成部分。在 AI 编程项目中，rules.md / CLAUDE.md 可以约束 AI 如何、何时使用 Function Calling。

## 核心特征

### 与 rules.md 的关系
- Function Calling 的能力由模型提供
- 何时、如何调用由 rules.md 约束
- 工具使用规范应在项目规则中明确

### Function Calling 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

Function Calling 的底层机制与 Skill 路由密切相关：

- 每个 Skill 通常对应一个或多个 Function
- 当 Skill 数量过多时，模型需要在大量 Function 描述中进行选择
- 这本质上就是 Skill 路由问题：模型通过 Function 的 Name 和 Description 来决定调用哪个 Function
- 优化 Function 描述的区分度、增加负样本、分层组织 Function，都能提升 Function Calling 的命中率

## 关联

- 相关概念：[[Tool Use]]、[[Agent范式]]、[[rules.md]]、[[AI项目规范]]、[[Skill路由]]、[[Skill]]

## 开放问题

- 如何在 rules.md 中规范 Function Calling 的使用？
- Function Calling 的 Schema 描述如何像 Skill Description 一样优化？
