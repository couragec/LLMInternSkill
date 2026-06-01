# Role: Search / Ranking + LLM

Use for JD keywords such as search relevance, ranking, recall, rough rank, fine rank, rerank, doc understanding, long-tail query, authority, freshness, and LLM for search.

## What Big Companies Care About

- Understanding the search pipeline: query understanding -> recall -> rough rank -> fine rank/rerank -> result presentation.
- Query-doc relevance modeling: text matching, semantic matching, features, labels, negative sampling.
- Ranking metrics: NDCG, MRR, MAP, Recall@K, CTR/CVR when online.
- Doc understanding: structure, quality, authority, freshness, spam/low-quality filtering.
- Long-tail query analysis and bad-case taxonomy.
- How LLMs can help: query rewrite, doc representation, rerank, answer grounding, synthetic labels, judge models.
- Data and problem analysis ability, not just model naming.

## Toy Signals

- Only says "used LLM to improve search" with no query-doc data.
- No ranking metric.
- No baseline.
- No bad-case examples.
- Cannot explain recall vs rank vs rerank.
- Confuses RAG answer quality with search ranking quality.

## Evidence To Collect

- A small query-doc dataset with relevance labels.
- Bad-case table: query, bad result, expected result, failure type.
- Baseline: BM25, embedding retrieval, cross-encoder rerank, or simple LambdaMART-style baseline.
- Metric report: NDCG@K / MRR / Recall@K.
- Doc quality examples: freshness, authority, duplication, spam, low-quality page.

## Upgrade Actions

Half day:

- Write a search pipeline diagram.
- Collect 20 long-tail query bad cases.
- Define relevance labels and metric.

1 day:

- Run BM25 or embedding retrieval baseline.
- Add a rerank comparison on 20-50 query-doc pairs.
- Write a bad-case report.

3 days:

- Compare BM25 vs embedding vs cross-encoder rerank.
- Add query rewrite or doc understanding features.
- Produce NDCG/MRR table and qualitative analysis.

1 week:

- Build a small reproducible search/rerank repo with scripts, dataset sample, metrics, and report.

## Safe Resume Bullets

Conservative:

```text
围绕搜索相关性场景整理长尾 query-doc bad case，梳理召回、粗排、精排/重排各阶段的输入输出与失败类型，为后续排序优化建立分析口径。
```

Standard:

```text
基于小规模 query-doc 样例集复现 BM25、embedding 召回与 cross-encoder rerank baseline，使用 NDCG@10 / MRR 对比相关性表现，并沉淀长尾查询失败案例分析。
```

Stronger after evidence:

```text
构建搜索相关性离线评估闭环，围绕长尾查询、DOC 质量与时效性特征设计 query-doc 标注样例和 rerank 对比实验，产出 NDCG/MRR 指标报告与可复现改进方案。
```

## High-Pressure Questions

1. 召回、粗排、精排、rerank 分别解决什么问题？
2. 你怎么定义 query-doc 相关性？
3. NDCG 和 MRR 的区别是什么？
4. 长尾 query 为什么难？
5. LLM 在搜索里具体放在哪一段？
6. DOC 理解中的权威性、时效性、质量怎么建模？
7. 你怎么构造负样本？
8. 如果线上 CTR 变差但离线 NDCG 变好，你怎么排查？
