# Example: Post-Training / Agentic RL Case

This example shows how to safely write a frontier-training project without pretending it is industrial-scale model training.

## Target JD Summary

```text
Top Seed / 大模型应用算法 / Agentic RL / post-training:
- complex reasoning
- autonomous Agent
- scalable supervision
- data synthesis
- verifier / reward
- rigorous quantitative evaluation
```

## Candidate Evidence

```text
- Read papers and notes on RLHF, DPO, GRPO, and verifier-guided reasoning.
- Built 20 long-horizon tool-use tasks for a research assistant Agent demo.
- Saved tool-call traces for 12 tasks.
- Implemented a rule-based verifier for citation correctness and task completion.
- Compared prompt-only vs verifier-guided retry on 20 tasks.
- No RL training loop yet.
- No reward model training.
- No large-scale rollout generation.
```

## Truth Boundary

| Claim | Status | Safe Wording |
| --- | --- | --- |
| Agentic RL 训练 | 不能写 | Agent 任务评估与 verifier-guided retry |
| Post-training 经验 | 谨慎写 | 后训练方法学习与小规模 verifier 设计 |
| 提升 Agent 成功率 | 补证据后写 | 对比 prompt-only 与 verifier-guided retry 的任务完成情况 |
| 大规模数据合成 | 不能写 | 手工构造 20 条长链路任务样例 |

## Resume-Safe Bullets

Conservative:

```text
围绕 research assistant Agent 场景构造 20 条长链路 tool-use 任务，记录 prompt、工具调用、观测结果和最终回答，分析参数错误、引用缺失和无效终止等失败轨迹。
```

Standard after metric table:

```text
实现 citation correctness 与 task completion 的规则 verifier，对比 prompt-only 与 verifier-guided retry 在 20 条任务上的完成情况，沉淀任务成功判定、失败类型和后训练改进方向。
```

Stronger after evidence:

```text
构建小规模 Agent 任务评估与 verifier 数据闭环，围绕 tool-call trajectory、过程判定和最终结果质量分析 reward/verifier 设计风险，为 Agentic RL / post-training 方案提供可复现实验基础。
```

## Interview Grilling

1. 为什么这不是完整 Agentic RL？
2. verifier 的误判 case 有哪些？
3. retry 带来的成功率提升是否只是多采样？
4. 你的 trajectory 数据字段是什么？
5. 如果要进入 RL 训练，你下一步缺什么？
6. GRPO/PPO/DPO 分别适合什么？
7. 如何避免 reward hacking？
