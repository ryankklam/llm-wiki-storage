---
type: concept
created: 2026-05-10
updated: 2026-05-26
sources: [2026-05-10-skill实战- 从0到1写一个你自己的skill, 2026-05-26-抄作业Claude负责人演示]
---

# Claude Code

## 定义

Claude Code 是 Anthropic 推出的 AI 编程助手，一款完全 Agentic 的命令行工具，能够编写完整功能、整个文件、修复整个 Bug，而不仅仅是代码补全。

## 关键信息

### 核心特性
- **完全 Agentic**：不只是代码补全，可以完成完整任务
- **IDE 无关**：兼容 VS Code、Xcode、JetBrains 等所有 IDE
- **环境通用**：支持本地、SSH、Tmux 等各种终端环境
- **代码本地**：不上传代码到云端，不用于模型训练

### 入门工作流
1. **代码库问答 (Codebase Q&A)**：先问问题了解代码库（Anthropic 新员工培训第一步）
2. **探索与规划**：让 Claude 先制定计划，确认后再编码
3. **迭代优化**：提供测试/截图等反馈工具，让 Claude 自我迭代

### 核心技巧

#### Claude.md
- 项目根目录的特殊文件，存储上下文信息
- 包含：常用命令、架构决策、重要文件、MCP 工具配置
- 支持嵌套目录的局部 Claude.md

#### 快捷键
- **Shift+Tab**：自动接受编辑
- **# + 内容**：让 Claude 记住某事（自动写入 Claude.md）
- **! + 命令**：执行 Bash 命令
- **Esc**：安全停止当前操作
- **Ctrl+R**：查看完整输出

#### SDK 使用
`claude -p` 将 Claude 作为 Unix 工具：
- JSON / 流式 JSON 输出
- 管道输入输出（配合 `git status`、`jq` 等）
- 适用于 CI、事件响应

### 工具集成
- **Bash 工具**：调用团队 CLI 工具
- **MCP (Model Context Protocol)**：标准化工具接口
- **多模态**：支持图片输入（拖拽、文件路径、复制粘贴）

### 内部使用情况
- Anthropic 80% 技术人员每天使用
- 新员工技术 onboarding 从 2-3 周缩短到 2-3 天

## 关联
- 相关概念：[[Claude]], [[MCP]], [[Model Context Protocol]], [[Coding Agent vs 日常任务Agent]], [[Agent]], [[Tool Use]], [[Cursor]]
- 相关实体：[[Claude]], [[Anthropic]]

## 开放问题
- Claude Code 与 Cursor 在实际效率上的对比
- 未来是否会有 GUI 版本
