---
type: concept
created: 2026-05-31
tags: [公司, 大数据, 企业软件, Ontology]
---

# Palantir

> Palantir 花了 20 年，在为真实世界打地基。

## 定义

Palantir 是美国大数据分析公司，以 Ontology 语义建模层和 FDE（Forward Deployed Engineer）模式著称。其核心产品包括 Foundry（企业数据平台）和 Gotham（政府/国防数据分析平台）。

## 核心技术

### Ontology
Palantir 的核心语义建模层，把企业数据变成有类型的对象、有关系、有动作权限的语义系统。四大组件：
- Object Type：定义企业里有什么
- Property：定义每个类型的特征
- Link Type：定义类型之间的关系
- Action Type：定义能对对象做什么

### OSDK
Ontology SDK，支持 TypeScript、Python、Java，让 FDE 能用已建模的 Ontology API 直接开发，自动生成类型安全的接口。

### Embedded Ontology
把 Ontology 搬到设备端，实现分布式数据架构。让设备成为整个数据系统的一个自治节点。

## FDE 模式

Forward Deployed Engineer（前线部署工程师）是 Palantir 的核心角色：
- 把客户业务场景映射到 Ontology 数字世界
- 用 OSDK 在极短时间内做出能用的应用
- 第一周就在调业务流程，而不是还在对字段名

## 为什么被 AI 行业关注

Palantir 做了 20 年的 FDE 角色，最近被整个 AI 行业疯狂抄作业：
- OpenAI 划 40 亿估值给类似角色
- Anthropic 划 15 亿估值给类似角色

原因：模型再强，到了客户现场，面对的是几十个系统、几十套命名、几十年的混乱。FDE 解决的是怎么把模型嵌入真实世界的问题。

## 核心洞察

Palantir 文档的核心观点：
- Ontology 不是为了表示数据，而是为了表示决策
- Digital Twin of an Organization（企业的数字孪生）不是一个好看的数据中台，是一个可操作的决策系统

## 相关来源
- [[2026-05-31-FDE脚下的地基Ontology]]

## 相关概念
- [[Ontology]] - Palantir 的语义建模层
- [[FDE]] - Forward Deployed Engineer
- [[OSDK]] - Ontology SDK 开发框架
- [[数字孪生]] - Digital Twin of an Organization