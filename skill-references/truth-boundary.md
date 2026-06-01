# Truth Boundary

Goal: prevent overclaiming while preserving the strongest truthful story.

## Status Labels

| Status | Meaning |
| --- | --- |
| 可以写 | Current evidence supports it. |
| 谨慎写 | Can write only with careful wording. |
| 补证据后写 | Plausible, but needs proof first. |
| 不能写 | Unsupported or false. |
| 无法判断 | Need user clarification. |

## Common Downgrades

| Unsafe | Safer |
| --- | --- |
| 主导系统建设 | 参与模块开发 / 负责某一子模块 |
| 上线生产 | 完成 demo / 内部试用 / 本地验证 |
| 提升准确率 30% | 基于样例对比观察到效果改善 |
| 训练大模型 | 复现小模型训练 / 做 LoRA 微调 / 调用模型 API |
| Agent 自动完成任务 | 在限定流程内完成工具调用和人工复核 |
| 优化搜索排序 | 梳理 query-doc bad case / 复现 rerank baseline |

## Output

For each important claim:

```text
claim:
status:
evidence:
risk:
safe wording:
question to user:
```
