# Resume Tailoring

Goal: generate a targeted resume without inventing experience.

## Process

1. Start from JD must-haves.
2. Select only evidence-backed experiences.
3. Rank projects by JD relevance and interview survivability.
4. Write bullets at three strengths:
   - conservative: current evidence supports it.
   - standard: minor evidence upgrades needed.
   - stronger after evidence: only after concrete upgrades.
5. Remove or downgrade claims that fail the evidence contract.

## Bullet Formula

```text
Action + technical object + constraint/bad case + evidence/result
```

Good:

```text
围绕企业文档问答场景整理 50 条 query-answer-evidence 样例，分析召回错、引用错位和无依据回答等 bad case，并基于 citation accuracy 与 answer relevance 形成评估口径。
```

Too vague:

```text
负责 RAG 效果优化，显著提升准确率。
```

## Output

```markdown
## Resume Strategy

## Conservative Bullets

## Standard Bullets

## Stronger After Evidence

## Full Resume Draft

## Claims To Remove Or Downgrade
```

## LaTeX Template

When the user wants a final PDF-ready resume, use the downloaded Bill Ryan elegant LaTeX template:

```text
templates/resume-latex/bill-ryan-elegant-zh_CN/
```

Use `resume-zh_CN.tex` as the Chinese starting point and compile with XeLaTeX. Keep upstream attribution and license files. Do not commit or redistribute large CJK font bundles unless their license is confirmed.
