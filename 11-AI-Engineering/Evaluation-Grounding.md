# Evaluation & Grounding

## Why evaluation
“Looks good” is not an engineering metric.

Build representative test sets and measure task-specific outcomes: factual support, retrieval quality, schema validity, task completion, safety, latency and cost.

## Layers
1. deterministic checks where possible;
2. human rubric evaluation;
3. model-based graders with calibration/spot checks;
4. production feedback/telemetry.

## Grounding
Require answers to rely on supplied/retrieved evidence when the use case needs factual traceability. Citations do not prove correctness if retrieval itself is wrong.

## Regression
Prompt/model/retrieval changes can alter behavior. Maintain eval suites like software regression tests.
