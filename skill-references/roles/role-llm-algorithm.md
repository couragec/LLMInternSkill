# Role: LLM Algorithm

Use for JD keywords such as Transformer, pretraining, SFT, LoRA, DPO, RLHF, inference, alignment, model evaluation, distillation, MoE, long context, and LLM research.

For specialized frontier-training JDs, also read:

- `role-pretraining.md` for pretraining / mid-training / data engine / distributed training.
- `role-posttraining.md` for SFT / DPO / RLHF / GRPO / reward / verifier / alignment.
- `role-agentic-rl.md` for RL over tool-use, long-horizon Agent tasks, trajectory data, and verifier/reward design.

## What Big Companies Care About

- Transformer basics: attention, RoPE, normalization, KV cache.
- Training/fine-tuning pipeline: data, tokenizer, objective, optimizer, schedule.
- SFT / LoRA / DPO / RLHF basics and tradeoffs.
- Evaluation: benchmark, held-out set, ablation, baseline.
- Code ability: can implement and debug training/inference, not only call APIs.
- Research judgment: failure analysis and hypothesis iteration.

## Toy Signals

- Says "trained LLM" but only called API.
- No dataset, config, or training logs.
- No baseline or metric.
- Cannot explain loss, tokenizer, attention, or evaluation.

## Upgrade Actions

Half day:

- Read model structure and training script.
- Write pipeline notes.
- Run inference/eval on a tiny model.

1 day:

- Reproduce a small SFT or LoRA run.
- Save config, logs, sample outputs.

3 days:

- Compare two settings and write a short report.
- Add eval set and error analysis.

1 week:

- Build a reproducible mini LLM experiment repo with README, scripts, logs, and analysis.

## Safe Resume Bullets

Conservative:

```text
复现小参数 LLM 的训练与推理流程，梳理 tokenizer、Transformer 结构、SFT 数据格式和评测脚本，形成从数据到模型输出的端到端理解笔记。
```

Standard:

```text
基于小规模数据完成 LoRA/SFT 复现实验，记录训练配置、loss 曲线、样例输出和错误类型，对比不同数据或超参设置对生成质量的影响。
```

## High-Pressure Questions

1. Attention 的复杂度是什么？
2. RoPE 为什么能外推？
3. SFT 和 DPO 解决的问题有什么区别？
4. LoRA 为什么省显存？
5. 怎么判断模型真的变好？
6. 训练 loss 降低但效果差怎么办？
7. tokenizer 会影响什么？
8. KV cache 的作用是什么？
