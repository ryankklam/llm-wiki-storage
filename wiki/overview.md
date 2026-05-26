---
type: overview
created: 2026-05-10
updated: 2026-05-26
---

# 知识库概览

> 本 Wiki 由 LLM 自动维护。

## 当前状态
- 来源数量：4
- 总页面数：32
- 最近更新：2026-05-26

## 核心发现
<!-- 随着知识积累，这里将总结最重要的发现 -->

### Claude Code 实战技巧（Anthropic 官方）

#### 入门建议
- **从代码库问答开始**：Anthropic 新员工培训的第一步
- ** onboarding 效率提升**：从 2-3 周缩短到 2-3 天
- **无需索引**：代码完全本地，不上传云端

#### 核心工作流
1. **探索与规划**：先让 Claude 制定计划，确认后再编码
2. **迭代优化**：提供测试/截图等反馈工具，让 Claude 自我迭代
3. **工具集成**：通过 MCP 和 Bash 工具扩展能力

#### 效率技巧
- **Claude.md**：项目根目录存储上下文、常用命令、架构决策
- **快捷键**：Shift+Tab 自动接受、# 记住内容、! 执行 Bash、Esc 安全停止
- **SDK 模式**：`claude -p` 作为 Unix 工具使用，支持管道操作

#### 内部使用情况
- Anthropic 80% 技术人员每天使用 Claude Code
- 研究人员使用 Notebook 工具进行 ML 实验

### Prompt工程最佳实践（Anthropic 官方）

#### 结构化 Prompt
- 使用 XML tags 分离角色、指南、政策、语气等
- 经验法则：如果你无法区分，模型也无法区分

#### 评估驱动开发
- 控制用例：验证基本功能
- 边缘用例：防止问题再次出现
- 能力边界用例：确保正确升级或拒绝

#### 关键教训
- **指令不增加能力**：需要计算时给工具
- **说明权衡的两面**：不只说成本，也要说收益
- **模型可能扣留信息**：过度优化可能导致信息扣留

#### Agent 构建策略
- 简单任务：小模型 + 好 Prompt
- 复杂推理：大模型 + Extended Thinking
- 高可靠性：生成-评估-修复循环

### Agent分类体系
Agent按产出类型可分为两大类：
1. **Coding Agent**（Claude Code、Codex、OpenCode）：产出代码，预装完整工具链
2. **日常任务Agent**（Pi Agent）：产出结果，极简底座 + Skill按需扩展

### Pi Agent的核心优势
- System Prompt不到1500 tokens（Claude Code约20000 tokens）
- 三大优势：快、省（token消耗约1%）、聪明（注意力集中）
- 核心公式：Agent + Skill = 最基本的框架

### Skill生态
- Skill是给Agent的说明书/操作手册
- 按需安装，支持global和project两种模式
- 覆盖搜索、文件读取、语音合成、图片生成、视频制作等场景

### 工具协议
- **MCP (Model Context Protocol)**：标准化工具接口协议
- **Function Calling**：大模型原生工具调用能力
- **Claude Code**：同时支持 Bash 工具和 MCP 工具
