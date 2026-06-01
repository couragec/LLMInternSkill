# Project Scout

Goal: recommend open-source projects that help the user fill JD gaps through real learning, reproduction, modification, and evidence collection.

## When To Use

- User asks for projects to learn.
- Materials are too weak for a JD.
- The fit verdict is `weak fit` or `risky fit` because of missing project evidence.
- The upgrade plan needs a concrete external project.

## Search Strategy

Search by combining:

```text
role keywords + mechanism keywords + "github" + "from scratch" / "tutorial" / "benchmark" / "rerank" / "agent" / "RAG"
```

Examples:

- `from scratch LLM training github`
- `search ranking rerank LLM github`
- `RAG evaluation citation accuracy github`
- `agent tool calling workflow github`
- `LLM inference quantization serving github`

## Scoring

| Criterion | Meaning |
| --- | --- |
| JD relevance | Directly maps to target JD. |
| Learning value | Teaches mechanisms, not just API usage. |
| Reproducibility | Can run under user's time/hardware. |
| Evidence potential | Can produce logs, metrics, code diffs, report. |
| Interview value | Supports deep questions. |
| Upgrade potential | User can add a meaningful modification. |
| Risk | License, complexity, stale repo, too hard, too shallow. |

## Output

```markdown
## Search Queries

## Candidate Table

| Repo | Fit | Minimum Run | Modification | Evidence | Risk |
| --- | --- | --- | --- | --- | --- |

## Top 3 Recommendations

## Study Plan

## Resume-Safe Claims After Completion

## Interview Grilling Questions
```

Hard boundary:

```text
Open-source learning is not internship experience.
Only write what the user actually reproduced, understood, modified, and documented.
```
