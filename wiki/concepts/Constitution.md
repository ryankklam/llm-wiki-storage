---
type: concept
created: 2026-06-17
updated: 2026-06-17
sources: [2026-06-17-AI编程交付企业级项目SpecKit]
---

# Constitution

## 定义

**Constitution**（项目宪法）是 Spec-Kit 框架中的核心概念，指在项目根目录下创建的项目级规则文档。它是约束整个开发框架的"法律"，定义项目的架构设计、技术选型、代码规范等。在 Claude Code 中对应 CLAUDE.md，在 Cursor 中对应 rules.md。

## 核心特征

### 宪法内容

来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]

1. **核心原则**：构建当前项目必须遵循的原则
2. **额外约束**：技术栈版本号、代码规范、禁止项
3. **开发流程**：项目开发的标准流程定义
4. **治理方式**：如何管理和维护项目

### 约束范围

来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]

只要是使用 Spec-Kit，无论是内置驱动、扩展插件市场的新增能力，还是不同的 Preset 模板，都要遵循项目宪法。

### 宪法质量与输出质量的关系

Constitution 的质量直接决定 AI 在 Claude Code 驱动项目时的实际输出质量和必须遵循的规范。

## 关键信息

- Constitution 是写给 AI 的语言书，术语越精确、边界描述越清楚，AI 生成代码越规范（来源：[[2026-06-12-企业AI项目rules红线]]）
- Constitution 不是写给人看的，是写给 AI 在执行代码时看的约束（来源：[[2026-06-12-企业AI项目rules红线]]）

## 关联

- 相关概念：[[rules.md]]、[[CLAUDE.md]]、[[Spec-Kit]]、[[立宪法]]、[[AI项目规范]]、[[System Prompt]]
- 相关工具：[[Claude Code]]、[[Cursor]]
- 相关概念：[[红线规则]]、[[代码规范]]、[[工业级]]

## 开放问题

- Constitution 的最佳实践模板如何沉淀？
- 多项目共享 Constitution 的管理策略？
