# AI / ML Mental Map

```mermaid
flowchart TD
    AI["Artificial Intelligence (AI)<br/>Broad field"]
    RB["Rule-based systems<br/>Explicit human rules"]
    ML["Machine Learning (ML)<br/>Learns patterns from data"]
    SUP["Supervised learning<br/>Labelled examples"]
    UNS["Unsupervised learning<br/>Find structure"]
    RL["Reinforcement learning<br/>Actions + rewards"]
    SSL["Self-supervised learning<br/>Targets derived from data"]
    DL["Deep learning<br/>Multi-layer neural networks"]
    GEN["Generative AI<br/>Generates content"]
    LLM["LLMs<br/>Language-focused models"]
    TASK["Task types<br/>Classification, regression,<br/>clustering, anomaly detection,<br/>dimensionality reduction,<br/>recommendation/ranking"]

    AI --> RB
    AI --> ML
    ML --> SUP
    ML --> UNS
    ML --> RL
    ML --> SSL
    ML --> DL
    DL --> GEN
    GEN --> LLM
    ML -. "can address" .-> TASK
```

## Remember

- Learning paradigms describe **how a model learns**.
- Task types describe **what output or problem is required**.
- Generative AI describes systems that generate content; LLMs focus on language. This is a simplified conceptual map, not a strict hierarchy in every case.

## Semiconductor example

**Proposed Physical Design application:** Use historical design-run features to estimate timing slack.

- Learning paradigm: supervised learning, if historical target values are available.
- Task type: regression.
- Output: estimated timing slack.
- Limitation: validate on unseen designs and confirm final timing with the approved EDA flow.
