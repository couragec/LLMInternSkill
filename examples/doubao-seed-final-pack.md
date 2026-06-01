# Example Output: Doubao Seed Search / Ranking Final Pack

This is the expected style for `10_final_pack.md` when the candidate has weak-to-medium evidence.

## 1. Fit Verdict

```text
Verdict: risky fit
Why: The JD is search/ranking + LLM research oriented. The candidate has adjacent RAG and small search demo evidence, but lacks ranking metrics, strong algorithm internship evidence, and doc-understanding experiments.
Strongest match: Mini search demo with query-doc examples and bad-case notes.
Biggest gap: No NDCG/MRR report and no LLM-for-ranking experiment.
Highest interview risk: Claiming "优化搜索相关性" without being able to explain recall/rank/rerank and metrics.
Fastest useful upgrade: Convert the mini search demo into a reproducible BM25 vs embedding vs rerank comparison with NDCG@10/MRR and bad-case analysis.
```

## 2. JD Analysis

| JD Requirement | Hidden Interview Test | User Evidence | Strength | Strategy |
| --- | --- | --- | --- | --- |
| 搜索相关性 / Ranking | Explain query-doc relevance, recall/rank/rerank, NDCG/MRR | 30 query-doc examples, no metric table | medium | Lead with offline analysis, not "improved ranking" |
| DOC 理解 | Quality, authority, freshness, long-doc structure | 12 bad cases, no rubric | weak | Add doc quality labels before writing strong claim |
| LLM + deep learning | Knows LLM basics and eval | notes only | weak | Say "学习/复现理解", not "训练大模型" |
| Code ability | Python scripts, reproducibility | scripts exist, README weak | medium | Add run command and clean README |

## 3. Truth Boundary

| Claim / Experience | Status | Can Write? | Evidence | Risk |
| --- | --- | --- | --- | --- |
| 优化知识库问答效果 | 补证据后写 | Not yet | RAG demo, no eval | Sounds like fake metric |
| 完成企业文档问答系统 | 谨慎写 | Yes, as demo | code + screenshot | Avoid production wording |
| 搜索排序相关性分析 | 可以写 | Yes | query-doc examples + bad cases | Add metric to strengthen |
| 熟悉 LLM 算法 | 谨慎写 | Notes only | learning notes | Do not imply training experience |

## 4. Evidence Contract

| Resume Claim | Evidence | Status | Safer Wording | Interview Proof |
| --- | --- | --- | --- | --- |
| 围绕搜索相关性整理长尾 query-doc bad case | 30 examples + 12 bad cases | 可以写 | Keep | Show bad-case table and label rules |
| 复现 BM25/embedding/rerank baseline | notebook exists, rerank missing | 补证据后写 | 复现 BM25 与 embedding retrieval baseline | Run rerank and save metrics first |
| 优化 RAG 效果 | no eval | 不能写 as strong result | 梳理 RAG 召回错误与引用错位问题 | Show retrieved chunks and failure cases |

## 5. Targeted Resume Bullets

### Conservative

```text
围绕搜索相关性场景整理 30 组 query-doc 样例和 12 类长尾查询 bad case，分析歧义查询、时效性不足、低权威 DOC 等失败原因，梳理召回、粗排、重排阶段的输入输出与评估口径。
```

```text
完成企业文档问答 demo 的文档切分、向量检索和 Prompt 模板配置，记录召回错误、引用错位和无依据回答等问题，为后续 RAG 评估集建设沉淀样例。
```

### Standard After 1-Day Upgrade

```text
基于小规模 query-doc 样例集对比 BM25、embedding 召回与 cross-encoder rerank baseline，使用 NDCG@10 / MRR 评估相关性表现，并输出长尾查询失败案例分析报告。
```

### Stronger After Evidence

```text
构建可复现的搜索相关性离线评估流程，围绕长尾查询、DOC 质量与时效性特征设计标注样例和 rerank 对比实验，沉淀指标报告、bad-case taxonomy 与后续优化方向。
```

## 6. Interview Grilling

1. 召回、粗排、精排、rerank 分别解决什么问题？你的 demo 属于哪一层？
2. 你怎么定义 query-doc 相关性？三档标签的边界是什么？
3. 为什么 NDCG@10 比 accuracy 更适合排序？
4. BM25 和 embedding retrieval 在长尾 query 上分别容易错在哪里？
5. DOC 权威性和时效性怎么变成可计算特征？
6. LLM 可以在哪些位置帮助搜索？哪些位置成本太高？
7. 你的 RAG demo 有没有 citation？无答案时会不会拒答？
8. 如果线上 CTR 上升但人工相关性下降，你怎么排查？

## 7. Answer Card

Question:

```text
你说你优化了搜索排序，指标提升多少？
```

Dangerous answer:

```text
提升挺明显的，用户看到的结果更准了。
```

Passable answer:

```text
我现在不会写线上提升，因为没有线上流量和 CTR 记录。我做的是离线 query-doc 分析和 baseline 复现。
```

Strong answer after upgrade:

```text
我用固定的 query-doc 样例集比较 BM25、embedding retrieval 和 cross-encoder rerank，并用 NDCG@10 / MRR 记录结果。我的重点是长尾 query bad-case taxonomy 和可复现评估流程，不把它包装成线上优化。
```

Evidence needed:

```text
metric table, run command, labels, bad-case report, notebook or script
```

Resume wording to downgrade:

```text
Remove "提升搜索排序效果". Use "复现并分析搜索相关性 baseline".
```

## 8. Upgrade Plan

| Time | Task | Evidence Produced | Resume Claim Unlocked |
| --- | --- | --- | --- |
| Half day | Draw search pipeline and define labels | diagram + label guide | Can explain recall/rank/rerank |
| 1 day | Add NDCG@10/MRR for BM25 and embedding | metric table + notebook | Baseline comparison |
| 3 days | Add cross-encoder rerank and doc quality labels | rerank report + bad cases | LLM-assisted rerank analysis |
| 1 week | Publish reproducible mini search repo | README + scripts + examples | Strong personal project |

## 9. Project Scout

Recommended directions:

1. MiniMind-style from-scratch LLM repo for LLM algorithm basics.
2. Small search/rerank baseline repo for BM25, embedding retrieval, and cross-encoder rerank.
3. RAG evaluation repo focused on citation accuracy and answer grounding.

Hard boundary:

```text
Do not write these as internship experience. Write them only after reproduction, modification, logs, and a short report exist.
```
