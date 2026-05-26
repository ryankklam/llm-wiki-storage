---
type: concept
created: 2026-05-26
updated: 2026-05-26
sources: [2026-05-26-抄作业Claude负责人演示]
---

# Cursor

## 定义

Cursor 是一款基于 AI 的代码编辑器，集成了 Claude 等大语言模型，提供智能代码补全、代码生成、代码解释等功能。它是当前流行的 AI 编程工具之一。

## 关键信息

### 产品定位
- AI 原生的代码编辑器
- 基于 VS Code 构建，兼容 VS Code 生态
- 深度集成 Claude、GPT 等大语言模型

### 与 Claude Code 的区别
| 特性 | Cursor | Claude Code |
|------|--------|-------------|
| 形态 | IDE 插件/编辑器 | 终端 CLI 工具 |
| 工作方式 | 编辑器内交互 | 命令行交互 |
| 适用范围 | 主要在 IDE 内 | 任何终端环境 |
| 工具链 | 预装 IDE 功能 | 可自定义工具 |

### Claude Code 的设计理念
根据 Boris 的分享，Claude Code 选择 CLI 而非 IDE 的原因：
1. **通用性**：终端是最大公约数，兼容所有 IDE 和工作流
2. **未来趋势**：模型能力快速进步，IDE 可能很快被取代
3. **灵活性**：不绑定特定编辑器，避免过度 UI 投资

## 关联
- 相关概念：[[Claude Code]], [[Coding Agent vs 日常任务Agent]], [[VS Code]]
- 相关实体：[[Claude]], [[Anthropic]]

## 开放问题
- Cursor 与 Claude Code 在实际开发效率上的对比
- 未来 IDE 和 CLI 工具的融合趋势
