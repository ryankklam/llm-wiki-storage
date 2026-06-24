---
type: source
date: 2026-06-17
source: raw/rednote/video/2026-06-17-AgentSkill过多4招提升命中_51CzJE5TRxS.mp4
platform: xiaohongshu
video_id: 51CzJE5TRxS
author: 小哲讲大模型
tags: [Agent, Skill, 路由, Routing, Skill Tree, 分层路由, 负样本, 召回, 重排, 检索, 命中率, LLM, 大模型, Prompt, Function Calling, Tool Use, Multi-Agent, Sub-Agent, Orchestrator, Planner, Executor, Context Window, Token, RAG, Embedding, 向量检索, 语义搜索, 相关性, 相似度, 渐进式加载, Progressive Disclosure, Claude, Anthropic, Skill Router, 语义匹配]
---

# 来源：Agent Skill过多？4招提升命中

## 视频信息
- **作者**：小哲讲大模型
- **发布时间**：2026-06-17
- **视频链接**：http://xhslink.com/o/51CzJE5TRxS
- **平台**：小红书

## 核心要点

1. **问题本质**：当Agent的Skill从十几个涨到几十个上百个后，模型开始"抽风"——明明有对应Skill却不用，或者用了错误的Skill。这不是模型变笨了，而是Skill路由本身变成了一个检索问题。

2. **核心思想（Anthropic Progressive Disclosure）**：Claude不会把所有Skill全部塞进上下文，而是先读取每个Skill的名称和描述，再决定要不要加载完整内容。Skill的Name和Description本质上就是向量检索里的标题和摘要。

3. **方法一：优化Skill描述，提升区分度**
   - 不要写Skill是什么，而要写什么时候用它
   - Description里应该包含触发场景，而不仅仅是功能介绍
   - 场景描述越清晰，语义匹配命中率越高

4. **方法二：建立Skill Tree进行分层路由**
   - 不要平铺100多个Skill让模型一次性判断
   - 第一层分大类（研发、运营、市场、财务），第二层分子类（代码生成、代码评审、测试生成）
   - 模型先找大类再找具体Skill，搜索空间大幅缩小

5. **方法三：增加负样本描述**
   - 除了告诉模型什么时候用，还要告诉模型什么时候不要用
   - 例如："仅用于生成SQL，不用于数据库设计和性能优化"
   - 社区高质量Skill都开始增加When Not to Use部分，显著减少误触发

6. **方法四：引入召回加重排机制**
   - 不要让大模型直接从几百个Skill里选
   - 先用Embedding或关键词检索召回Top 10，再交给大模型做最终判断
   - 和RAG思路完全一致，Skill Router本身变成了一个检索系统

## 视频内容摘要

视频围绕"Agent Skill过多如何保证命中率"这一面试高频问题，系统阐述了Skill路由的本质和四个实用优化方法。

视频前半部分（00:00-00:24）引入问题：Skill少时命中率高，Skill多到上百个后模型开始"抽风"，本质是Skill路由变成了检索问题。

视频中间部分（00:25-02:12）详细展开四个方法：
- 优化Skill描述（写触发场景而非功能介绍）
- 建立Skill Tree分层路由（大类→子类→具体Skill）
- 增加负样本描述（When Not to Use）
- 召回加重排（Embedding召回Top 10 + LLM重排）

视频结尾（02:13-02:33）总结：当Skill数量达到几百上千后，Skill Router本身就变成了一个检索系统，很多研究工作甚至专门训练Skill Router来解决这个问题。

## 关键信息

- **核心心法**：Skill路由的本质是检索问题，不是模型变笨了
- **Skill描述原则**：Name和Description是向量检索的标题和摘要，模糊描述导致模型分不清谁是谁
- **分层路由价值**：把100+选项的平铺判断变成2-3层的逐级筛选
- **负样本价值**：When Not to Use能显著减少误触发
- **召回重排价值**：先用Embedding/关键词缩小候选集，再用LLM精排，和RAG同构

## 与其他来源的关系

- 与 [[2026-05-11-万物都可蒸馏Skill-5min讲清机制]] 在Skill设计理念上相互印证：Skill的元数据（Name/Description）和渐进式加载思想
- 与 [[2026-05-31-AI Agent四种范式对比]] 在Agent架构层面形成互补：Tool Use层之上，Skill路由是实际工程中的关键挑战
- 与 [[2026-06-05-Anthropic数据Agent95%准确率背后②]] 在Anthropic方法论上一脉相承：Progressive Disclosure与四层架构都强调信息的结构化编排
- 与 [[2026-05-28-如何在有限上下文窗口内放入关键内容]] 在Context Window优化上呼应：不一次性塞所有Skill，而是按需加载

## 衍生概念

- [[Skill路由]]
- [[Skill Tree]]
- [[分层路由]]
- [[负样本]]
- [[召回重排]]
- [[渐进式加载]]
- [[Skill Router]]
- [[语义匹配]]
