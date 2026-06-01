# Interview Grilling

Goal: generate interviewer-style questions that expose weak claims before the real interview.

## Rounds

1. Truth boundary: what did you actually do?
2. Technical depth: input/output, data, model, system, metrics.
3. JD-specific deep dive: match the target role.
4. Scenario questions: failure, latency, quality drop, data drift, permissions.
5. Summary score: can answer / needs evidence / high risk / cannot write.

## Question Style

Ask questions that follow the user's claims.

Bad:

```text
请介绍 RAG。
```

Good:

```text
你说优化了 RAG 召回，具体是 chunk、embedding、top_k、rerank 还是 prompt 改了？每一步怎么证明有效？
```

## Output

```markdown
## Round 1: Truth Boundary

## Round 2: Technical Depth

## Round 3: JD-Specific Deep Dive

## Round 4: Scenario Questions

## Round 5: Risk Summary
```

Each question should include why it matters and what evidence would answer it.
