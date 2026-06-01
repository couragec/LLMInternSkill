# Project Scout Example: Search / Rerank For Doubao Seed

Use this when the target JD asks for search relevance, DOC understanding, recall, rough rank, or LLM-assisted rerank.

## Target Gap

```text
The candidate has RAG or semantic-search experience, but lacks search-ranking evidence:
- no query-doc labels
- no BM25 / embedding / rerank baseline
- no NDCG / MRR / Recall@K
- no long-tail query bad-case taxonomy
```

## Search Queries

```text
github search rerank bm25 embedding cross encoder
github information retrieval learning to rank python
github pyserini bm25 dense retrieval rerank tutorial
github sentence transformers cross encoder reranking example
github rag evaluation citation accuracy retrieval benchmark
```

## Candidate Project Types

| Type | Why It Fits | Why Not / Risk | Evidence Potential |
| --- | --- | --- | --- |
| BM25 + dense retrieval tutorial | Best first baseline for search pipeline understanding | May be too shallow if no labels or metrics are added | query-doc examples, Recall@K, bad cases |
| Cross-encoder rerank demo | Directly maps to LLM-assisted reranking | Needs careful explanation of cost and latency | NDCG@10/MRR comparison |
| Pyserini-style IR baseline | Strong search/retrieval learning value | Setup can be heavier | reproducible scripts, metric table |
| RAG eval repo | Useful for citation and answer grounding | Not enough for ranking unless query-doc metrics are added | citation accuracy, answer relevance |
| Learning-to-rank toy project | Useful for ranking features and labels | May not involve LLM | feature table, label guide, metric report |

## Recommended 3-Day Plan

Day 1:

```text
Build 30-50 query-doc examples with relevance labels.
Run BM25 and embedding retrieval.
Record Recall@10 and failure cases.
```

Day 2:

```text
Add cross-encoder rerank on top-k candidates.
Compute NDCG@10 and MRR.
Categorize long-tail failures: ambiguity, freshness, authority, low-quality DOC, exact-match miss.
```

Day 3:

```text
Write a short report:
- search pipeline diagram
- label definition
- metric table
- before/after examples
- why rerank helps or fails
- cost/latency tradeoff
```

## Resume-Safe Claim After Completion

```text
基于 30-50 组 query-doc 样例复现 BM25、embedding retrieval 与 cross-encoder rerank baseline，使用 Recall@10、NDCG@10 和 MRR 对比搜索相关性表现，并沉淀长尾查询 bad-case taxonomy。
```

## Interview Grilling

1. 召回、粗排、精排、rerank 分别解决什么问题？
2. 为什么 rerank 不直接替代 recall？
3. NDCG 和 MRR 的差异是什么？
4. 你的 relevance label 怎么定义？
5. Cross-encoder rerank 的成本和延迟怎么控制？
6. DOC 权威性和时效性怎么建模？
7. 如果 embedding retrieval 找不到正确 DOC，rerank 还有用吗？

