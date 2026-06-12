---
name: work-doc-zh
description: Write and edit Chinese work documents for internal alignment, reporting, reviews, decision memos, and presentation drafts. Use when the user asks to write, rewrite, polish, de-AI, structure, summarize, or prepare Chinese workplace documents, including 同步、汇报、展示、复盘、周报、方案、会议纪要、PPT 大纲.
---

# 中文工作文档写作

## Core Principle

Treat every work document as a guided thought path. The reader should be able to follow the document from purpose, to evidence, to reasoning, to conclusion, and finally to the requested action.

Do not default to separate templates for 同步、汇报、展示. They share the same core job: make a point understandable and traceable.

## Workflow

1. Identify the document's purpose.
   - What should the reader understand, agree with, decide, review, or do after reading?
   - If the purpose is unclear, ask before writing.

2. Build the document spine before drafting.
   - Reader question: what question is this document answering?
   - One-sentence answer: what is the main judgment?
   - Evidence: what facts, data, files, or external docs support it?
   - Reasoning: how does the evidence lead to the judgment?
   - Action: what happens next, and who needs to do it?

3. Anchor claims to sources.
   - Cite external docs, file paths, data files, query ranges, screenshots, meeting notes, or chat records near the claim they support.
   - Distinguish fact, inference, and recommendation.
   - Do not invent metrics, causes, owners, or timelines.

4. Draft in plain workplace Chinese.
   - Lead with the useful conclusion, not background padding.
   - Use short sections whose headings describe the point, not generic labels.
   - Keep paragraphs focused: one paragraph, one job.
   - Use bullets when they improve scanning; use prose when the relationship between ideas matters.

5. Run a de-AI pass.
   - Remove slogan-like phrases, forced summaries, excessive parallelism, and generic value claims.
   - Preserve the user's facts, uncertainty, tone, and domain vocabulary.
   - Do not make work documents sound like a speech, press release, public account article, or government notice unless requested.

6. Run a traceability pass.
   - Can a reader tell why this document exists?
   - Can a reader trace each key claim to evidence?
   - Can a reader tell what is known, what is inferred, and what is still uncertain?
   - Can a reader tell what to do next?

## Reference Files

- For purpose-driven structure, source citation, and document patterns, read [document-logic.md](document-logic.md).
- For Chinese de-AI rules, banned patterns, and style cleanup, read [zh-style-rules.md](zh-style-rules.md).

## Output Preference

When writing from scratch, return the document itself, not a long explanation of the method.

When editing, make targeted changes first. If the original structure is broken, briefly explain the new spine before rewriting.
