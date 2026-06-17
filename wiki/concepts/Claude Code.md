---
type: concept
created: 2026-05-10
updated: 2026-06-17
sources: [2026-05-10-skill实战- 从0到1写一个你自己的skill, 2026-06-12-企业AI项目rules红线, 2026-06-17-AI编程交付企业级项目SpecKit]
---

# Claude Code

## 定义

**Claude Code**是 Anthropic 推出的 Coding Agent 产品，基于 Claude 大语言模型，支持通过项目根目录下的 CLAUDE.md 文件进行项目级规则约束。Claude Code 本身是一个黑盒，需要通过 Spec-Kit 等文档驱动框架来让人类掌控整个开发进度。

## 关键信息

- Claude Code 的 CLAUDE.md 本质与 rules.md、Cursor Rules 相同，都是立给 AI 的项目规则文件（来源：[[2026-06-12-企业AI项目rules红线]]）
- 是 Coding Agent 的代表产品之一（来源：[[2026-05-10-skill实战- 从0到1写一个你自己的skill]]）
- Claude Code 是 Spec-Kit 框架的主要适配工具之一，通过 Agent 注册中心进行集成（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）
- Claude Code 本身是命令行工具，Cursor 本质也是命令行之壳封装了可视化 IDE 环境（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）

## 关联

- 相关产品：[[Claude]]、[[Cursor]]、[[Codex]]
- 相关概念：[[Coding Agent vs 日常任务Agent]]、[[rules.md]]、[[CLAUDE.md]]、[[Spec-Kit]]、[[Constitution]]、[[AI编程交付]]
