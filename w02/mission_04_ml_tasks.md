# Mission 4 — Understand ML Task Types

## 1. Task types

| Task type | What it does | Typical output |
|---|---|---|
| Classification | Predicts a category | Pass/Fail, defect/no defect |
| Regression | Predicts a numerical value | Delay in ns, power in mW |
| Clustering | Groups similar observations without given class labels | Groups of similar design runs |
| Anomaly detection | Flags observations that differ unusually from normal patterns | Alert or anomaly score |
| Dimensionality reduction | Represents data with fewer variables while preserving useful structure | A smaller set of dimensions |
| Recommendation / ranking | Orders or suggests candidates | Ranked list of design configurations |

## 2. Six real-world problems

| Problem | Input data | Task type | Expected output |
|---|---|---|---|
| Predict whether a chip run meets timing | Utilisation, cell count, estimated delay, process corner | Classification | Pass or Fail |
| Estimate final delay before a long EDA run finishes | Design features and earlier flow measurements | Regression | Predicted delay |
| Group similar physical-design runs | Congestion, cell count, wirelength and timing measurements | Clustering | Groups of similar runs |
| Find unusual sensor readings in a fab process | Sensor measurements and normal historical patterns | Anomaly detection | Flag or anomaly score |
| Simplify hundreds of correlated design measurements | Large feature vector | Dimensionality reduction | Fewer dimensions |
| Suggest promising design settings to try next | Previous configurations and their PPA outcomes | Recommendation / ranking | Ordered candidate list |

These are illustrative semiconductor use cases, not claims that every use is deployed in every company.

## 3. Task type versus learning paradigm

A **learning paradigm** describes how a model learns: from labelled examples, unlabelled data, or reward feedback. A **task type** describes the output or problem being solved.

For example, predicting timing pass/fail is a classification task and can use supervised learning when labelled examples are available. Clustering is commonly unsupervised. A task type alone does not identify the training method; multiple algorithms may address a similar task.

## Sources
- Google, [What is Machine Learning?](https://developers.google.com/machine-learning/intro-to-ml/what-is-ml)
- Google, [Problem Framing](https://developers.google.com/machine-learning/problem-framing/ml-framing)
