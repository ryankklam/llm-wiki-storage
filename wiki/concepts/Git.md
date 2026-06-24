---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# Git

## 定义

**Git**是 AI 编程项目中的版本控制工具。在 AI 辅助开发流程中，Specate 等工具内置 Git 分支管理，每个新需求当作 Feature 通过独立 Git 分支处理。rules.md / CLAUDE.md 可以约束 AI 的 Git 操作规范。

## 核心特征

### AI 项目中的 Git 规范
- **分支策略**：每个 Feature 独立分支
- **提交规范**：commit message 格式约束
- **禁止项**：禁止直接提交到主分支等红线规则

### 与 rules.md 的关系
- Git 操作规范应在 rules.md 中明确
- 插件市场可安装 Git 相关操作扩展
- 版本控制约束是项目规范的一部分

## 关联

- 相关概念：[[版本控制]]、[[GitHub]]、[[rules.md]]、[[AI项目规范]]

## 开放问题

- 如何让 AI 遵循团队的 Git 工作流规范？
