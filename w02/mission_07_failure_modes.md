# Mission 7 — Understand Why ML Systems Fail

## Failure 1: Poor or unrepresentative data

**Scenario:** A timing prediction model is trained mostly on small designs and then used on a much larger SoC.

- **Likely cause:** Training data does not represent the designs where the model is now used.
- **Evidence:** Compare design sizes, cell counts, utilisation, process corners and prediction errors in training versus new runs.
- **Mitigation:** Collect representative examples, evaluate on held-out designs, and define the model's supported range.

## Failure 2: Incorrect labels or missing values

**Scenario:** Some historical runs are marked Pass even though final timing reports show a violation. Some rows also have missing delay values.

- **Likely cause:** Label mistakes, inconsistent report parsing or careless handling of missing values.
- **Evidence:** Audit labels against original reports, count missing values and inspect suspicious outliers.
- **Mitigation:** Define consistent labelling rules, validate data extraction and document missing-value handling.

## Failure 3: Data leakage and changing conditions

**Scenario:** A model achieves very high test accuracy, but performance falls after the EDA flow or library version changes. A feature also includes a result only known after the prediction should have been made.

- **Likely cause:** **Data leakage** makes evaluation look better than real use, while **data drift** changes the relationship between inputs and outcomes.
- **Evidence:** Review feature timestamps, confirm the train/test split, compare error by tool/library version and monitor results over time.
- **Mitigation:** Remove unavailable-at-prediction-time features, split data to reflect real use, test on newer independent data and monitor performance.

## Additional risks

- **Bias:** Under-represented design types or conditions may have worse model performance.
- **Human oversight:** Engineers should investigate uncertain or high-impact predictions. ML should not automatically override approved sign-off tools.
- **Consequences:** A false prediction can waste compute time, hide a risk or encourage a poor design choice.

## Sources
- Google, [Overfitting](https://developers.google.com/machine-learning/crash-course/overfitting/overfitting)
- Google, [Understand the Problem](https://developers.google.com/machine-learning/problem-framing/problem)
- Google, [Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course/)
