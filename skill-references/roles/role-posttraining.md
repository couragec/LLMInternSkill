# Role: Post-Training / Alignment

Use for JD keywords such as post-training, SFT, RLHF, RLAIF, DPO, GRPO, PPO, reward model, preference alignment, instruction tuning, data synthesis, verifier, model evaluation, safety alignment, and reasoning improvement.

## What Big Companies Care About

- Data: instruction data, preference pairs, rejection sampling, synthetic data, contamination control.
- Methods: SFT, DPO, RLHF/RLAIF, PPO/GRPO, reward modeling, verifier-guided training.
- Objective and tradeoffs: helpfulness, harmlessness, instruction following, reasoning, factuality, style.
- Evaluation: held-out eval set, win rate, pairwise preference, task accuracy, safety tests, regression.
- Failure analysis: reward hacking, over-optimization, style drift, refusal errors, degraded capabilities.
- Training evidence: config, logs, checkpoints, eval reports, before/after samples.

## Toy Signals

- Says "post-training" but only changed prompts.
- Says "RLHF" without preference data, reward model, or RL loop.
- Says "提升推理能力" without benchmark or error analysis.
- Has training logs but no held-out eval.

## Evidence To Collect

- Dataset card: source, filtering, format, size, split, risks.
- Training config: base model, LoRA/full fine-tune, optimizer, learning rate, epochs, batch size.
- Eval report: baseline vs checkpoint, metrics, sample outputs, bad cases.
- Preference or verifier definition where applicable.
- Safety and regression checks.

## Upgrade Actions

Half day:

- Document data format and create a held-out eval split.
- Save baseline outputs for 20 examples.

1 day:

- Run a tiny SFT/LoRA reproduction with config and logs.
- Build a before/after sample table.

3 days:

- Add DPO or preference-style comparison on a small dataset.
- Add human preference rubric or model-judge prompt with limitations.

1 week:

- Produce a reproducible post-training report with data card, training logs, evals, failure cases, and limitations.

## Safe Resume Bullets

Conservative:

```text
复现小规模 SFT/LoRA 后训练流程，整理指令数据格式、训练配置、loss 日志和生成样例，分析格式不稳定、事实错误和拒答异常等 bad case。
```

Standard after evidence:

```text
基于 held-out 样例集对比 base model 与 LoRA checkpoint 的 instruction following、format validity 和 factuality，结合训练日志与 bad-case 分析评估后训练收益和局限。
```

## High-Pressure Questions

1. SFT、DPO、RLHF/RLAIF、GRPO 的核心差别是什么？
2. 你的训练数据怎么来？有没有污染评测集？
3. reward model 或 verifier 怎么设计？
4. loss 下降为什么不等于模型变好？
5. 怎么评估 helpfulness、factuality、safety？
6. 模型某项能力变好但另一项退化怎么办？
7. 如何识别 reward hacking？
