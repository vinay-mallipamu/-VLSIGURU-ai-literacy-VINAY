# Mission 6 — Understand Evaluation and Generalisation

## 1. Data splits

- **Training set:** Used to fit the model's parameters.
- **Validation set:** Used during development to compare models or settings.
- **Test set:** Held aside for a final evaluation after model choices are made.

## 2. Key terms

- **Generalisation:** How well a model works on new, unseen examples.
- **Overfitting:** The model fits training examples too closely and performs worse on unseen data.
- **Underfitting:** The model is too simple or insufficiently trained to capture the important pattern.
- **Accuracy:** Fraction of all predictions that are correct.
- **Precision:** Of cases predicted positive, how many are truly positive?
- **Recall:** Of all truly positive cases, how many did the model find?
- **False positive:** Predicted positive when the true class is negative.
- **False negative:** Predicted negative when the true class is positive.
- **Absolute error:** Magnitude of the difference between a predicted number and the true number.

## 3. Worked example: accuracy can mislead

Suppose a test set has 1,000 chip runs: 990 pass timing and 10 fail timing. A model predicts **Pass for every run**.

| Actual class | Model prediction | Count |
|---|---|---:|
| Pass | Pass (correct) | 990 |
| Fail | Pass (incorrect; failure missed) | 10 |
| Total |  | 1,000 |

Accuracy = 990 / 1,000 = **99%**.

However, the model detects **0 out of 10 timing failures**. It is not useful for finding failures even though accuracy looks high.

- **Recall for the Fail class:** 0 / 10 = 0%. This reveals that every failure was missed.
- **Precision for predicted Fail:** Undefined because the model predicted no Fail cases.
- A confusion matrix and the counts of false negatives should be reviewed, not accuracy alone.

If missing a timing failure is costly, failure-class recall and false negatives are important. Compare the model with a simple baseline, such as predicting the majority class, to check whether it adds value.

## Sources
- Google, [Overfitting](https://developers.google.com/machine-learning/crash-course/overfitting/overfitting)
- Google, [Classification](https://developers.google.com/machine-learning/crash-course/classification)
- Google, [Problem Framing](https://developers.google.com/machine-learning/problem-framing/ml-framing)
