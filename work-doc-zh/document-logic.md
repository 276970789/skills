# Purpose-Driven Chinese Work Documents

## What This Skill Optimizes For

A good workplace document is not just polished text. It helps a specific reader reconstruct a specific line of thinking:

1. why this document exists
2. what question it answers
3. what the answer is
4. what evidence supports the answer
5. what is uncertain
6. what should happen next

If a section does not help one of these jobs, cut it or move it to an appendix.

## Document Spine

Before drafting, fill this spine mentally or explicitly:

```text
Purpose:
Reader:
Reader's likely question:
One-sentence answer:
Key evidence:
Reasoning chain:
Open risks / uncertainties:
Requested action:
Source list:
```

For short docs, this spine can become the whole document. For longer docs, it becomes the hidden outline.

## First Screen Rule

The first screen should answer three questions:

- What is this about?
- What is the main conclusion or current state?
- What does the reader need to pay attention to?

Avoid opening with broad background such as "随着业务不断发展" or "为了进一步提升". Start from the concrete situation.

## Claim-Evidence-Meaning

For every important claim, include three layers:

- Claim: the point you want the reader to accept.
- Evidence: the data, file, external doc, example, or observation.
- Meaning: why this evidence matters for the current decision or understanding.

Do not stack many claims and put all evidence at the end. Evidence should sit near the claim it supports.

## Citing Sources Clearly

When citing external material, include enough information for someone else to verify it.

Use these patterns:

```text
来源：`path/to/file.md`，章节「xxx」，用于确认 xxx。
来源：`path/to/data.jsonl`，时间范围 2026-04-22 15:00 至 2026-04-24 00:00，筛选条件为 xxx。
来源：飞书文档《xxx》，段落「xxx」，访问时间 2026-06-12，用于确认 xxx。
来源：会议纪要 2026-06-11，参会人 xxx，用于确认 xxx 决策。
```

For data files, cite:

- file path or link
- time range
- filter condition
- sample size, if relevant
- metric definition
- whether the data is raw, sampled, or manually labeled

For external documents, cite:

- title or file path
- section, heading, or paragraph
- access date if the document may change
- what exact claim it supports

For screenshots or images, cite:

- file path
- page or feature shown
- capture time, if relevant
- what observation the screenshot supports

## Fact, Inference, Recommendation

Keep these three separate:

```text
事实：线上 badcase 池中，A 类问题占比 18%。
判断：A 类问题已经不是零散噪声，会影响本轮指标解释。
建议：先把 A 类问题单独拆层评估，再合入总分。
```

This is better than:

```text
A 类问题较为突出，需要持续优化相关能力，进一步提升整体效果。
```

## Section Headings

Prefer headings that carry the point:

- Good: `当前主要误差来自多轮指令遗漏`
- Good: `先拆出人工标注集，再比较模型版本`
- Avoid: `背景介绍`
- Avoid: `问题分析`
- Avoid: `优化建议`

Generic headings are acceptable only when the document is very short or the audience expects a fixed format.

## Structure Patterns

### Alignment / Sync

Use when the reader needs to quickly understand state and next steps.

```text
# [Topic] 当前进展与下一步

一句话状态：

目前已经完成：

当前卡点：

依据：

下一步：

需要协同：
```

### Reporting / Decision

Use when the reader needs to understand a judgment and decide.

```text
# 关于 [Topic] 的判断与建议

结论：

为什么现在要看：

关键依据：

推导过程：

风险和不确定性：

建议动作：
```

### Presentation / Slides

Use when the document will become slides or spoken explanation.

```text
# [Topic] 展示主线

主线一句话：

第 1 页：要回答的问题
第 2 页：最重要的发现
第 3 页：证据和例子
第 4 页：影响和风险
第 5 页：建议和下一步
```

Each slide should carry one message. Do not put background, finding, evidence, and recommendation on the same slide unless it is an executive summary.

## Ending

End with the next useful action, not a generic summary.

Good endings:

- `如果这个拆分方式 OK，我会按该口径补齐 4/28-4/30 的样本评估。`
- `需要确认的是：本轮是否先冻结标签口径，再继续跑模型对比。`
- `建议先按方案 B 试跑一天，明天同步结果和异常样本。`

Avoid:

- `综上所述，本方案能够有效提升整体效率。`
- `后续我们将持续优化，不断完善。`
- `相信在大家的共同努力下，项目会取得更好的成果。`
