# Example Input: Agent + RAG Internal Assistant

This example targets LLM app / RAG / Agent internship roles.

## Target Role Summary

```text
LLM 应用工程实习生：负责企业知识库问答、Agent 工具调用、结构化输出、评估与 bad case 分析。
```

## Materials Summary

### Project: Internal QA Assistant Demo

- Built a local demo that answers questions from 20 internal policy documents.
- Uses text chunking, embedding retrieval, and one LLM API.
- Returns answer and a source document name, but not exact page/chunk citation.
- Has a small web UI.
- Has 25 manually written questions, but no expected answers.
- Logs only final answer, not retrieved chunks.

### Project: Tool-Calling Assistant

- Calls two tools: calendar lookup and reimbursement status query.
- Tool schema exists in Python dict form.
- No timeout/retry/fallback.
- No permission model.
- Has 8 tool-call traces saved as screenshots.

## Current Resume Claims

- "搭建企业级 RAG 智能问答系统，提升知识检索效率。"
- "实现 Agent 自动化办公流程。"
- "优化 Prompt，提升回答准确率。"

## Evidence Risks

- "企业级" sounds too strong for a local demo.
- "提升效率/准确率" has no metric.
- "Agent 自动化" is risky because there are only two tools and no verifier or state handling.
