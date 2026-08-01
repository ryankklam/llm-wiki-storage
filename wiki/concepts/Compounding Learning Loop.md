---
type: concept
created: 2026-08-01
updated: 2026-08-01
sources: [2026-08-01-生产级Agent缺的不是PromptContext]
---

# Compounding Learning Loop

## 定义

**Compounding Learning Loop** 是Agent执行后，将Trace（执行轨迹和反馈）回流到 [[Company Brain]] 和 [[Context Layer]]，持续修正Skills与Context，形成知识复利增长的闭环机制。

## 核心机制

```
Agent执行任务 → 产生Trace → Trace回流 → 修正Skills和Context → 下次任务更智能 → 循环
```

每一次Agent执行都是一次学习机会：
1. Agent使用Context Layer提供的Context执行任务
2. 执行过程产生Trace（包括决策路径、工具调用、结果反馈）
3. Trace回流到Company Brain
4. 系统根据Trace修正Skills和Context的质量
5. 修正后的知识在下次任务中提供更精准的Context

## 与人类团队学习的关系

演讲者用人类梦之队做类比：
- 高效团队有"什么是好的"的compounding learning loops
- 他们有共享记忆——"上个季度我们发布了那个东西，结果很糟糕，我们不会再犯同样的错误"
- Agent系统也需要同样的学习闭环

## 与Agent Loop的区别

| 维度 | [[Agent Loop]] | Compounding Learning Loop |
|------|----------------|--------------------------|
| 关注点 | 单次任务的执行循环 | 跨任务的知识积累循环 |
| 时间跨度 | 单次会话 | 跨会话、跨任务 |
| 产出 | 任务结果 | 知识和Skills的持续改进 |
| 反馈来源 | 工具执行结果 | Agent Trace + 业务反馈 |

两者互补：Agent Loop是执行层面的循环，Compounding Learning Loop是知识层面的循环。

## 关联

- 相关概念：[[Context Layer]]、[[Company Brain]]、[[Agent Loop]]、[[Loop Engineering]]
- 来源：[[2026-08-01-生产级Agent缺的不是PromptContext]]
