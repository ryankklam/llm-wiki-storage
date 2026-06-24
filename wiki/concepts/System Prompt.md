---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# System Prompt

## 定义

**System Prompt（系统提示词）**是发给大模型的底层指令，用于设定 AI 的角色、行为边界和全局约束。在 AI 编程工具中，项目级的 System Prompt 通常以 rules.md 或 CLAUDE.md 的形式持久化存储在项目根目录下。

## 核心特征

### 层级结构
- **对话级 System Prompt**：单次会话生效，临时约束
- **项目级 System Prompt**：以 rules.md / CLAUDE.md 形式存在，持久约束
- **工具级 System Prompt**：如 Specate 的 Constitution，整合工具链规范

### 与 rules.md 的关系
- rules.md / CLAUDE.md 本质上是**项目级的 System Prompt**
- 比单次对话的 Prompt 更持久、更系统
- 是工业级 AI 项目管理的基石

## 编写原则

来源：[[2026-06-12-企业AI项目rules红线]]

1. **禁止项优先** — 先告诉 AI 别做什么
2. **量化可验证** — 每条规则附"为什么"
3. **控制长度** — 500 字以内，防止 AI 漏项
4. **术语精准** — 是写给 AI 的语言书，不是写给人看的

## 关键信息

- System Prompt 不增加能力，需要计算时给工具（来源：[[2026-05-25-Anthropic内部Prompt写法]]）
- 项目级的 System Prompt（rules.md）让管 AI 的方式从碰运气变成稳定可控（来源：[[2026-06-12-企业AI项目rules红线]]）

## 关联

- 相关概念：[[Prompt]]、[[Prompt工程]]、[[rules.md]]、[[CLAUDE.md]]
- 相关规范：[[AI项目规范]]、[[Prompt工程规范]]

## 开放问题

- 如何衡量 System Prompt 的有效性？
- 不同模型的 System Prompt 兼容性如何处理？
