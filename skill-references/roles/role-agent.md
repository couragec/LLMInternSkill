# Role: Agent / Tool Use

Use for JD keywords such as Agent, tool calling, workflow automation, planner, function calling, MCP, multi-step task, memory, verifier, and human review.

## What Big Companies Care About

- Agent is not a chatbot. It should choose tools, pass parameters, verify outputs, handle failures, and respect permissions.
- Tool schema, parameter validation, timeout, retry, fallback.
- State/session management and cross-user isolation.
- Trace logs for each tool call.
- Human-in-the-loop for risky actions.
- Evaluation: task success rate, tool-call success, invalid-call rate, latency, cost.

## Toy Signals

- Only one prompt.
- No real tools.
- No schema or logs.
- No state boundary.
- No failure cases.
- Claims "autonomous" but actually manual.

## Upgrade Actions

Half day:

- List tools, inputs, outputs, and failure types.
- Add 10 failure examples.

1 day:

- Add JSON schema validation.
- Add trace_id logs.
- Add retry/fallback for one tool.

3 days:

- Build a small evaluation set for tasks.
- Add verifier or human review state.

1 week:

- Add task dashboard, permissions, and cost/latency tracking.

## Safe Resume Bullets

Conservative:

```text
参与内部业务 Agent 原型开发，整理工具调用样例、Prompt 模板和模型输出失败案例，梳理字段缺失、参数错误和工具超时等工程化风险。
```

Standard:

```text
为 Agent 工具调用链路补充参数校验、trace 日志和失败重试机制，基于 bad case 回归样例分析字段缺失、工具超时与多轮状态混乱问题。
```

## High-Pressure Questions

1. Agent 和 chatbot 的区别是什么？
2. 你的工具 schema 怎么设计？
3. 参数错了怎么办？
4. 工具超时怎么办？
5. 多轮状态怎么管理？
6. 有没有 human review？
7. 怎么评估任务成功率？
8. 权限怎么控制？
