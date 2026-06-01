# Role: AIGC / Content Generation

Use for image/video/text generation, content workflow, creative tools, diffusion, multimodal generation, and AI product roles.

## What Big Companies Care About

- Generation pipeline: input, prompt/control, model, post-processing, review, output.
- Quality metrics and human preference.
- Safety, copyright, harmful content, and moderation.
- Latency and cost.
- Product workflow integration.
- Bad cases: style drift, artifacts, hallucinated text, inconsistent identity.

## Toy Signals

- Only calls a generation API.
- No quality criteria.
- No review/moderation.
- No product workflow.
- No failure analysis.

## Upgrade Actions

Half day:

- Collect generation bad cases.
- Define quality rubric.

1 day:

- Compare prompts/model settings.
- Add output review checklist.

3 days:

- Build a small generation workflow with logging and manual review.
- Produce before/after examples.

1 week:

- Add batch evaluation, safety checks, and a simple UI/demo.

## Safe Resume Bullets

```text
参与 AIGC 内容生成流程原型开发，整理生成失败、风格不一致和内容安全 bad case，基于固定样例对比 Prompt 与参数配置对输出质量的影响。
```

## High-Pressure Questions

1. 生成质量怎么评估？
2. 如何处理内容安全？
3. 失败样例有哪些？
4. 用户编辑链路怎么接？
5. 延迟和成本怎么控制？
