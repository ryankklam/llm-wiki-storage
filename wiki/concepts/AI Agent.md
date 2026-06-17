---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
---

# AI Agent

## 定义

**AI Agent**是能够自主执行任务的 AI 系统。在 AI 编程语境下，Coding Agent（如 Claude Code、Cursor）需要 rules.md / CLAUDE.md 等规范文件来约束其行为边界，确保代码生成符合项目要求。

## 核心特征

### Coding Agent 的规范约束
来源：[[2026-06-12-企业AI项目rules红线]]

- AI Agent 聪明不等于听话
- 需要通过 rules.md 明确行为边界
- 禁止项优先于允许项

### 与 rules.md 的关系
- rules.md 是约束 AI Agent 行为的"宪法"
- 没有红线的规则等于没规则
- 好的规范让 AI Agent 从碰运气变成稳定可控

### AI Agent 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

当 AI Agent 拥有的 Skill 数量从几个增长到上百个时，路由成为关键挑战：

- **问题表现**：明明有对应 Skill，模型却不用；或者用了错误的 Skill
- **本质原因**：Skill 路由从简单匹配变成了检索问题
- **解决思路**：优化 Skill 描述、建立 Skill Tree 分层路由、增加负样本、引入召回加重排
- **大型系统实践**：很多大型 AI Agent 系统都在做分层路由，而不是一次性全量匹配

## 关联

- 相关概念：[[Coding Agent vs 日常任务Agent]]、[[Claude Code]]、[[Cursor]]、[[rules.md]]、[[Skill路由]]、[[Skill]]、[[Skill Tree]]、[[分层路由]]
- 相关范式：[[Agent范式]]、[[Tool Use]]、[[Function Calling]]

## 开放问题

- 如何设计适合不同 AI Agent 的通用规则模板？
- Skill 数量规模化后，Agent 的架构应如何演进？
