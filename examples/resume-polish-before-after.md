# Example: Resume Polish Before / After

Use this example when the user only provides resume lines and asks for polishing.

## Input

Target role:

```text
LLM / RAG / Agent 应用工程实习生
```

Original resume lines:

```text
1. 熟悉大模型和 RAG，优化知识库问答效果。
2. 搭建企业级智能问答系统，提升用户检索效率。
3. 实现 Agent 自动化办公流程。
4. 训练大模型并提升回答质量。
```

Known evidence:

```text
- Local RAG demo with 20 PDF docs.
- Implemented document chunking, FAISS retrieval, and prompt template.
- Has a demo screenshot.
- No eval set, no citation metric, no production release.
- Tool-calling demo has two tools, but no schema validation or retry.
- No model training logs or checkpoint.
```

## Output

## Resume Polish Verdict

```text
Overall: 可润色，但必须降级强 claim。
Best usable line: RAG demo 的文档切分、检索和 bad-case 分析。
Most risky line: 训练大模型并提升回答质量。
Fastest evidence upgrade: 补 30 条 query-answer-evidence 样例和 retrieved chunk 日志。
```

## Before / After

| Original | Clean | Technical | JD-Targeted | Status | Interview Risk |
| --- | --- | --- | --- | --- | --- |
| 熟悉大模型和 RAG，优化知识库问答效果 | 参与 RAG 问答 demo 开发，整理问答样例和回答失败问题 | 完成文档切分、FAISS 向量检索和 Prompt 模板配置，记录召回错误、引用缺失和无依据回答等 bad case | 围绕企业文档问答场景搭建 RAG demo，沉淀 query-answer 样例和召回/引用失败分析，为后续评估集建设提供依据 | 谨慎润色 | 如果问“效果提升多少”，当前没有指标 |
| 搭建企业级智能问答系统，提升用户检索效率 | 搭建企业文档问答原型 demo | 基于 20 份 PDF 文档完成本地知识库问答 demo，支持向量检索和答案生成 | 完成企业文档问答 demo 的 ingestion、chunking、retrieval 和回答生成链路，梳理检索效率和回答可靠性问题 | 建议降级 | “企业级”“提升效率”缺上线和指标 |
| 实现 Agent 自动化办公流程 | 实现两类工具调用原型 | 实现日程查询和报销状态查询工具调用，整理参数缺失和调用失败样例 | 参与 Agent 工具调用原型开发，梳理 tool schema、参数缺失和失败处理需求 | 谨慎润色 | 如果问 state、retry、permission，当前证据不足 |
| 训练大模型并提升回答质量 | 学习并复现小模型训练流程 | 当前没有训练证据，不建议写训练 claim | 可改为“阅读并整理 Transformer、LoRA、RAG 评估笔记” | 建议删除/降级 | 没有 dataset/config/log/checkpoint |

## Final Polished Version

```text
- 完成企业文档问答 demo 的文档切分、FAISS 向量检索和 Prompt 模板配置，记录召回错误、引用缺失和无依据回答等 bad case。
- 实现日程查询和报销状态查询两类工具调用原型，整理工具参数缺失、调用失败和后续 schema 校验需求。
- 阅读并整理 Transformer、LoRA 与 RAG 评估相关笔记，结合 demo 分析 LLM 应用中回答可靠性和检索质量问题。
```

## Optional English Version

```text
- Built a local enterprise document QA demo with chunking, FAISS retrieval, and prompt templates; analyzed retrieval misses, missing citations, and unsupported answers.
- Implemented two tool-calling prototypes for calendar lookup and reimbursement status queries; documented missing-parameter and tool-call failure cases.
- Studied Transformer, LoRA, and RAG evaluation notes, connecting them to answer reliability and retrieval-quality issues in the demo.
```

## Evidence Upgrade List

| Task | Time | Evidence Produced | Stronger Claim Unlocked |
| --- | --- | --- | --- |
| Add retrieved chunk logs | Half day | logs + screenshots | RAG traceability |
| Build 30 query-answer-evidence samples | 1 day | eval set | citation / answer relevance discussion |
| Add tool schema validation and retry | 3 days | code diff + traces | Agent reliability work |
| Run a tiny LoRA or SFT reproduction | 3 days to 1 week | config + logs + outputs | small-model training reproduction |

