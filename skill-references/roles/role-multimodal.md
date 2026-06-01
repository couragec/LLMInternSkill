# Role: Multimodal / VLM

Use for VLM, OCR, image/video understanding, multimodal retrieval, document understanding, and visual-language tasks.

## What Big Companies Care About

- Input modalities and preprocessing.
- Visual encoder / text encoder / cross-modal alignment.
- OCR, layout, table, chart, and document structure.
- Evaluation set and error types.
- Latency, resolution, cost, and deployment constraints.

## Toy Signals

- Only sends image to model API.
- No dataset or eval.
- Cannot explain OCR/layout failures.
- No modality-specific bad cases.

## Upgrade Actions

Half day:

- Collect 10 visual bad cases.
- Categorize OCR/layout/table/chart failures.

1 day:

- Build small eval set and compare model outputs.
- Record latency and cost.

3 days:

- Add preprocessing or post-processing.
- Produce report by error type.

1 week:

- Build a multimodal demo with evidence traces and manual review.

## Safe Resume Bullet

```text
围绕多模态理解场景整理图文输入、OCR/Layout 失败样例和人工评估口径，对比不同模型在表格、截图和长图场景下的输出稳定性。
```

## High-Pressure Questions

1. OCR 错误怎么影响下游？
2. 表格和图表怎么评估？
3. 分辨率和延迟怎么取舍？
4. VLM 输出怎么验证？
