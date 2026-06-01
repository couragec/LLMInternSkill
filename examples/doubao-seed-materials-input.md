# Example Input: Weak-To-Medium Candidate Materials

This mock candidate is intentionally imperfect. The point is to show how LLMInternSkill avoids fake polishing.

## Folder Summary

```text
materials/
├── target_jd.txt
├── resume.md
├── projects/
│   ├── rag-course-project.md
│   ├── mini-search-demo.md
│   └── llm-notes.md
├── code/
│   └── README.md
├── notes/
│   ├── bad-cases.md
│   └── transformer-notes.md
└── awards/
    └── contests.md
```

## Current Resume Claims

- "熟悉大模型与 RAG，优化知识库问答效果。"
- "完成一个基于向量数据库的企业文档问答系统。"
- "了解搜索排序和推荐算法。"
- "掌握 Python，刷题约 200 题。"

## Actual Evidence

### RAG Course Project

- Built with LangChain, FAISS, and one commercial LLM API.
- Has 15 PDF documents and a demo screenshot.
- Has no eval set, no citation accuracy, no no-answer refusal rule.
- Personal work: ingestion script, chunking config, prompt template, demo UI.
- Unknown: whether rerank was implemented; no logs saved.

### Mini Search Demo

- Local notebook comparing BM25 and embedding retrieval on 30 manually collected query-doc examples.
- Has rough labels: relevant / partially relevant / irrelevant.
- Has no NDCG/MRR table yet.
- Has 12 bad cases about ambiguous query, stale doc, and low-authority content.

### LLM Notes

- Read Transformer, RoPE, LoRA, RAG evaluation notes.
- No training/fine-tuning code.
- No model checkpoint or training log.

### Coding / Algorithm

- Python is strong enough for project scripts.
- C++ evidence is only coursework.
- Contest evidence is weak: school programming contest participation, no major award.

## Missing Evidence

- Ranking metric report.
- Search pipeline explanation.
- DOC quality rubric.
- LLM algorithm experiment beyond notes.
- Reproducible README and run command.
- Clear before/after comparison for RAG or search.
