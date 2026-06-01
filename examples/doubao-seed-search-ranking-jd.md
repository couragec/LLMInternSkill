# Example JD: Doubao Seed Search / Ranking Research Internship

Use this as a realistic `target_jd.txt` example for search/ranking + LLM roles.

## Raw JD

```text
Top Seed人才计划-豆包大模型研究实习生专项:
面向2025年9月及以后毕业的博士及本硕在读同学，加入我们，你可以自主决定研究课题，与正式员工享受同等权限和资源，和优秀的研究员一起，向智能上限发起挑战。

团队介绍:
字节跳动豆包大模型团队(Seed)成立于2023年，致力于寻找通用智能的新方法，追求智能上限，并探索新的交互。团队研究方向涵盖LLM、语音、视觉、世界模型、基础架构、AI Infra、下一代AI交互等，在中国、新加坡、美国等地设有实验室和岗位。豆包大模型团队在AI领域拥有长期愿景与决心，坚持深耕基础，期望成为世界一流的AI研究团队，为科技和社会发展作出贡献。目前团队已推出业界领先的通用大模型及前沿的多模态能力，支持豆包、扣子、即梦等超过50个应用场景。

岗位方向:
1. 利用大模型优化搜索相关性、权威性、时效性等模型，解决各种复杂长尾查询的 Ranking 问题。
2. 利用大模型做 DOC 理解，筛选优质 DOC 以及更好支持在线检索。
3. 大模型在搜索召回和粗排等阶段的应用。

职位要求:
1. 2026届及以后本科及以上学历在读，人工智能、计算机、自动化、数学相关专业优先。
2. 优秀的代码能力、数据结构和基础算法功底，熟练掌握 C/C++ 或 Python。
3. 熟悉深度学习和 LLM 相关的算法和技术，有一定的算法应用实习经验。
4. 良好的沟通协作能力，有出色的数据和问题分析能力，对新问题能够独立探索解决方案。
5. 有搜索算法经验以及 ACM/ICPC、NOI/IOI、Top Coder、Kaggle 等比赛获奖者优先。
```

## Role Detection

```text
primary role: search-ranking
secondary role: llm-algorithm
supporting role: rag / doc-understanding
fit style: research internship, evidence-heavy
```

## Must-Haves

| Requirement | Hidden Interview Test |
| --- | --- |
| 搜索相关性 / Ranking | Can explain recall, rough rank, fine rank, rerank, query-doc relevance, metrics. |
| LLM for search | Knows where LLM helps: query rewrite, doc representation, rerank, judge, synthetic labels. |
| DOC 理解 | Can talk about structure, authority, freshness, quality, spam, long documents. |
| Python/C++ and algorithms | Can code and reason about data structures, retrieval, ranking metrics. |
| Deep learning / LLM | Understands model basics, fine-tuning/eval, not only API calls. |
| Problem analysis | Can show bad cases, labels, baselines, metrics, and iteration logic. |

## High-Risk Claims

- "提升搜索相关性" without query-doc labels or ranking metric.
- "使用 LLM 优化召回" without baseline, recall@K, or failure analysis.
- "做 DOC 理解" without document quality criteria or examples.
- "熟悉 LLM 算法" with only prompt/API evidence.
