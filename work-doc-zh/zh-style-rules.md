# Chinese Workplace Style Rules

These rules synthesize common ideas from Chinese de-AI writing projects such as qu-ai-wei, shuorenhua, stop-slop-zh, anti-aistyle-zh, deslop-zh, and Chinese technical writing guides. Adapt them for workplace documents: clarity and traceability matter more than sounding casual.

## Main Rule

Remove template smell, not professionalism.

Do not turn a work document into chatty copy just to avoid AI flavor. The target voice is: a responsible colleague explaining a real situation clearly.

## High-Signal AI Smells In Chinese

### Empty Value Claims

Avoid phrases that sound useful but do not add evidence:

- 赋能
- 助力
- 打造
- 抓手
- 闭环
- 拉通
- 沉淀
- 体系化
- 显著提升
- 全面推进
- 持续优化
- 有效支撑
- 深度融合
- 高质量发展
- 进一步完善

Replace them with the actual change:

```text
Bad: 该方案能够有效支撑后续能力建设。
Good: 该方案先解决样本口径不一致的问题，后续模型对比可以复用同一批 badcase。
```

### Forced Summary

Avoid endings that only repeat the document:

- 综上所述
- 总体来看
- 可以看出
- 值得注意的是
- 需要指出的是
- 在未来工作中
- 后续将持续推进

End with a decision, open question, owner, or next action.

### Fake Structure

Watch for structures that make the document look organized but do not improve understanding:

- `首先 / 其次 / 最后` when the order is arbitrary
- `一方面 / 另一方面` when the two sides are not truly in tension
- `不仅是 A，更是 B`
- `既要 A，也要 B，还要 C`
- three-item parallel lists used only for rhythm
- every section ending with a mini-summary

Replace fake structure with the actual relationship:

- cause and effect
- before and after
- evidence and conclusion
- tradeoff
- risk and mitigation
- decision and consequence

### Abstract Subjects

Chinese AI prose often uses abstract nouns as subjects:

```text
Bad: 数据质量的提升为模型效果优化提供了重要保障。
Good: 标注口径统一后，模型对比里少了一类人为噪声。
```

Prefer concrete actors and objects:

- this sample set
- this rule
- this metric
- the current version
- the reviewer
- the upstream document
- the downstream evaluation

### Nominalization

Avoid turning actions into heavy nouns:

```text
Bad: 完成了对问题样本的识别、归因和治理。
Good: 我们先找出问题样本，再按原因拆成三类，最后只修影响结论的部分。
```

Use verbs when the action matters.

### Over-Neat Tone

AI text is often too smooth:

- every paragraph has the same length
- every sentence has the same rhythm
- every point is equally confident
- uncertainty disappears
- tradeoffs disappear

Work documents should keep real texture:

- say when a result is preliminary
- say when the evidence is partial
- say when there are competing explanations
- say what you have not checked yet

## Workplace Voice

Use this default voice:

- direct
- specific
- calm
- traceable
- not promotional
- not overly polite
- not slogan-like

Good:

```text
目前更像是标签口径问题，不像模型能力单独退化。原因有两个：同一类样本在 4/17 和 4/03 的结果差异不大；人工复核里，大部分分歧集中在“是否算遗漏”。
```

Bad:

```text
本轮分析充分说明，模型能力建设仍需围绕数据质量持续发力，通过标签口径优化形成闭环，进一步提升整体评估准确性。
```

## Editing Order

When polishing a draft, use this order:

1. Preserve facts and intent.
2. Clarify the main claim.
3. Move evidence closer to the claim.
4. Delete empty transitions and value claims.
5. Shorten sentences that carry too many abstract nouns.
6. Add source details where claims rely on external material.
7. Check the ending for a concrete next action.

Do not start by making the language more literary.

## Common Rewrites

```text
Bad: 为了进一步提升项目质量，我们对相关问题进行了深入分析。
Good: 这次分析主要想确认一个问题：当前 badcase 是模型问题，还是标签口径问题。
```

```text
Bad: 数据表现呈现出一定波动，需要持续关注。
Good: 4/22 晚上的样本比 4/17 多出 31 条 schema invalid，需要单独看来源。
```

```text
Bad: 后续将围绕问题持续优化，推动能力不断提升。
Good: 下一步先补 50 条人工复核样本，再决定是否调整标签规则。
```

```text
Bad: 该能力不仅提升了效率，也为后续建设奠定基础。
Good: 这一步把人工筛样从半天缩到 20 分钟，后面可以每天固定跑一次。
```

## Source-Aware Language

Use precise source verbs:

- `显示` for data or logs
- `记录` for meeting notes or chat history
- `定义` for specs and rules
- `推测` for uncertain explanations
- `建议` for proposed action
- `尚未验证` for untested assumptions

Avoid writing inferred claims as facts.

```text
Bad: 该问题由 prompt 变更导致。
Good: 目前只能推测和 prompt 变更有关，因为异常集中出现在 4/17 版本之后；还需要对比同一批样本的 raw prompt。
```

## Final Checklist

Before returning the document, check:

- The opening states the purpose or conclusion quickly.
- Key claims have nearby evidence or clearly marked uncertainty.
- External docs, data files, and paths are cited clearly enough to verify.
- The document does not rely on slogans, generic transitions, or forced parallelism.
- The ending tells the reader what to decide, check, or do next.
