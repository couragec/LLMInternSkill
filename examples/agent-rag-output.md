# Example Output: Agent + RAG Internal Assistant

## Fit Verdict

```text
Verdict: weak fit
Why: The candidate has relevant LLM app, RAG, and tool-calling demos, but lacks evaluation, citation grounding, trace logs, and failure handling.
Strongest match: Has real retrieval and tool-call artifacts.
Biggest gap: No eval set or trace-level evidence.
Highest interview risk: Overclaiming "enterprise-grade" and "accuracy improvement".
Fastest useful upgrade: Add query-answer-evidence eval samples, retrieved-chunk logs, and schema validation for tool calls.
```

## Truth Boundary

| Claim | Status | Safe Wording |
| --- | --- | --- |
| 企业级 RAG 系统 | 不能写 | 企业文档问答 demo / 原型 |
| 提升回答准确率 | 补证据后写 | 整理 bad case 并建立评估样例 |
| Agent 自动化办公流程 | 谨慎写 | 实现两类工具调用原型 |
| 优化 Prompt | 谨慎写 | 维护 Prompt 模板并分析格式错误、幻觉、引用缺失 |

## Targeted Resume Bullets

Conservative:

```text
参与企业文档问答 demo 开发，负责文档切分、向量检索和 Prompt 模板配置，整理 25 条问答样例与召回错误、引用缺失、无依据回答等 bad case。
```

```text
实现日程查询和报销状态查询两类工具调用原型，梳理工具 schema、参数缺失和调用失败样例，为后续 Agent trace 日志和失败重试设计提供依据。
```

Standard after 1-day upgrade:

```text
为 RAG 问答链路补充 query-answer-evidence 样例、retrieved chunk 日志和拒答规则，基于 citation accuracy 与 answer relevance 分析回答可靠性。
```

```text
为 Agent 工具调用链路补充 JSON schema 校验、trace_id 日志和超时失败记录，基于固定任务样例统计工具调用成功率与失败类型。
```

## Interview Grilling

1. 你的 RAG demo 每个答案有没有证据链？怎么定位到 chunk？
2. 25 条问题有没有标准答案？没有的话怎么评估？
3. chunk size、top_k、embedding 模型怎么选？
4. 什么时候应该拒答？
5. 你的 Agent 和 chatbot 有什么区别？
6. 工具参数缺失怎么办？工具超时怎么办？
7. trace 日志记录什么？哪些信息不能记录？
8. 你所谓的 "准确率提升" 是怎么定义的？

## Upgrade Plan

| Time | Task | Evidence Produced | Claim Unlocked |
| --- | --- | --- | --- |
| Half day | Add retrieved chunk logging and 10 bad cases | logs + bad-case table | RAG bad-case analysis |
| 1 day | Build 30 query-answer-evidence examples | eval samples | Citation/answer eval |
| 3 days | Add schema validation, retry, and trace_id | traces + error table | Agent reliability work |
| 1 week | Add fixed eval suite and report | report + metrics | Stronger LLM app engineering project |
