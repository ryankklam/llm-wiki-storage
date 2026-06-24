---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AI编程交付企业级项目SpecKit]
---

# CLAUDE.md

## 定义

**CLAUDE.md 是 Claude Code 工具中的项目规则文件**，功能上等同于通用的 rules.md 或 Cursor 的 Cursor Rules。它是放置在项目根目录下的 Markdown 文档，用于向 Claude AI 定义项目规范、行为边界和技术约束。在 Spec-Kit 框架中，CLAUDE.md 是 Constitution（项目宪法）在 Claude Code 中的具体体现。

## 核心特征

### 技术定位
- **工具专属**：Claude Code 的默认规则文件名
- **功能等价**：与 rules.md、Cursor Rules 本质相同
- **加载方式**：Claude Code 自动读取项目根目录下的 CLAUDE.md

### 文件内容
- 项目定位（是什么、不是什么）
- 技术栈及具体版本号
- 代码规范与复用策略
- 禁止项（红线规则）
- 质量约束

## 与 rules.md 的关系

| 文件名 | 工具 | 本质 |
|--------|------|------|
| CLAUDE.md | Claude Code | 项目规则文件 |
| rules.md | 通用/社区惯例 | 项目规则文件 |
| Cursor Rules | Cursor | 项目规则文件 |

三者本质都是**同一份东西**——立给 AI 的项目规则文件（来源：[[2026-06-12-企业AI项目rules红线]]）。

## 编写原则

来源：[[2026-06-12-企业AI项目rules红线]]

1. **先写清项目不是什么** — 定义边界比定义范围更有效
2. **量化可验证** — 每条规则附"为什么"
3. **做和不做都列清楚** — 不留模糊地带
4. **技术栈写版本号** — 如 React 19、Tailwind CSS v4
5. **压在 500 字以内** — 控制长度防止 AI 漏项

## 关键信息

- CLAUDE.md 是 Claude Code 的"项目宪法"，AI 执行任何操作前都必须先服从（来源：[[2026-06-12-企业AI项目rules红线]]）
- 术语越精确、边界描述越清楚，AI 生成代码越规范
- 不是写给人看的，是写给 AI 在执行代码时看的约束

## 关联

- 相关概念：[[rules.md]]、[[System Prompt]]、[[Prompt工程]]、[[Claude Code]]、[[Constitution]]、[[Spec-Kit]]
- 同功能文件：Cursor Rules、.cursorrules
- 相关工具：[[Claude Code]]
- 相关流程：[[立宪法]]、[[AI编程交付]]

## 开放问题

- CLAUDE.md 与 Claude 的 System Prompt 如何协同？
- 多项目共享的 CLAUDE.md 模板如何管理？
