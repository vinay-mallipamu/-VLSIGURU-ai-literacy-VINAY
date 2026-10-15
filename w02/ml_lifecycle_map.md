# ML Foundations Map — Lifecycle

```mermaid
flowchart TD
    A["1. Define the problem<br/>Goal, constraints, success criteria"]
    B["2. Understand data<br/>Samples, features, labels, quality"]
    C["3. Select approach<br/>Rule-based or ML; paradigm and task"]
    D["4. Prepare and train<br/>Clean, split data, learn parameters"]
    E["5. Evaluate<br/>Validation/test sets, metrics, baseline"]
    F["6. Use model<br/>Inference on new input"]
    G["7. Monitor and improve<br/>Failures, bias, drift, human oversight"]

    A --> B --> C --> D --> E --> F --> G
    G -. "If problems appear, revisit earlier steps" .-> B
```

## Where the concepts fit

- **Learning paradigms:** supervised, unsupervised, reinforcement and self-supervised.
- **Task types:** classification, regression, clustering, anomaly detection, dimensionality reduction and recommendation/ranking.
- **Possible failure points:** incorrect labels, unrepresentative data, data leakage, overfitting and changing real-world data.
- **Semiconductor application:** early estimation of timing slack from historical Physical Design runs. This is an estimate to investigate, not final sign-off.
