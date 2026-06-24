---
type: entity
created: 2026-05-10
updated: 2026-05-26
sources: [2026-05-10-skill实战- 从0到1写一个你自己的skill, 2026-05-25-Anthropic内部Prompt写法, 2026-05-26-抄作业Claude负责人演示]
---

# Claude

## 定义

Claude 是 Anthropic 开发的大语言模型系列，包括 Claude 3.5 Sonnet、Claude 3 Opus 等多个版本，以强大的推理能力、长上下文窗口和安全性著称。

## 关键信息

### 产品形态
- **Claude 模型**：通过 API 调用的基础大模型
- **Claude Code**：AI 编程助手（命令行工具）
- **Claude.ai**：网页版对话界面

### 技术特点
- **长上下文**：支持 200K+ tokens 的上下文窗口
- **多模态**：支持图片、文档等多种输入格式
- **工具使用**：支持 Function Calling、MCP 等工具调用协议
- **安全性**：Constitutional AI 训练，减少有害输出

### 在 Anthropic 内部的使用
- 80% 技术人员每天使用 Claude Code
- 用于代码编写、代码审查、问题解答、自动化任务
- 研究人员使用 Notebook 工具进行 ML 实验

### Prompt 最佳实践（Anthropic 官方）
- 使用 XML tags 结构化 Prompt
- 区分角色、指南、政策、数据
- 指令不增加能力，需要计算时给工具
- 使用评估套件驱动开发

## 关联
- 相关概念：[[Claude Code]], [[Anthropic Prompt技巧]], [[MCP]], [[Model Context Protocol]], [[Prompt工程]]
- 相关实体：[[Anthropic]]

## 开放问题
- Claude 4 的发布时间线和能力预期
- Claude Code 是否会开源
