# Resume Polish

Goal: make resume lines clearer, stronger, and more technical without inventing facts.

Use this when the user asks for:

- 简历润色
- 简历优化
- 技术表达增强
- 中文/英文简历改写
- ATS keyword suggestions
- Before/After comparison
- line-by-line diagnosis

## Core Rule

```text
Polish expression, not reality.
```

If a strong verb, metric, ownership word, production claim, or model claim lacks evidence, downgrade the wording or mark it `补证据后写`.

## Process

1. Split the resume into lines or claims.
2. For each line, identify:
   - role target
   - action
   - technical object
   - ownership
   - metric/result
   - evidence
   - interview risk
3. Classify each line:
   - `可直接润色`
   - `谨慎润色`
   - `先补证据`
   - `建议删除/降级`
4. Produce three versions:
   - **clean**: clearer and more concise.
   - **technical**: more concrete engineering language.
   - **JD-targeted**: aligned with the target JD when present.
5. Add interview-risk notes for lines likely to trigger deep questions.

## Polish Levels

| Level | When To Use | Output Style |
| --- | --- | --- |
| Clean | The line is true but vague | concise, readable, no overclaim |
| Technical | There is technical evidence | add pipeline, model, metric, tool, failure case |
| JD-targeted | A target JD is present | reorder emphasis around JD must-haves |
| Evidence-upgraded | User can still collect proof | stronger wording gated by required evidence |

## Good Bullet Formula

```text
Action + technical object + constraint / bad case + evidence or result
```

Examples:

```text
整理 30 组 query-doc 样例与长尾查询 bad case，分析歧义查询、时效性不足和低权威 DOC 对搜索相关性的影响。
```

```text
为 RAG demo 补充 retrieved chunk 日志和 query-answer-evidence 样例，定位召回错误、引用错位和无依据回答等问题。
```

## Dangerous Words

Downgrade unless evidence exists:

| Risky Word | Evidence Needed | Safer Wording |
| --- | --- | --- |
| 主导 | ownership docs, code, design decisions | 参与 / 负责某模块 |
| 上线 | release record, traffic, users, logs | demo / 内部试用 / 本地验证 |
| 提升 X% | metric definition, baseline, report | 对比分析 / 建立评估口径 |
| 训练大模型 | dataset, config, logs, checkpoint | 复现小模型训练 / 学习训练流程 |
| 企业级 | production requirements, scale, reliability | 企业文档问答 demo / 内部原型 |

## Output Format

```markdown
## Resume Polish Verdict

## Before / After

| Original | Clean | Technical | JD-Targeted | Status | Interview Risk |
| --- | --- | --- | --- | --- | --- |

## Lines To Downgrade Or Remove

## Evidence To Add

## Final Polished Version

## Optional English Version
```

## English Version Rules

- Keep English direct and compact.
- Do not translate Chinese overclaims literally.
- Prefer "built a demo", "reproduced a baseline", "analyzed failure cases", "implemented logging", "created an evaluation set".
- Avoid "led", "owned", "productionized", "improved by X%" unless proven.

