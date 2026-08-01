---
type: concept
created: 2026-08-01
updated: 2026-08-01
sources: [2026-08-01-生产级Agent缺的不是PromptContext]
---

# Company Brain

## 定义

**Company Brain** 是企业级的可复用知识中枢，将分散在不同业务系统中的知识、专业能力和规范汇聚到一个统一的"大脑"中，使通用Agent能够跨Research、Sales、Operations等任务保持一致性。

## 核心思想

就像人类梦之队依赖共享Context一样：

- **共享语言**：团队成员（和Agent）使用统一的术语和沟通方式
- **共享当前事实图景**：对企业"今天什么是对的"有共同认知
- **共享Playbook**：标准化的操作流程和最佳实践
- **共享决策Norms**：明确谁被允许做什么决策
- **共享记忆**：记录过去的成功和失败经验

Company Brain 就是将这些人类团队的共享Context转化为Agent可复用的知识基础设施。

## 在Context Layer中的角色

Company Brain 是 [[Context Layer]] 的核心存储层：

1. 各团队构建domain skills，每个团队负责一组技能
2. 所有skills和知识汇聚到Company Brain
3. Company Brain通过检索机制与通用Agent交互
4. Agent执行后的Trace回流到Company Brain，持续修正

## 与现有概念的关系

- Company Brain 是 [[Context工程]] 理念在企业级场景的系统化落地
- 它解决了 [[Context Window]] 有限的问题：不是把所有信息塞进窗口，而是按需从Company Brain检索
- 它是 [[Compounding Learning Loop]] 的知识沉淀载体
- 与 [[RAG]] 的关系：RAG是Company Brain的一种检索机制

## 关联

- 相关概念：[[Context Layer]]、[[Compounding Learning Loop]]、[[Context工程]]
- 检索机制：[[MCP]]、[[RAG]]
- 来源：[[2026-08-01-生产级Agent缺的不是PromptContext]]
