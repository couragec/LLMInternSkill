# Role: LLM Application Engineering

Use for LLM app, AI product engineering, prompt engineering, model API integration, evaluation, quality iteration, and backend integration.

## What Big Companies Care About

- Turning LLM output into a reliable product flow.
- Structured output, schema validation, retry, fallback.
- Prompt/version management and bad-case regression.
- Evaluation and human review.
- Latency, cost, observability, safety.
- Backend integration and data flow.

## Toy Signals

- Only "prompt optimization".
- No eval cases.
- No output validation.
- No logs.
- No product workflow.

## Upgrade Actions

Half day:

- Collect 20 bad cases.
- Add prompt version notes.
- Define output schema.

1 day:

- Add JSON schema validation and retry.
- Add latency/token logging.
- Build fixed eval set.

3 days:

- Add comparison report across prompts/models.
- Add human review status.

1 week:

- Build a small production-like demo with monitoring, fallback, and documentation.

## Safe Resume Bullets

Conservative:

```text
参与 LLM 应用原型开发，负责 Prompt 模板维护、输出样例整理和 bad case 分类，分析幻觉、格式不稳定和字段缺失等问题。
```

Standard:

```text
为 LLM 应用链路补充结构化输出校验、失败重试和版本化评估样例，基于固定 case 对比不同 Prompt / 模型配置的输出稳定性。
```

## High-Pressure Questions

1. 你怎么证明 prompt 改动有效？
2. JSON 输出缺字段怎么办？
3. 模型幻觉怎么处理？
4. token 成本和延迟怎么控制？
5. 人工复核放在哪？
6. prompt 版本怎么管理？
