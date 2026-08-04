<div align="center">

# LLMInternSkill / LLM Intern Skill

**English** | [简体中文](README.md)

**An evidence-bound resume and job-search toolkit for LLM internships: resume polishing, JD tailoring, RAG / Agent / post-training project packaging, interview grilling, and open-source project scouting.**

<sub>Built for LLM internships, AI job applications, and Codex Skill workflows. It does more than make a resume sound better: every line should survive follow-up questions in a real interview.</sub>

<sub>Keywords: LLM internship resume, Codex Skill, resume polish, JD tailoring, interview prep, RAG, Agent, post-training, pretraining, search ranking, AIGC, multimodal.</sub>

<br>
<br>

![Type](https://img.shields.io/badge/type-Codex%20Skill-111827)
![License](https://img.shields.io/badge/license-MIT-blue)
![Focus](https://img.shields.io/badge/focus-LLM%20Internship-4f46e5)
![Method](https://img.shields.io/badge/method-evidence--bound-f59e0b)
![Language](https://img.shields.io/badge/language-ZH%20%2B%20EN-10b981)
![Status](https://img.shields.io/badge/status-final%20MVP-ec4899)
![GitHub Repo stars](https://img.shields.io/github/stars/wanyichen06/LLMInternSkill?style=flat&label=stars)

[30-second overview](#30-second-overview) · [Quick start](#quick-start) · [Seed example](#flagship-example-doubao-seed-search--ranking) · [Feature map](#feature-map) · [Star history](#star-history) · [References](#references)

</div>

---

## 30-second overview

| What you provide | What the Skill does |
| --- | --- |
| A raw resume | 📝 Rewrites it into clearer, more technical, internship-ready language |
| A target job description | 🎯 Assesses fit, reorders experience, and produces a targeted resume |
| A materials folder | 🔍 Audits code, project artifacts, paper notes, logs, screenshots, and awards |
| Several thin projects | 🧪 Turns real work into defensible project stories and identifies missing evidence |
| A resume you worry cannot survive an interview | 🎤 Generates interviewer-style follow-ups and dangerous / passable / strong answer cards |
| Insufficient evidence | 🌱 Recommends open-source projects to reproduce, modify, and document |
| A final application package | 📄 Produces a PDF-ready draft with the Bill Ryan LaTeX template |

Core truth-boundary verdicts:

```text
safe to write / write with caution / write after adding evidence /
do not write / cannot determine
```

Core workflow:

```text
raw resume + materials/ + target_jd.txt
-> resume polish
-> JD fit analysis
-> truth boundary
-> Evidence Contract
-> targeted resume
-> interview grilling
-> answer cards
-> evidence upgrade plan
-> Project Scout
-> LaTeX resume draft
```

---

## Before / After at a glance

<table>
  <tr>
    <th width="28%">Raw resume line</th>
    <th width="36%">Evidence-safe rewrite</th>
    <th width="36%">Why</th>
  </tr>
  <tr>
    <td>Familiar with LLMs and RAG; optimized search quality.</td>
    <td>Collected query-document examples and long-tail search failures for a relevance-focused search prototype; analyzed ambiguous queries, stale information, and low-authority documents that degraded retrieval quality.</td>
    <td>Without metrics, do not claim a measured improvement. Express the evidence as problem-analysis work instead.</td>
  </tr>
  <tr>
    <td>Built an enterprise-grade knowledge-base QA system.</td>
    <td>Implemented document chunking, vector retrieval, and prompt templates for a document QA demo; recorded retrieval misses, citation misalignment, and unsupported answers.</td>
    <td>Without deployment, access control, monitoring, or user evidence, do not call it an enterprise-grade system.</td>
  </tr>
  <tr>
    <td>Trained a large language model and improved generation quality.</td>
    <td>Reproduced the training and inference workflow of a small language model; documented configuration, logs, sample outputs, and failure cases to build an end-to-end understanding.</td>
    <td>Without data, configurations, training logs, and checkpoints, do not claim that you trained a large model.</td>
  </tr>
</table>

One-line rule:

```text
Polishing can make real experience clearer and more technical.
It cannot turn unsupported experience into fact.
```

---

## Quick start

### Option 1: Resume polish only

```text
Use LLMInternSkill.
Please polish my resume without fabricating experience.

Target role:
[paste the JD or describe the role]

Raw resume:
[paste the resume]

Please provide:
1. Before / After
2. Which lines are safe and which should be downgraded
3. A more technical version
4. A JD-targeted version
5. Likely interview follow-up questions
```

### Option 2: Full materials folder

Prepare:

```text
materials/
├── target_jd.txt
├── resume.md
├── projects/
├── code/
├── notes/
├── papers/
├── awards/
└── other/
```

Then ask:

```text
Use LLMInternSkill on ./materials.
Generate resume polish, JD fit verdict, targeted resume, interview grilling,
answer cards, evidence upgrade plan, and project scout recommendations.
```

### Option 3: Install as a Codex Skill

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/wanyichen06/LLMInternSkill.git ~/.codex/skills/llm-intern-skill
```

Restart Codex or open a new session, then say:

```text
Use LLMInternSkill and read my materials/ folder.
```

The core [`SKILL.md`](SKILL.md) and workflow instructions are already written in English.

---

## Flagship example: Doubao Seed Search / Ranking

This example deliberately targets a demanding JD: a research internship in Search / Ranking / document understanding at the Doubao Foundation Model Seed team.

It demonstrates the project's central behavior:

```text
strong JD + weak or medium evidence
-> do not force a "strong fit" verdict
-> identify defensible evidence
-> downgrade risky claims
-> produce a conservative, usable resume
-> generate interviewer follow-up questions
-> propose 1-day / 3-day / 1-week evidence upgrades
```

Start with these files:

- [Target JD](examples/doubao-seed-search-ranking-jd.md)
- [Candidate materials](examples/doubao-seed-materials-input.md)
- [Final output pack](examples/doubao-seed-final-pack.md)
- [Sample LaTeX resume PDF](examples/seed-resume-latex/seed-topseed-resume.pdf)

Key output excerpt:

```text
Verdict: risky fit
Why: The candidate has RAG and a small search demo, but lacks ranking metrics,
strong algorithm-internship evidence, and document-understanding experiments.
Fastest upgrade: Extend the mini search demo into a BM25 vs. embedding vs. rerank
comparison with NDCG@10 / MRR and failure-case analysis.
```

---

## Feature map

| Icon | Module | Output |
| --- | --- | --- |
| 📝 | Resume Polish | Before/After, stronger technical wording, CN/EN versions, ATS keywords |
| 🎯 | JD Tailoring | JD match table, targeted resume, role-specific keyword ordering |
| 🔍 | Resume Diagnosis | Weak wording, risky claims, missing evidence, likely failure points |
| 🧪 | Project Packaging | Project bullets, architecture narrative, two-to-three-minute project story |
| 🛡 | Evidence Guard | Truth Boundary, Evidence Contract, safe downgrades for risky claims |
| 🎤 | Interview Drill | Line-by-line grilling, follow-up chains, dangerous / passable / strong answers |
| 🌱 | Project Scout | Open-source recommendations, minimum run path, modifications, collectable evidence |
| 📄 | LaTeX Export | Bill Ryan resume template and a PDF-ready draft |

---

## Output structure

Full mode produces:

```text
output/
├── 01_jd_analysis.md
├── 02_materials_audit.md
├── 03_truth_boundary.md
├── 04_evidence_contract.md
├── 05_resume_polish.md
├── 06_targeted_resume.md
├── 07_interview_grilling.md
├── 08_answer_cards.md
├── 09_upgrade_plan.md
├── 10_project_scout.md
└── 11_final_pack.md
```

Resume-polish mode prioritizes:

```text
1. Resume Polish Verdict
2. Before / After
3. Line-by-line diagnosis
4. Final polished resume section
5. Optional English version
6. Evidence upgrade list
```

---

## Supported roles

| Track | What the Skill checks |
| --- | --- |
| RAG / Knowledge-base QA | chunking, retrieval, reranking, citations, evaluation, refusal, access control |
| Agent / Tool Use | tool schema, argument validation, traces, retries, state, human review |
| Agentic RL | trajectories, environments, rewards/verifiers, GRPO/PPO, task success rate |
| Post-training / Alignment | SFT, DPO, RLHF/RLAIF, reward models, preference data, evaluation |
| Pretraining / Mid-training | data engines, tokenizers, training configuration, loss, distributed systems, contamination checks |
| LLM Application Engineering | structured output, prompt versions, failure cases, cost, latency |
| LLM Algorithms | Transformers, SFT/LoRA/DPO, training configuration, logs, evaluation |
| Search / Recommendation / Ranking | query-document data, retrieval, initial ranking, reranking, NDCG/MRR, document quality |
| AIGC | generation pipelines, quality evaluation, safety, human review, cost |
| Multimodal | OCR/layout, VLMs, cross-modal retrieval, visual failure cases |
| AI Backend | APIs, queues, retries, observability, permissions, deployment, cost |

---

## Why this is more than a resume rewriter

A typical resume rewriter often does only this:

```text
Turn an ordinary sentence into a polished sentence.
```

LLMInternSkill asks three additional questions:

```text
What evidence supports this sentence?
How will an interviewer challenge it?
If it is not safe today, what evidence would make it safe?
```

It will not turn:

```text
Built a RAG demo.
```

into:

```text
Led the production launch of an enterprise knowledge system and significantly
improved business efficiency.
```

It is more likely to write:

```text
Implemented document chunking, vector retrieval, and prompt templates for a
document QA demo; recorded retrieval misses, citation misalignment, and
unsupported answers to seed a query-answer-evidence evaluation set.
```

The difference: **stronger wording without fictional evidence.**

---

## Project Scout

When the current materials are too weak, LLMInternSkill recommends projects to complete instead of inventing claims.

Examples:

- MiniMind-style language-model training from scratch
- RAG evaluation and citation-accuracy projects
- Search / reranking baselines
- Agent tool-calling workflows
- LLM inference, serving, or quantization projects

Every recommendation must contain:

```text
why this fits
why not / risk
minimum run path
what to modify
what evidence to collect
resume-safe claim after completion
interview grilling questions
```

Boundary:

```text
Studying an open-source project is not work experience.
It becomes a defensible personal or open-source project only after you genuinely
reproduce, understand, modify, and document it.
```

Example: [MiniMind Project Scout](examples/project-scout-minimind.md)

More examples:

- [Resume Polish Before / After](examples/resume-polish-before-after.md)
- [Prompt-only Work Safely Downgraded](examples/prompt-only-downgrade.md)
- [Search / Rerank Project Scout](examples/project-scout-search-rerank.md)
- [LoRA Experiment With Weak Metrics](examples/lora-weak-metrics.md)
- [Post-training / Agentic RL Case](examples/posttraining-agentic-rl-case.md)
- [Seed Resume LaTeX Demo](examples/seed-resume-latex/README.md)

---

## LaTeX resume template

The default Chinese template is based on Bill Ryan's elegant LaTeX resume:

```text
templates/resume-latex/bill-ryan-elegant-zh_CN/
```

Sources:

- Overleaf: <https://www.overleaf.com/latex/templates/bill-ryans-elegant-latex-resume/xcqmhktmzmsw>
- Upstream: <https://github.com/billryan/resume>

Notes:

- Chinese entry file: `resume-zh_CN.tex`
- Compiler: XeLaTeX
- Upstream attribution and license are retained
- Large CJK fonts stay local and are not tracked by Git

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=wanyichen06%2FLLMInternSkill&type=Date)](https://www.star-history.com/#wanyichen06/LLMInternSkill&Date)

---

## References

This project learned from the following open-source projects. Thanks to their authors:

- [`resumify`](https://github.com/breaker505/resumify)
- [`shushu-internship-resume-optimizer`](https://github.com/Sunanzhe2004/shushu-internship-resume-optimizer)
- [`shushu-internship-tool`](https://github.com/LiuMengxuan04/shushu-internship-tool)
- [`shushu-ProjectProof`](https://github.com/YingaoWang-casia/shushu-ProjectProof)
- [`vibe-resume`](https://github.com/LiuMengxuan04/vibe-resume)
- [`resuml`](https://github.com/phoinixi/resuml)
- [`Auto-claude-code-research-in-sleep`](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep)

---

## Repository structure

```text
.
├── SKILL.md
├── skill-references/
│   ├── resume-polish.md
│   ├── resume-tailoring.md
│   └── roles/
├── templates/
│   ├── resume-polish-report.md
│   └── resume-latex/
├── examples/
├── evals/
├── docs/
└── agents/
```

Issues and pull requests with additional job descriptions, examples, role references, and evaluations are welcome.

## License

MIT. The bundled Bill Ryan resume template retains its upstream license and attribution; see `templates/resume-latex/README.md`.
