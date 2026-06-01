# Role: Pretraining / Foundation Model Training

Use for JD keywords such as pretraining, mid-training, foundation model, data engine, tokenizer, scaling law, distributed training, model architecture, data mixture, contamination, evaluation, checkpoint, and large-scale training.

## What Big Companies Care About

- Data engine: collection, filtering, deduplication, quality scoring, domain mix, contamination checks.
- Tokenizer and data format: tokenization efficiency, multilingual/code/math support, special tokens.
- Model/training basics: Transformer, attention, RoPE, normalization, optimizer, LR schedule, loss.
- Distributed training: data/model/pipeline parallelism, checkpointing, fault tolerance, throughput.
- Evaluation: perplexity, downstream benchmarks, held-out sets, contamination, regression.
- Compute awareness: GPU memory, batch size, sequence length, MFU/throughput, cost.

## Toy Signals

- Says "pretrained a model" but only ran inference or API calls.
- No data pipeline, tokenizer, config, training log, checkpoint, or eval.
- Cannot explain attention, RoPE, optimizer schedule, or distributed training basics.
- No contamination or data quality awareness.

## Evidence To Collect

- Data pipeline notes: sources, filters, dedup, quality scores, split.
- Training script/config and run command.
- Loss curve, throughput, GPU memory, checkpoint.
- Eval script and held-out results.
- Error analysis and limitations.

## Upgrade Actions

Half day:

- Read a small LLM pretraining repo and draw the data -> tokenizer -> model -> loss -> eval flow.
- Run inference/eval on a tiny model.

1 day:

- Run a tiny pretraining or continued-pretraining experiment.
- Save config, logs, checkpoint, sample outputs.

3 days:

- Compare two data mixes or tokenizer/settings on a tiny setup.
- Add a simple held-out eval and contamination note.

1 week:

- Build a reproducible mini-pretraining report with scripts, config, logs, evals, and limitations.

## Safe Resume Bullets

Conservative:

```text
复现小参数 LLM 的预训练数据处理、tokenizer、Transformer 训练与评测流程，记录训练配置、loss 日志、样例输出和局限分析，形成端到端训练链路理解。
```

Standard after evidence:

```text
基于小规模语料完成 tiny LLM continued-pretraining 实验，对比不同数据过滤或数据配比设置下的 loss、held-out perplexity 和生成样例，沉淀可复现实验报告。
```

## High-Pressure Questions

1. 预训练、mid-training、SFT/post-training 的区别是什么？
2. tokenizer 会影响哪些能力和成本？
3. RoPE、KV cache、attention 复杂度怎么解释？
4. 数据去重和污染检查为什么重要？
5. loss/perplexity 和下游能力是什么关系？
6. 分布式训练常见瓶颈是什么？
7. 如何判断 tiny pretraining 实验能写到什么强度？
