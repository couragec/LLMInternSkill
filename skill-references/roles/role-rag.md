# Role: RAG / Knowledge Base QA

Use for JD keywords such as RAG, knowledge base, retrieval, citation, document QA, hallucination, chunking, rerank, and evaluation.

## What Big Companies Care About

- Data ingestion and document parsing.
- Chunking, metadata, embedding, vector store, recall, rerank.
- Citation grounding and no-answer refusal.
- Evaluation set and metrics: retrieval hit, citation accuracy, answer relevance, refusal accuracy.
- Bad cases: hallucination, wrong citation, table failure, cross-page context, permissions.
- Latency, cost, trace logs, and iteration workflow.

## Toy Signals

- Only calls an API with a prompt.
- No eval set.
- No citation or evidence chain.
- No bad cases.
- No permission or freshness thinking.

## Upgrade Actions

Half day:

- Draw RAG pipeline.
- Collect 10 bad cases.
- Add metadata fields: doc_id, page, section, chunk_id.

1 day:

- Create 30-50 query-answer-evidence examples.
- Add citation output and refusal rule.
- Log retrieved chunks and final answer.

3 days:

- Compare chunk size, top_k, and rerank choices.
- Build simple eval report.
- Add table/cross-page examples.

1 week:

- Add permission filtering, caching, monitoring, and a small review UI or report.

## Safe Resume Bullets

Conservative:

```text
参与知识库问答原型开发，负责文档切分、Prompt 模板维护和问答样例整理，梳理召回错误、引用错位和无依据回答等 bad case。
```

Standard:

```text
基于 query-answer-evidence 样例集对比 chunk size、top_k 与 rerank 策略，记录召回命中、引用准确和答案可用性，为 RAG 迭代建立离线评估口径。
```

## High-Pressure Questions

1. chunk size 怎么选？
2. top_k 太大或太小会怎样？
3. 什么时候需要 rerank？
4. 怎么证明答案有依据？
5. 无答案时怎么拒答？
6. 表格和跨页内容怎么处理？
7. 权限过滤怎么做？
8. 你怎么证明效果提升？
