# Frontier Training JD Notes

These notes summarize current public recruiting signals for optional LLMInternSkill role references. Use them as inspiration for role detection and examples, not as a replacement for reading the user's target JD.

Checked on 2026-06-01.

## Sources

Official / higher-confidence:

- ByteDance campus job detail: `https://jobs.bytedance.com/campus/position/7483736511101602056/detail`
- ByteDance campus frontier technology page: `https://jobs.bytedance.com/campus/page-6272Gc`
- Tencent Careers query API, keyword `混元`: `https://careers.tencent.com/tencentcareer/api/post/Query?keyword=%E6%B7%B7%E5%85%83&pageIndex=1&pageSize=10&language=zh-cn&area=cn`
- Tencent Careers query API, keyword `大模型`: `https://careers.tencent.com/tencentcareer/api/post/Query?keyword=%E5%A4%A7%E6%A8%A1%E5%9E%8B&pageIndex=1&pageSize=10&language=zh-cn&area=cn`

Lower-confidence market signals:

- BOSS pages often redirect to security checks in a browser. Search-result snippets still show market keywords such as Agent, RLHF, post-training, Agentic RL, pre train / mid train / post training, but do not treat them as authoritative JD text.
- Third-party reposts may be useful for vocabulary discovery, but verify against official careers pages when possible.

## Observed Signals

### ByteDance / Seed-Style Research

The official Top Seed Doubao LLM application algorithm internship emphasizes:

- complex real-world tasks
- scalable general methods
- complex reasoning
- multimodal ability
- autonomous Agent
- scalable supervision
- large-scale data synthesis
- high-value applications such as Agent systems, professional consulting, research collaboration, deep insight, personalized education
- rigorous quantitative evaluation
- ML / NLP / RL foundation
- top conference research signal as a plus

Skill implication:

```text
When JD mentions Top Seed / complex reasoning / autonomous Agent / scalable supervision,
load role-agentic-rl.md, role-posttraining.md, role-llm-algorithm.md, and role-agent.md as needed.
```

### Tencent / Hunyuan-Style Agent Engineering

Tencent Careers search for `混元` surfaced an official Hunyuan Agent Harness Engineer role with signals such as:

- Agent execution tracing and observability
- automated eval pipeline
- A/B testing
- regression detection
- Agent debugging tools
- labeling, SBS evaluation, and data pipelines
- close collaboration with AI research teams
- engineering latest model and Agent capabilities into platforms

Skill implication:

```text
When JD mentions harness, observability, eval pipeline, regression detection, SBS evaluation,
load role-agent.md, role-agentic-rl.md, role-backend-ai.md, and optionally role-posttraining.md.
```

### Post-Training / Alignment

Common signals across public recruiting snippets:

- SFT, RLHF, RLAIF, DPO, PPO, GRPO
- reward model / verifier
- preference alignment
- instruction data construction
- data synthesis and filtering
- model evaluation and safety
- reasoning improvement

Skill implication:

```text
Do not let users write "post-training" unless they can show data, config, logs, eval, before/after samples, and failure analysis.
```

### Pretraining / Mid-Training

Common signals:

- data engine and data quality
- pre train / mid train / continued pretraining
- tokenizer and data mixture
- distributed training and checkpointing
- loss / perplexity / held-out eval
- contamination checks

Skill implication:

```text
Most students should write "复现小参数训练流程" or "continued-pretraining experiment",
not "训练大模型", unless they have real training evidence.
```

## Resume Boundary

Allowed wording for weak evidence:

```text
学习并复现 tiny LLM 训练/后训练流程
整理 post-training 数据格式与评估样例
构建 Agent 任务评估集与 tool-call trace
分析 reward/verifier 设计和失败轨迹
```

Do not write without evidence:

```text
主导大模型 post-training
负责预训练基座模型
显著提升推理能力
实现 Agentic RL 训练闭环
上线企业级 Agent 平台
```
