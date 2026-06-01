# Project Scout Example: MiniMind-Style LLM Learning

Use this when the candidate lacks LLM algorithm evidence and wants a small open-source project to learn, reproduce, and modify.

## Candidate Project

```text
repo: https://github.com/jingyaogong/minimind
role fit: LLM algorithm basics, from-scratch learning, training/inference pipeline
use case: personal learning project, not internship/work experience
```

## Why It Fits

- It is closer to "understand the LLM pipeline" than prompt-only API projects.
- It can support interview discussion around tokenizer, Transformer blocks, SFT-style data, training scripts, inference, and evaluation.
- It is suitable for a student who needs concrete evidence for "熟悉 LLM 相关算法和技术".

## Why Not / Risk

- It does not directly prove search/ranking ability.
- Running a small model is not the same as training an industrial LLM.
- If the user only reads the README, it cannot be written as project experience.
- Resume claims must stay small unless there are configs, logs, output samples, and a personal modification.

## Minimum Run Path

```text
1. Clone the repo.
2. Read model definition, tokenizer/data pipeline, training script, and inference script.
3. Run the smallest inference or training path the hardware allows.
4. Save config, command, log, sample outputs, and failure cases.
5. Write a short report: what changed, what failed, what was learned.
```

## Modification Ideas

Half day:

- Draw the model/data/training/inference pipeline.
- Add comments to the most important modules.
- Collect 10 output examples and failure cases.

1 day:

- Run a tiny training or SFT path.
- Save loss curve or logs.
- Compare two prompts or decoding settings.

3 days:

- Add a small evaluation script.
- Compare two hyperparameter/data settings.
- Write an ablation note.

1 week:

- Publish a reproducible personal fork or report with commands, logs, outputs, and a clear limitation section.

## Evidence To Collect

| Evidence | Why It Matters |
| --- | --- |
| run command | proves reproducibility |
| config | proves the experiment setup |
| log / loss | supports training or fine-tuning claims |
| output samples | enables error analysis |
| code diff | proves personal modification |
| short report | supports interview explanation |

## Resume-Safe Claims After Completion

Conservative:

```text
复现小参数 LLM 的训练与推理流程，梳理 tokenizer、Transformer 模块、训练脚本和推理链路，形成可复现命令、运行日志和样例输出分析。
```

Standard after modification:

```text
基于 MiniMind 类小型 LLM 项目完成本地复现与小规模实验，记录训练配置、loss 日志和生成 bad case，对比不同数据/解码设置对输出质量的影响。
```

Do not write:

```text
训练工业级大模型 / 主导大模型研发 / 显著提升模型效果
```

## Interview Grilling

1. 这个项目里 tokenizer 怎么影响训练和生成？
2. Transformer block 里 attention、MLP、norm 的顺序是什么？
3. 你实际跑了哪个命令？用了什么数据和配置？
4. loss 下降是否一定代表效果变好？
5. 你改了哪一行代码？为什么改？
6. 你怎么评估输出质量？
7. 这个项目和工业 LLM 训练差在哪里？
