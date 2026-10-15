# Mission 9 — Connect ML to Semiconductor Engineering

## Case study: Early prediction of PPA-related metrics in Physical Design

### 1. Engineering problem

Physical Design engineers evaluate design alternatives using EDA flows. Some useful metrics, such as timing slack and power, may only be available after computationally expensive stages. A possible ML application is to estimate selected metrics earlier, helping engineers decide which configurations deserve a full run.

This is a research-supported application area, not a claim that every team uses the same model or that ML estimates replace sign-off analysis.

### 2. Data required

A training dataset could contain historical design runs with:
- Design or RTL characteristics available at prediction time.
- Cell and connectivity features, plus relevant flow settings.
- Process, voltage and temperature corner information where appropriate.
- Tool and library versions.
- Reference outputs from completed EDA runs, such as timing slack, area and power.

Only permitted data should be used. In a real company, proprietary RTL, netlists, libraries and reports must be handled under the organisation's data-security rules.

### 3. Intended output and task

| Item | Proposed choice |
|---|---|
| Main output | Estimated numerical metric, such as timing slack or power |
| Task type | Regression |
| Learning approach | Supervised learning, if completed runs provide target values |
| Intended use | Rank or screen candidate configurations for further analysis |
| Baseline | A simple heuristic or existing early estimate, where available |

A separate model could classify whether a run is likely to meet a timing target. That would be a classification task.

### 4. Evaluation plan

1. Split historical examples into training, validation and test sets.
2. Where practical, hold out complete designs or later runs to reduce leakage between similar design versions.
3. Compare predictions with reference EDA results.
4. Examine absolute error and the error distribution.
5. Compare the model with a simple baseline.
6. Check errors across design sizes, process corners, tool versions and flow settings.
7. Use predictions to support prioritisation only after validation. Confirm final results with the approved EDA flow.

### 5. Limitations and risks

- Training data may not cover a new design style, process node, library or EDA version.
- Historical results may contain inconsistent measurements or missing values.
- Data leakage can make test performance look better than real performance.
- Prediction errors may cause engineers to prioritise the wrong candidate or overlook a risk.
- The model may not generalise to unseen designs.
- The model must not replace sign-off timing, power or physical verification.

### 6. Research context

The IEEE conference paper **“Physical Synthesis Optimization Prediction Using Machine Learning”** describes supervised ML to predict selected PPA-related outputs such as timing slack, critical path depth, leakage power and area from physical-synthesis data. The reported results apply to the paper's demonstrated setting and should not be treated as a guarantee for other designs.

A second IEEE conference paper, **“Machine Learning Framework for Early Power, Performance, and Area Estimation of RTL,”** proposes estimating PPA metrics from RTL-related representations before a full synthesis flow. Its results are specific to the authors' experimental setup.

### 7. Conclusion

ML could help Physical Design by estimating numerical PPA-related metrics and reducing unnecessary full-flow experiments. The key question is whether it improves decisions compared with a simple baseline. It should be evaluated on unseen designs, monitored for changing conditions and used as engineering support rather than sign-off truth.

## Sources
1. IEEE, [Physical Synthesis Optimization Prediction Using Machine Learning](https://doi.org/10.1109/VLSID64188.2025.00018) — Research demonstration of PPA-related prediction from physical-synthesis data.
2. IEEE, [Machine Learning Framework for Early Power, Performance, and Area Estimation of RTL](https://doi.org/10.1109/ICCC64910.2025.11077283) — Research framework for early PPA estimation from RTL-related representations.
3. Google, [Understand the Problem](https://developers.google.com/machine-learning/problem-framing/problem) — Problem definition, data suitability and baseline comparisons.
4. Google, [Overfitting](https://developers.google.com/machine-learning/crash-course/overfitting/overfitting) — Generalisation and unseen data.
