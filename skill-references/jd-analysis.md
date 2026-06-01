# JD Analysis

Goal: turn the target JD into concrete interview and resume requirements.

## Steps

1. Extract explicit requirements.
2. Infer hidden interview tests.
3. Detect role type.
4. Map requirements to user evidence.
5. Produce a fit verdict.

## Role Type Detection

Use the strongest matching type:

- `rag`: retrieval, chunking, rerank, citation, evals, hallucination.
- `agent`: tool calling, workflow, planner, memory/session, verifier, human review.
- `agentic-rl`: Agentic RL, verifier, reward, trajectory, GRPO, PPO, tool-use RL, long-horizon tasks.
- `posttraining`: SFT, DPO, RLHF, RLAIF, GRPO, reward model, preference alignment, instruction tuning.
- `pretraining`: pretraining, mid-training, data engine, tokenizer, scaling, distributed training, contamination.
- `llm-app`: LLM product engineering, prompt, API, eval, backend integration.
- `llm-algorithm`: Transformer, training, fine-tuning, alignment, inference, evaluation.
- `search-ranking`: recall, rough rank, fine rank, rerank, query-doc relevance, doc understanding.
- `aigc`: image/video/text generation, content workflow, safety, latency, product integration.
- `multimodal`: VLM, OCR, image/video understanding, cross-modal retrieval.
- `backend-ai`: APIs, queues, storage, observability, deployment, cost, latency.
- `mixed`: multiple types are equally important.

## Fit Verdict

Use:

```text
strong fit
weak fit
risky fit
not recommended
```

Judgment:

- `strong fit`: clear evidence for must-haves and can answer deep questions.
- `weak fit`: some evidence but missing depth or metrics.
- `risky fit`: resume can be written, but interview likely exposes gaps.
- `not recommended`: core JD asks for things the user has no evidence for.

## Output

```markdown
## JD Mainline

## Role Type

## Must-Haves

## Hidden Interview Tests

## User Evidence Mapping

## Fit Verdict

## Strategy
```
