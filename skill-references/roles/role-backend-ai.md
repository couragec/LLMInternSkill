# Role: AI Backend / LLM Platform Engineering

Use for backend roles involving LLM APIs, model serving, queues, storage, observability, deployment, latency, cost, and reliability.

## What Big Companies Care About

- API design and data flow.
- Async tasks, queues, retries, idempotency.
- Model service integration and fallback.
- Observability: logs, metrics, tracing.
- Cost and latency control.
- Permissions and security.

## Toy Signals

- Only calls model API from a script.
- No backend interface.
- No retry/fallback.
- No logs or metrics.
- Cannot explain failure handling.

## Upgrade Actions

Half day:

- Draw service flow.
- Add API contract and error codes.

1 day:

- Add structured logs and retry.
- Add request/response examples.

3 days:

- Add queue, timeout, fallback, and basic tests.
- Record latency/cost metrics.

1 week:

- Build a reproducible service demo with observability and deployment docs.

## Safe Resume Bullets

```text
参与 AI 功能后端接口联调，补充请求参数校验、错误码、结构化日志和超时重试逻辑，提升 LLM 调用链路的问题定位能力。
```

## High-Pressure Questions

1. LLM 接口超时怎么办？
2. 如何保证请求幂等？
3. 怎么做降级和 fallback？
4. 如何监控 token 成本？
5. 日志里记录什么，不能记录什么？
