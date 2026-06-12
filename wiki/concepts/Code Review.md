---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# Code Review

## 定义

**Code Review（代码审查）**在 AI 编程时代，不仅是人类开发者之间的相互检查，还包括通过 rules.md / CLAUDE.md 等规则文件对 AI 生成代码的事前约束。没有红线的规则文件，到 Code Review 阶段才发现 AI 动了不该动的地方，代价巨大。

## 核心特征

### AI 时代的 Code Review
- **事前约束 > 事后检查**：rules.md 立在工程最前面，比后面任何补救都管用
- **红线规则**：明确禁止项，防止 AI 在 Code Review 前就越界
- **量化验证**：每条规则能量化、能验证，减少 Review 时的主观判断

### 常见 AI 导致的 Code Review 问题
来源：[[2026-06-12-企业AI项目rules红线]]

- 明明有现成代码，偏要新建一份
- 保留的东西顺手改了
- 动了不该动的地方，到 Code Review 才发现

## 关键信息

- 没有红线的 rules.md 等于没 rules.md。没卡红线，代码越写越容易崩。到 Code Review 哪天才发现一堆动了不该动的地方。（来源：[[2026-06-12-企业AI项目rules红线]]）
- 好的 rules.md 能让你立刻判断：是 AI 的问题，还是写 rules.md 的人一开始就写错了对象

## 关联

- 相关概念：[[rules.md]]、[[CLAUDE.md]]、[[红线规则]]、[[AI项目规范]]
- 相关流程：[[CI/CD]]、[[自动化]]、[[测试]]

## 开放问题

- AI 生成的代码如何与人工 Code Review 流程高效结合？
- 能否让 AI 自动执行 Code Review 规则？
