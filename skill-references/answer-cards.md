# Answer Cards

Goal: convert high-risk interview questions into safer, stronger answers.

## Format

```text
Question:
Why risky:
Dangerous answer:
Passable answer:
Strong answer:
Evidence needed:
Resume wording to downgrade:
```

## Rules

- Dangerous answers overclaim, hide gaps, or use vague words.
- Passable answers admit boundaries and explain real work.
- Strong answers add evidence, tradeoffs, failure cases, and next steps.
- If the user lacks evidence, the strong answer may be "I would not write that claim yet".

## Example

Question:

```text
你说提升了搜索排序效果，指标是什么？
```

Dangerous answer:

```text
感觉排序结果更好了，用户体验提升很多。
```

Passable answer:

```text
目前没有线上指标，所以我不会写提升比例。我做的是长尾 query bad case 分类和 rerank baseline 复现。
```

Strong answer:

```text
我用固定 query-doc 样例集对比 BM25、embedding 召回和 cross-encoder rerank 的结果，记录 NDCG@10 与 bad case 类型。现阶段只把它写成离线分析和 baseline 复现，不写线上提升。
```
