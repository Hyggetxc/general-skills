---
name: source-research
description: Use when a question needs fact-checking, current information, official documentation, primary-source research, source-backed comparison, or a reusable Markdown evidence note outside or before product requirements work.
---

# 一手来源查证

用可靠来源回答问题，并说明证据边界。本技能是通用查证能力，不属于需求分析专属流程。

## 来源原则

1. 优先一手来源：官方文档、源代码、规范、平台后台、原始表格/文档、公开监管或政策原文。
2. 二手文章只能作为线索，不能作为最终事实来源。
3. 时效性强的问题必须查最新来源。
4. 每个关键结论都要能追到来源。
5. 查不到时直接说明无法确认，不用推测补齐。

## 输出

短问题可直接回复：

1. 结论。
2. 来源。
3. 证据边界。
4. 仍需确认的问题。

需要留痕时，创建 `source-research-<主题>.md`：

```markdown
# source-research-<主题>

## 问题

## 结论

## 证据

## 无法确认或冲突

## 对后续工作的影响
```

## 边界

1. 不写 PRD。
2. 不做业务取舍。
3. 不维护术语表；术语归一使用 `business-glossary`。
4. 不代替法律、财务、医疗等高风险专业意见。
