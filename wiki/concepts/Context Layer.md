---
type: concept
created: 2026-08-01
updated: 2026-08-06
sources: [2026-08-01-生产级Agent缺的不是PromptContext, 2026-08-06-我现在给agent补上下文只做这四层]
---

# Context Layer

## 定义

**Context Layer** 是将企业的知识、专业能力和规范（Norms）转化为机器可用上下文（Machine-usable Context）的系统层。它是连接企业业务系统与通用Agent之间的中间基础设施，负责持续挖掘、归一化、关联和评估企业知识，为不同Agent动态组装所需Context。

## 核心公式

**Performance = Intelligence × Context**

Agent的绩效不是仅由模型智能决定的，而是模型智能（Intelligence）和业务上下文（Context）的乘积。更强的模型只是能力上限，而Context决定能力能否转化为实际结果。

## 工作原理

Context Layer 以五个步骤运行：

1. **持续挖掘**：从企业业务系统（Docs、Slack、CRM、Data Warehouse、Policies、Tickets）中持续抽取Context
2. **沉淀中枢**：将抽取的知识输入到 [[Company Brain]]
3. **生命周期管理**：在Skills和Context开发生命周期中利用这些知识
4. **多通道检索**：通过 [[MCP]]、SQL、[[RAG|Vector Retrieval]]、Hybrid Assembly等方式为Agent检索Context
5. **学习闭环**：从Agent的Trace中拉回反馈，构建 [[Compounding Learning Loop]]

## Context应该像Code一样管理

Context Layer 的核心理念是 **"GitHub for Context"**——Context需要像代码一样进行工程化管理：

| 维度 | 代码管理 | Context管理 |
|------|----------|-------------|
| 版本控制 | Git版本号 | Context Versioning |
| 依赖管理 | package.json | Dependency Management |
| 质量管理 | CI/CD + 测试 | Quality & Security Posture |
| 作用域 | Global/Local变量 | Global/Local Context |
| 角色管理 | Approver/Maintainer/Contributor | 同样的角色体系 |

## 与Context工程的区别

[[Context工程]] 关注的是"在正确时机把正确信息喂给大模型"的策略层面，而 Context Layer 是这一理念在企业级Agent场景下的系统化落地——它不仅是策略，更是一个持续运行的基础设施。

## 关键数据

- 模型智能过去十年增长约1000倍，最近六个月又2倍
- 但仅1/5的AI Use Case进入Production
- 56%的CEO表示AI尚未带来财务收益
- IQ只解释约10%的工作绩效差异

## 实践落地：四层上下文架构

Context Layer 的实践落地方法是 [[四层上下文架构]]——将上下文从静态到动态分为四层：

1. **[[AGENTS.md]]（项目地图）**：精简后的项目导航，只回答三个问题
2. **[[按需知识树]]**：会议纪要、历史决策、业务规则和排查经验，分层组织按需查询
3. **[[任务现场]]**：每次任务开始时动态组装Issue、代码、口径、时间、环境、日志
4. **[[长期记忆管理]]**：只留稳定的结论、决策、风险和验证结果

核心实践原则：上下文不是给模型补充更多知识，而是给它当前决策所需要的真实事实。按需加载，不是按量加载。

## 关联

- 相关概念：[[Company Brain]]、[[Compounding Learning Loop]]、[[GitHub for Context]]、[[Context工程]]、[[四层上下文架构]]、[[AGENTS.md]]、[[按需知识树]]、[[任务现场]]
- 检索机制：[[MCP]]、[[Model Context Protocol]]、[[RAG]]
- 前置概念：[[Context Window]]、[[AI Agent]]、[[LLM]]
- 来源：[[2026-08-01-生产级Agent缺的不是PromptContext]]、[[2026-08-06-我现在给agent补上下文只做这四层]]
