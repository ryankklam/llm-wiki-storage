---
type: concept
created: 2026-05-25
updated: 2026-05-25
sources: [2026-05-25-Anthropic内部Prompt写法]
---

# XML Tags

## 定义

**XML Tags 是用于结构化 Prompt 的标记语言**，通过使用 XML 格式的标签来分离 Prompt 中的不同类型内容，使模型更容易理解和遵循指令。

## 核心作用

### 1. 内容分离

将 Prompt 中的不同类型内容清晰分离：
- `<role>` - 角色定义
- `<guidelines>` - 通用指南
- `<policy>` - 政策规则
- `<tone>` - 语气要求
- `<data>` - 数据输入
- `<output>` - 输出格式

### 2. 提高模型理解

**经验法则**：如果你在阅读 Prompt 时无法区分指南、政策和数据，模型很可能也无法区分。

使用 XML tags 后：
- 模型可以更准确地定位相关指令
- 减少指令之间的冲突
- 提高指令遵循的准确性

### 3. 输出格式控制

在输出部分使用 XML tags：
- 定义清晰的输出结构
- 配合 Stop Sequence 确保输出一致性
- 便于下游程序解析

## 使用示例

### 结构化输入

```xml
<role>
你是一个电信公司的客服机器人。
</role>

<guidelines>
- 使用友好、专业的语气
- 准确回答客户问题
- 必要时升级到人工客服
</guidelines>

<policy>
- 基础套餐：5GB 数据流量
- 无限套餐：无限数据 + 4GB 热点
- 祖父套餐客户：按客户账户信息为准
</policy>

<customer_data>
客户姓名：张三
当前套餐：祖父套餐
热点数据：5GB
</customer_data>
```

### 结构化输出

```xml
<output_format>
<response>
[你的回复内容]
</response>
<action>
[需要采取的行动，如 escalate、answer 等]
</action>
</output_format>
```

## 最佳实践

1. **保持标签语义化**：使用描述性的标签名称
2. **层次清晰**：避免过度嵌套
3. **配合 Stop Sequence**：在 API 调用中设置停止序列
4. **版本控制**：记录标签结构的变化原因

## 与其他技术的关系

- **Stop Sequence**：检测闭合 XML tag，控制输出结束
- **Structured Outputs**：对于复杂输出结构，可配合使用
- **Tool Schema**：工具定义也可以使用类似的结构化方式

## 关联

- 相关概念：[[Prompt]]、[[Anthropic Prompt技巧]]、[[Evaluations]]
- 应用场景：[[System Prompt]]、[[输出契约]]

## 来源

- [[2026-05-25-Anthropic内部Prompt写法]]
