---
type: source
date: 2026-08-01
platform: xiaohongshu
author: Unknown
url: http://xhslink.cn/o/5oZCCwme72W
video: raw/rednote/video/2026-08-01-生产级Agent 缺的不是Prompt，Context_5oZCCwme72W.mp4
subtitle: raw/rednote/subtitle/2026-08-01-生产级Agent 缺的不是Prompt，Context_5oZCCwme72W.md
xhs_id: 5oZCCwme72W
title: 生产级Agent 缺的不是Prompt，Context
---

# 生产级Agent 缺的不是Prompt，Context

> 模型变得越来越聪明，为什么真正进入 Production 的 AI Use Case 仍然有限？这场演讲给出的解释很直接：现实中的 Agent Performance，不只取决于模型的 Cognitive Intelligence，还取决于它能否获得正确、及时、可执行的 Context。核心公式：**Performance = Intelligence × Context**。更强的模型只是能力上限，而任务目标、组织事实、工具权限、历史决策和反馈信号，决定能力能否转化为结果。

## 核心观点

1. **模型智能 vs 实际效用的落差**：过去十年模型智能增长约1000倍，最近六个月又提升约2倍；但只有约1/5的AI Use Case进入Production，56%的CEO表示AI尚未带来财务收益
2. **IQ只解释10%的工作绩效**：就像人类世界中IQ不是绩效的唯一决定因素，Agent的绩效也不只取决于模型智能
3. **Performance = Intelligence × Context**：Agent绩效是模型智能和业务上下文的乘积，两者缺一不可
4. **Context几乎没动**：智能增长了1000倍，但企业的situated knowledge还锁在dashboards、Slack threads和即将离职的分析师脑子里
5. **General-purpose Agent需要共享团队Context**：高效团队依赖共享语言、当前事实、Playbook、决策Norms和共享Memory，Agent也需要一个可复用的Company Brain
6. **Context应该像Code一样管理**：需要Versioning、Dependency Management、质量与Security Posture、Global/Local Scope，以及Approver、Maintainer、Contributor等明确角色
7. **Context Layer是持续学习的基础设施**：企业系统中的知识被持续抽取、归一化、关联和评估，沉淀为Company Brain，再通过MCP、SQL、Vector Retrieval或Hybrid Assembly为Agent动态组装Context
8. **Compounding Learning Loop**：Agent的Trace回流后，继续修正Skills与Context，形成持续学习的闭环

## 视频章节

### 一、模型智能 vs 实际效用
- [00:00] 模型在指数级变聪明：两年前无法通过律师资格考试，今天能进入前1%
- [00:09] 但模型并没有指数级地更有用：仅1/5的AI Use Case进入Production，56%的CEO称AI零财务收益
- [00:27] 这到底是怎么回事？

### 二、Performance的真正决定因素
- [00:29] 在人类世界中，认知智能并不真正决定实际效能——IQ只解释10%的工作绩效差异
- [00:45] 你最聪明的队友（SAT最高分）不一定是你最好的队友；最好的队友是工作最努力、最善于接受反馈、学得最快的人
- [01:07] Performance = Intelligence × Context：绩效是认知能力和情境知识的乘积
- [01:26] 过去十年只在一个参数上复合增长：Intelligence增长了1000倍，最近六个月又2倍
- [01:38] 但Context——企业的情境知识——几乎没动，还锁在dashboards、Slack threads和分析师脑子里

### 三、General-Purpose Agent需要共享团队Context
- [01:56] 随着通用Agent开始成为现实，我们提出：如果有不同的方法呢？
- [02:05] 回到人类世界——Maya不是个人明星，她是团队的一部分
- [02:20] 梦之队建立在共享Context之上：共享语言、共享当前事实图景、共享Playbook、共享决策Norms
- [02:37] 最重要的是：他们有"什么是好的"的复合学习循环（Compounding Learning Loops）
- [02:43] 他们有共享记忆——"上个季度我们发布了那个东西，结果很糟糕，我们不会再犯同样的错误"

### 四、Company Brain与Context Layer
- [02:57] 心智模型：让这些团队开始构建domain skills，每个团队负责一组技能
- [03:13] 所有这些汇聚到一个共同的地方——一个Company Brain
- [03:20] 我喜欢把它称为Context Layer，它有一系列检索机制与通用Agent交互

### 五、Context应该像Code一样管理
- [03:31] WTF is a Context Layer？这就是Context Layer要解决的问题
- [03:39] 核心问题：Context的GitHub长什么样？
- [03:45] 企业Context需要生命周期管理、协作和版本控制——就像代码一样
- [04:02] Context能有profile吗？能有自学习循环吗？质量管理、安全态势管理？
- [04:20] 内置版本控制、质量和依赖管理：能说"这个东西影响所有其他东西"
- [04:31] 这是Approver、这是Maintainer、这些是Contributors——如何构建人+AI工作空间

### 六、Context Layer的工作原理
- [04:41] Context Layer是一个将知识、专业能力和规范转化为机器可用Context的系统
- [05:00] 1. 持续从业务系统中挖掘Context
- [05:05] 2. 将其输入到Company Brain
- [05:09] 3. 在skills和context开发生命周期中利用它
- [05:16] 4. 多种检索方式：MCP、SQL、Vector Retrieval、Hybrid Assembly
- [05:25] 5. 从Trace中拉回反馈，构建Compounding Learning Loop

## 关键概念总结

| 概念 | 含义 |
|------|------|
| **Performance = Intelligence × Context** | Agent绩效由模型智能和业务上下文共同决定 |
| **Company Brain** | 可复用的企业级知识中枢，跨任务保持一致性 |
| **Context Layer** | 将知识/规范转化为AI可用上下文的系统层 |
| **GitHub for Context** | Context需要像代码一样进行版本管理、依赖管理、质量管理 |
| **Compounding Learning Loop** | Agent Trace回流后持续修正Skills与Context的闭环 |
| **MCP / SQL / Vector Retrieval** | Context Layer的多种检索机制 |

## 关联概念

- [[Context Layer]]
- [[Company Brain]]
- [[Compounding Learning Loop]]
- [[GitHub for Context]]
- [[Context工程]]
- [[Context Window]]
- [[MCP]]
- [[Model Context Protocol]]
- [[RAG]]
- [[AI Agent]]
- [[LLM]]
- [[Agent Loop]]
- [[Loop Engineering]]
- [[Skill]]
- [[Token]]
