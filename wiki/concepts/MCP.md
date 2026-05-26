---
type: concept
created: 2026-05-26
updated: 2026-05-26
sources: [2026-05-26-抄作业Claude负责人演示]
---

# MCP

## 定义

MCP (Model Context Protocol) 是一种标准化的协议，用于让 AI Agent 与外部工具进行交互。它允许 Claude 等 AI 助手调用各种工具和服务，扩展其能力边界。

## 关键信息

### 核心作用
- 标准化工具接口，让 AI 能够以统一方式调用不同工具
- 支持 Bash 工具、API 调用、数据库查询等多种工具类型
- 可以在 `Claude.md` 中配置常用 MCP 工具

### 使用方式
1. **直接告知**：告诉 Claude 关于工具的信息，它会自动学习如何使用
2. **Claude.md 配置**：将常用工具配置写入项目根目录的 `Claude.md` 文件
3. **动态发现**：Claude 可以使用 `--help` 等命令自行学习工具用法

### 与 Bash 工具的关系
- MCP 是更高层次的抽象和标准化
- Bash 工具是底层实现方式之一
- Claude Code 同时支持 Bash 工具和 MCP 工具

## 关联
- 相关概念：[[Model Context Protocol]], [[Claude Code]], [[Tool Use]], [[Agent]]
- 相关实体：[[Claude]]

## 开放问题
- MCP 与 Function Calling 的具体区别和联系
- MCP 生态中第三方工具的标准化程度
