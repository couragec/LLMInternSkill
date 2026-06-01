# Example: Prompt-Only Work Safely Downgraded

This example protects the Skill from turning prompt-only work into fake LLM engineering experience.

## Input

Target role:

```text
LLM 应用工程 / Agent 实习生
```

Original claim:

```text
负责公司大模型应用优化，通过 prompt engineering 显著提升回答准确率，并实现 Agent 自动化。
```

Actual evidence:

```text
- Wrote 6 prompt versions for a customer-service chatbot demo.
- Manually compared 12 examples.
- No fixed eval set.
- No accuracy metric.
- No tool calling.
- No logs or schema validation.
- No production deployment.
```

## Diagnosis

| Claim | Status | Reason |
| --- | --- | --- |
| 负责公司大模型应用优化 | 谨慎写 | Could be true only if scope is limited to prompt templates. |
| 显著提升回答准确率 | 不能写 | No metric, baseline, or eval set. |
| 实现 Agent 自动化 | 不能写 | No tools, state, verifier, or task execution. |

## Safe Rewrite

```text
参与客服问答 demo 的 Prompt 模板迭代，整理 12 条人工对比样例，分析格式不稳定、拒答不准确和回答不完整等问题。
```

## Stronger After Evidence

```text
基于固定客服问答评估集对比 6 版 Prompt 输出，记录 answer relevance、format validity 和 refusal accuracy，沉淀 bad-case 回归样例与提示词版本管理记录。
```

Required evidence:

```text
eval set, expected answers, metric definition, before/after table, prompt versions, logs
```

## Interview Grilling

1. 你说准确率提升，准确率定义是什么？
2. 12 条人工样例是否固定？有没有 expected answer？
3. prompt 改动后哪些 case 变好，哪些 case 变差？
4. 为什么这不是 Agent？
5. 如果模型输出 JSON 缺字段，你怎么处理？

