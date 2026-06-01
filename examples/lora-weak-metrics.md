# Example: LoRA Experiment With Weak Metrics

Use this example when the candidate has done a small LoRA/SFT experiment but lacks strong evaluation evidence.

## Input

Target role:

```text
LLM 算法 / 大模型应用算法实习生
```

Original resume claim:

```text
使用 LoRA 微调大模型，显著提升模型生成质量。
```

Actual evidence:

```text
- Ran one LoRA experiment on a small instruction dataset.
- Has training command, config, and loss log.
- Has 20 before/after generated samples.
- No held-out eval set.
- No human preference rubric.
- No baseline besides the original model outputs.
- No ablation.
```

## Diagnosis

| Claim | Status | Reason |
| --- | --- | --- |
| 使用 LoRA 微调模型 | 可以写 | Has command, config, and training log. |
| 显著提升模型生成质量 | 补证据后写 | Needs eval set, rubric, baseline, or preference data. |
| 大模型训练经验 | 谨慎写 | This is small-scale fine-tuning reproduction, not industrial LLM training. |

## Safe Resume Rewrite

```text
基于小规模指令数据完成 LoRA 微调复现实验，记录训练配置、loss 日志和 20 组生成样例，分析回答冗长、格式不稳定和事实错误等 bad case。
```

## Stronger After Evidence

```text
基于固定 held-out 样例集对比 base model 与 LoRA checkpoint 的生成质量，按照 instruction following、format validity 和 factuality 进行人工评估，并结合 loss 曲线与 bad case 分析微调收益和局限。
```

Required evidence:

```text
held-out eval set, rubric, before/after table, baseline, sample outputs, failure analysis
```

## Interview Grilling

1. LoRA 为什么比全参数微调省显存？
2. 你的 rank、alpha、learning rate 怎么选？
3. loss 降低为什么不一定代表生成质量变好？
4. 你怎么构造 held-out eval set？
5. 你的数据格式是什么？有没有污染评测样例？
6. 哪些 case 变好了，哪些 case 变差了？
7. 这个实验和工业级 LLM 训练差在哪里？

