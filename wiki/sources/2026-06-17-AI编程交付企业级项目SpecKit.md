---
type: source
date: 2026-06-17
source: raw/rednote/video/2026-06-17-AI编程交付企业级项目SpecKit_6B5XkCvlVpb.mp4
platform: xiaohongshu
video_id: 6B5XkCvlVpb
author: 木羽cheney
tags: [Spec-Kit, SpecKit, Spec, AI编程, 企业级项目, 立宪法, 说需求, 出方案, 拆任务, 生成, 主动追问, 一致性检查, Constitution, rules.md, CLAUDE.md, Claude Code, Cursor, Claude, Anthropic, OpenSpec, Clarify, Verify, Gate, 门控, 文档驱动, MVP, Extension, Preset, Workflow, Agent注册中心, Hooks, 黑盒, 代码生成, 项目管理, 需求分析, 架构设计, 任务拆解, 自动化, CI/CD, Git, Code Review, 测试, 部署, 文档, Markdown]
---

# 来源：AI 编程交付企业级项目 Spec-Kit 是必学技术

## 视频信息
- **作者**：木羽cheney
- **发布时间**：2026-06-17
- **视频链接**：http://xhslink.com/o/6B5XkCvlVpb
- **平台**：小红书

## 核心要点

1. **Spec-Kit 的定位**：Anthropic 官方开源的 Spec 驱动开发框架，专门配 Claude Code、Cursor、Copilot 等 AI 编程工具使用。相较于轻量框架 OpenSpec，Spec-Kit 具有更广泛的应用场景、可插拔架构和社区生态。

2. **AI 跑偏的根本原因**：你没把话说清楚，AI 只能靠猜。猜错了又没机会拦，等跑完错已经埋进代码里了。

3. **轻量工具的三大缺陷**：
   - 从零起步（Greenfield）没有引导式提问，不知道自己漏了什么
   - 不会主动追问缺什么信息，全靠你自己想起来补
   - 校验全靠人工经验，没经验的只能赌

4. **Spec-Kit 五条核心命令（最小闭环）**：
   - **立宪法（Constitution）**：给项目放一份 CLAUDE.md / rules.md，告诉 AI 什么能动什么不能碰
   - **说需求（Spec）**：把需求说成 AI 能读懂的格式，不是聊天里飘忽的一句话
   - **出方案（Plan）**：让 AI 拿着 rules.md 和需求，出一份技术方案
   - **拆任务（Tasks）**：把方案拆成一条条具体的活，每一条都能单独验收
   - **生成（Execute）**：让 AI 拿着任务清单去写代码，写完一对照跑没跑偏

5. **两道可选关卡**：
   - **主动追问（Clarify）**：AI 主动提问，帮你发现需求中的盲点和冲突
   - **一致性检查（Verify）**：内置校验机制，检查生成的代码与 Spec 是否一致

6. **Spec-Kit 与 OpenSpec 的核心区别**：Spec-Kit 每一步都停下来等人工确认（Gate 门控机制），而不是一口气替你跑完。把 AI 从靠运气变成步步看得见。

7. **Spec-Kit 五大组件系统**：
   - **CLI 主体**：面向用户的唯一入口，总调度
   - **AI Agent 注册中心**：集成 Claude Code、Cursor 等主流 AI 编程工具
   - **扩展系统（Extension）**：插件市场，做加法，新增能力（如 Git 分支管理、CI/CD）
   - **预设系统（Preset）**：主题包，做替换，覆盖默认的 Scales 和 Markdown 输出规范
   - **工作流引擎（Workflow）**：内置标准流程（0.6.1 版本引入）

8. **Constitution（项目宪法）的核心内容**：
   - 构建当前项目的核心原则
   - 额外的约束条件
   - 开发流程定义
   - 项目治理方式

9. **核心理念**：让 AI 停下来等你点头，比让 AI 跑得快更重要。方法是通用的，工具上的按钮随时可以换。

## 视频内容摘要

视频前半部分（00:00-03:43）为短视频引言，系统阐述了 Spec-Kit 的核心价值：通过五条核心命令（立宪法、说需求、出方案、拆任务、生成）+ 两道可选关卡（主动追问、一致性检查）构建最小闭环，解决 AI 编程中"一口气跑完代码、回头乱成一锅粥"的核心痛点。

视频后半部分（03:45-45:30）为直播课程，详细讲解了：
- OpenSpec 回顾：三条命令（Propose、Apply、Tasks）的轻量闭环
- OpenSpec 三大问题：Greenfield 困难、无 Clarify 机制、Verify 依赖人工经验
- Spec-Kit 对三大问题的解决方案：Constitution 立宪法、Clarify 主动追问、Verify 一致性校验
- Spec-Kit 核心工作流：Constitution → Spec → Clarify（可选）→ Plan → Tasks → Verify（可选）→ Execute
- Spec-Kit 五大组件系统：CLI 主体、Agent 注册中心、扩展系统、预设系统、工作流引擎
- Extension（做加法）vs Preset（做替换）的插件生态设计

## 关键信息

- **核心心法**：让 AI 停下来等你点头，比让 AI 跑得快更重要
- **大道至简**：9 个命令中 5 条核心命令就够跑通一个项目，剩下看场景该上才上
- **黑盒问题**：Claude Code 本身是黑盒，Spec-Kit 通过文档驱动让人类掌控整个开发进度
- **Gate 门控机制**：每一步完成后停下来由人工确认，再推进下一步
- **方法通用性**：工具换成 Cursor 和 Claude Code、Codex 都成立，模型换下一代也照样成立

## 与其他来源的关系

- 与 [[2026-06-12-企业AI项目rules红线]] 直接延续：rules.md / CLAUDE.md 的编写方法论是 Spec-Kit Constitution 的基础
- 与 [[2026-06-09-AgentLoop构建步骤实战指南]] 在系统工程化方面形成互补：Spec-Kit 的 Gate 门控机制与 Agent Loop 的 Guardrails 护栏机制异曲同工
- 与 [[2026-06-14-LoopEngineering做设计循环的人]] 在设计理念上呼应：都是强调人工确认和可控性
- 与 [[2026-05-25-Anthropic内部Prompt写法]] 在 Prompt 工程方法论上相互印证

## 衍生概念

- [[Spec-Kit]]
- [[企业级AI项目]]
- [[AI编程交付]]
- [[立宪法]]
- [[一致性检查]]
- [[主动追问]]
- [[Constitution]]
- [[OpenSpec]]
- [[Greenfield]]
- [[Brownfield]]
- [[Clarify]]
- [[Verify]]
- [[Gate]]
- [[门控]]
- [[文档驱动]]
- [[Extension]]
- [[Preset]]
- [[Workflow]]
- [[Hooks]]
- [[Agent注册中心]]
