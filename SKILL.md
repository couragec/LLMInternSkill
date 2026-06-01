---
name: llm-intern-skill
description: Use when polishing, diagnosing, tailoring, or exporting resumes for LLM, RAG, Agent, Agentic RL, post-training, pretraining, AIGC, search/ranking, multimodal, AI backend, or LLM algorithm internships from raw resume text, a materials folder, and/or a target job description. Audits evidence, maps JD fit, enforces truth boundaries, writes polished and targeted resumes, generates interviewer-style grilling questions, answer cards, evidence-upgrade plans, and optional open-source project recommendations without fabricating experience.
---

# LLMInternSkill

Use this Skill when the user wants resume polish, resume diagnosis, JD tailoring, project packaging, interview preparation, or final resume export for LLM-related internship applications.

Core rule:

```text
Do not fabricate. Diagnose first, polish second.
```

## Inputs

Preferred input folder:

```text
materials/
├── target_jd.txt
├── resume.md / resume.pdf
├── projects/
├── code/
├── notes/
├── papers/
├── awards/
└── other/
```

If the user only provides a JD and no materials, ask the intake questions from `templates/intake.md`.

If the user only asks for resume polish, run a lightweight version:

```text
raw resume line -> claim extraction -> evidence/risk check -> polished wording -> interview risk
```

## Main Workflow

1. **Decide the mode**
   - Resume polish only: use `skill-references/resume-polish.md`.
   - JD tailoring: use `skill-references/jd-analysis.md` and `skill-references/resume-tailoring.md`.
   - Full materials folder: run the complete workflow below.
   - Interview prep only: use `skill-references/interview-grilling.md` and `skill-references/answer-cards.md`.
   - Project Scout only: use `skill-references/project-scout.md`.

2. **Read the target JD when present**
   - Use `skill-references/jd-analysis.md`.
   - Detect role type: RAG, Agent, Agentic RL, post-training, pretraining, LLM app, LLM algorithm, search/ranking, AIGC, multimodal, backend AI, infra, or mixed.
   - Load the matching role file under `skill-references/roles/` when relevant.

3. **Audit the materials folder when present**
   - Use `skill-references/materials-audit.md`.
   - Extract projects, claims, evidence, missing evidence, and unclear ownership.

4. **Set truth boundaries**
   - Use `skill-references/truth-boundary.md`.
   - Classify content as `可以写`, `谨慎写`, `补证据后写`, `不能写`, or `无法判断`.

5. **Build the evidence contract**
   - Use `skill-references/evidence-contract.md`.
   - Every strong claim needs evidence, risk, safe wording, and interview proof.

6. **Generate polished / targeted resume**
   - Use `skill-references/resume-polish.md` for line-level polish.
   - Use `skill-references/resume-tailoring.md`.
   - Produce conservative, standard, and stronger-after-evidence bullets.
   - Generate a targeted full resume draft when enough information exists.
   - If the user wants a PDF-ready resume, use `templates/resume-latex/bill-ryan-elegant-zh_CN/resume-zh_CN.tex` as the LaTeX base.

7. **Generate interview grilling**
   - Use `skill-references/interview-grilling.md`.
   - Ask interviewer-style questions based on JD gaps and resume claims.

8. **Generate answer cards**
   - Use `skill-references/answer-cards.md`.
   - For high-risk questions, produce dangerous / passable / strong answers.

9. **Create upgrade plan**
   - Use `skill-references/upgrade-plan.md`.
   - Split into half-day, 1-day, 3-day, and 1-week evidence upgrades.

10. **Optional Project Scout**
   - Use `skill-references/project-scout.md` when the user's evidence is weak or they ask for projects to learn.
   - Recommend projects only as learning/reproduction/modification opportunities, not as fake experience.

11. **Assemble final pack**
   - Use `templates/final-pack.md`.

## Output Files

When writing files, prefer this structure:

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

If the user wants only an answer in chat, still follow the same section order.

## Fit Verdict

Always give one:

```text
strong fit
weak fit
risky fit
not recommended
```

Explain the verdict with:

- JD must-haves.
- User evidence.
- Gaps.
- Highest interview risk.
- Fastest useful upgrade.

## Non-Negotiables

- Never invent internships, production status, metrics, user scale, model training, ranking gains, or ownership.
- Do not write "主导" when evidence only supports "参与".
- Do not write "上线" when evidence only supports demo, local run, or internal trial.
- Do not write open-source learning as work experience unless the user actually reproduced, modified, and documented it.
- If materials are insufficient, ask questions or produce a conservative report instead of polished fiction.
