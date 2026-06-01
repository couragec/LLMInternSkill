# Project Search Criteria

Use this when the user asks for open-source projects to learn, reproduce, or modify.

## User Inputs

```text
Target JD:
Current gap:
Time budget:
Hardware:
Preferred language:
Can publish repo? yes/no
Interest: RAG / Agent / LLM algorithm / search ranking / AIGC / backend AI / multimodal
```

## Ranking Rubric

| Criterion | What To Check |
| --- | --- |
| JD relevance | Does it map to explicit JD requirements? |
| Learning value | Does it teach real mechanisms, not just API usage? |
| Reproducibility | Can the user run a minimal path with their hardware/time? |
| Readability | Can a student read and explain the code? |
| Maintenance | Recent commits, issues, docs, examples. |
| License | Safe to study, fork, or extend. |
| Evidence potential | Can it produce logs, reports, metrics, screenshots, code diffs? |
| Interview value | Can it support deep questions? |
| Upgrade potential | Can the user add a small but meaningful modification? |

## Output Requirements

For each recommended project:

```text
repo:
why this fits:
what to run first:
what to read first:
what to modify:
what evidence to collect:
resume-safe claim after completion:
interview questions:
why not / risk:
```
