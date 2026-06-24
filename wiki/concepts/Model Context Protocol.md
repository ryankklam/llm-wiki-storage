---
type: concept
created: 2026-05-26
updated: 2026-05-26
sources: [2026-05-26-抄作业Claude负责人演示]
---

# Model Context Protocol

## 定义

Model Context Protocol (模型上下文协议) 是一种开放协议，用于标准化 AI 模型与外部工具、数据源之间的交互方式。它让 AI Agent 能够安全、可控地访问和操作外部系统。

## 关键信息

### 设计目标
- **标准化**：统一工具调用的接口规范
- **安全性**：提供受控的工具访问机制
- **可扩展性**：支持各种第三方工具和服务集成

### 在 Claude Code 中的应用
- Claude Code 支持 MCP 工具，可以调用配置好的外部服务
- 用户可以在 `Claude.md` 中定义常用 MCP 工具的配置
- Claude 会自动学习如何使用这些工具来完成任务

### 与 Claude Code 工作流的结合
1. 在 `Claude.md` 中声明团队使用的 MCP 工具
2. Claude 在需要时会自动选择合适的工具
3. 工具执行结果会反馈到对话上下文中
4. Claude 可以基于反馈进行迭代优化

## 关联
- 相关概念：[[MCP]], [[Claude Code]], [[Tool Use]], [[Function Calling]], [[Agent]]
- 相关实体：[[Claude]], [[Anthropic]]

## 开放问题
- Model Context Protocol 的具体技术规范细节
- 与 OpenAI Function Calling 的兼容性
