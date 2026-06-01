# Evidence Contract

Every strong resume claim needs evidence.

## Claim Levels

| Level | Expression | Evidence Needed |
| --- | --- | --- |
| C0 | 了解 / 参与 | Notes, explanation, course material, project docs |
| C1 | 负责模块 | Code, README, screenshots, logs, task notes |
| C2 | 设计 / 优化 | Experiment, comparison, bad cases, design document |
| C3 | 结果影响 | Metric definition, baseline, logs, report, rollout record |

C3 claims are not allowed without metric definitions and records.

## Common Claims

| Claim | Minimum Evidence | Safe Wording If Missing |
| --- | --- | --- |
| 优化 RAG 效果 | eval set, bad cases, retrieval/citation metrics | 整理 RAG bad case 并提出优化方向 |
| 提升搜索相关性 | query-doc labels, NDCG/MRR/CTR, baseline | 分析长尾 query 和相关性失败样例 |
| 支持线上业务 | release/internal trial/user logs | 完成内部 demo 或流程验证 |
| Agent 工具调用 | tool schema, logs, failure cases | 梳理工具调用流程与失败类型 |
| 训练/微调模型 | dataset, script, config, metrics | 复现训练流程或完成小规模微调实验 |

## Output

```markdown
| Resume Claim | Level | Evidence | Status | Safer Wording | Interview Proof |
| --- | --- | --- | --- | --- | --- |
```
