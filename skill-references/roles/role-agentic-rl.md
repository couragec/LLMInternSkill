# Role: Agentic RL / RL For Agents

Use for JD keywords such as Agentic RL, agent reinforcement learning, tool-use RL, verifier, reward model, GRPO, PPO, RLHF, RLAIF, process reward, outcome reward, trajectory data, long-horizon tasks, and autonomous agent evaluation.

## What Big Companies Care About

- Agentic RL is about training or optimizing policies over multi-step tasks, not just prompting an Agent.
- Environment/task design: actions, observations, tool calls, termination, success criteria.
- Trajectory data: collection, filtering, labeling, replay, bad trajectories.
- Reward/verifier design: outcome reward, process reward, rule-based verifier, model-based judge, safety constraints.
- RL algorithms and tradeoffs: PPO, GRPO, DPO/RLHF/RLAIF where relevant.
- Evaluation: task success rate, tool-call success, hallucination/failure rate, reward hacking, generalization.
- Engineering: rollout generation, distributed training, logging, reproducibility, cost.

## Toy Signals

- Calls an LLM with tools but has no environment, reward, or trajectories.
- Says RLHF but only wrote prompts.
- Uses "Agentic RL" as a buzzword without verifier/eval evidence.
- No success metric, no failure taxonomy, no rollout logs.

## Evidence To Collect

- Task suite with input, tools, expected outcome, and success criteria.
- Rollout traces: prompt, tool call, observation, final answer, reward/verifier result.
- Reward/verifier definition and failure cases.
- Baseline: prompt-only agent, heuristic policy, supervised fine-tuned model, or prior checkpoint.
- Metric report: success rate, invalid tool-call rate, cost/latency, safety failures.
- Notes on reward hacking or verifier false positives.

## Upgrade Actions

Half day:

- Define 10 long-horizon agent tasks and success criteria.
- Save complete tool-call traces.

1 day:

- Build a rule-based verifier for one task family.
- Compare prompt-only vs verifier-guided retry.

3 days:

- Add rollout logs and a small task success evaluation.
- Analyze reward hacking and failed trajectories.

1 week:

- Reproduce a small RL/post-training or agent-eval pipeline; publish configs, logs, task suite, and report.

## Safe Resume Bullets

Conservative:

```text
围绕 Agent 长链路任务整理 tool-call 轨迹、成功判定和失败类型，分析参数错误、工具超时、状态丢失和无效终止等问题，为后续 verifier / reward 设计沉淀任务样例。
```

Standard after evidence:

```text
构建小规模 Agent 任务评估集与规则 verifier，对比 prompt-only 与 verifier-guided retry 在任务成功率、无效工具调用率和成本上的差异，分析 reward hacking 与失败轨迹。
```

## High-Pressure Questions

1. Agentic RL 和普通 tool-calling Agent 有什么区别？
2. 你的 environment/action/observation/reward 怎么定义？
3. verifier 怎么避免误判和 reward hacking？
4. GRPO/PPO/RLHF/DPO 分别适合什么场景？
5. 你怎么收集和过滤 trajectory？
6. 成功率提升是否来自更好 reward，还是更多 retry？
7. 长链路任务失败怎么归因？
