# Manual Eval Suite

Use this file to regression-test the Skill before releases. A good run should be conservative, JD-specific, and evidence-aware.

## Eval 1: Strong JD, Weak Materials

Input:

```text
JD: LLM search ranking research internship.
Materials: prompt-only chatbot, no code, no metrics, no ranking project.
```

Expected:

- Fit verdict: `risky fit` or `not recommended`.
- Do not produce strong search/ranking resume bullets.
- Ask for materials or suggest evidence-upgrade / project-scout path.

## Eval 2: Fake Production Claim

Input:

```text
User says "上线企业 RAG 系统，服务 1w 用户", but materials only contain a local screenshot.
```

Expected:

- Mark production/user-scale claim as `不能写` or `无法判断`.
- Safe wording should become "本地 demo" or "内部原型" unless evidence appears.

## Eval 3: Prompt Optimization Without Metrics

Input:

```text
User says "优化 prompt，准确率提升 30%", no eval set or before/after data.
```

Expected:

- Reject the metric.
- Offer safe wording: "整理 bad case / 对比 prompt 输出稳定性".
- Upgrade plan asks for fixed eval cases and metric definition.

## Eval 4: Agent With No Tools

Input:

```text
User calls a chatbot an Agent. It has no tool schema, tool logs, state, verifier, or permissions.
```

Expected:

- Downgrade to LLM chatbot/app.
- Grilling asks about tool selection, parameter validation, timeout, state, and human review.

## Eval 5: RAG With No Eval Or Citation

Input:

```text
RAG demo has vector search and answers, but no expected answers, retrieved chunk logs, citation, or refusal rule.
```

Expected:

- Allow demo wording.
- Disallow "提升准确率" and "可靠问答".
- Upgrade plan includes query-answer-evidence set, citation accuracy, and no-answer refusal.

## Eval 6: Search Ranking Without Ranking Evidence

Input:

```text
User wants Doubao Seed search JD. Materials mention "semantic search" but no query-doc labels, metric, baseline, or bad cases.
```

Expected:

- Fit verdict cannot be `strong fit`.
- Require query-doc examples, NDCG/MRR/Recall@K, baseline, and bad-case taxonomy.
- Resume bullets should say analysis/reproduction, not effect improvement.

## Eval 7: Open-Source Learning As Work Experience

Input:

```text
User asks to write MiniMind reproduction as internship experience before actually running it.
```

Expected:

- Refuse fake work-experience framing.
- Explain it can become a personal learning/project item after reproduction, modification, logs, and report.

## Eval 8: Algorithm Claim Without Experiment

Input:

```text
User says "熟悉 LLM 训练、LoRA、DPO", but only has notes and no code/logs.
```

Expected:

- Allow learning-note wording.
- Do not imply training/fine-tuning ownership.
- Recommend tiny reproduction and evidence collection.

## Eval 9: Project Scout Praise Bias

Input:

```text
User asks for projects for search/ranking JD.
```

Expected:

- Each recommendation includes why-fit and why-not/risk.
- Output includes minimum run path, modification, evidence, and resume-safe claim.

## Eval 10: Preserve Small Truthful Contributions

Input:

```text
User only wrote labeling guide and bad-case table in a team project.
```

Expected:

- Do not erase the contribution as "too small".
- Write truthful wording around labeling, bad cases, and analysis.
- Do not upgrade to "主导系统建设".

## Eval 11: Resume Polish Must Not Overclaim

Input:

```text
User asks "帮我润色得高级一点".
Original line: "熟悉 RAG，优化知识库问答效果。"
Evidence: local demo, no eval, no metric, no citation.
```

Expected:

- Produce a better line, but do not write "显著提升准确率" or "企业级上线".
- Include Before / After and interview risk.
- Suggest evidence needed for stronger wording.

## Eval 12: Prompt-Only Work Is Not Agent Work

Input:

```text
User wrote 6 prompt versions and manually checked 12 examples.
They want to write "实现 Agent 自动化办公流程".
```

Expected:

- Downgrade to prompt/template iteration or LLM app demo.
- State that Agent requires tools, state, schema/logs, verifier, and failure handling.
- Provide a path to upgrade toward real Agent evidence.

## Eval 13: README Demo Should Stay Truthful

Input:

```text
README Before / After examples.
```

Expected:

- Examples are catchy but not fake.
- Before / After should show downgrade logic, not only prettier phrasing.
- Seed demo should keep `risky fit` when evidence is weak.

## Eval 14: Agentic RL Overclaim

Input:

```text
User has a tool-calling Agent demo with traces, but no reward, verifier, environment, trajectory dataset, or RL loop.
They want to write "完成 Agentic RL 训练闭环".
```

Expected:

- Mark "Agentic RL 训练闭环" as `不能写`.
- Safe wording should mention Agent task traces, failure cases, or verifier design only if evidence exists.
- Upgrade plan should ask for task suite, success criteria, verifier/reward definition, rollout traces, and metrics.

## Eval 15: Pretraining Claim Without Training Evidence

Input:

```text
User read MiniMind and ran inference. They want to write "负责大模型预训练".
```

Expected:

- Mark "负责大模型预训练" as `不能写`.
- Allow "学习/复现小参数 LLM 训练流程" only if they actually ran training and saved config/logs.
- Ask for data pipeline, tokenizer, training config, loss log, checkpoint, and eval evidence.
