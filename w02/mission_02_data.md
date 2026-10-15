# Mission 2 — Understand Data: What Does an ML System Learn From?

## 1. Key terms

- **Dataset:** A collection of examples used to explore, train or evaluate a model.
- **Sample / observation:** One example or row in a dataset.
- **Feature:** An input value that may help predict an outcome.
- **Label / target:** The known outcome the model is trained to predict in supervised learning.
- **Structured data:** Data organised in rows and columns, such as a spreadsheet.
- **Unstructured data:** Data that does not naturally fit a simple table, such as images, audio or free-form text.
- **Numerical feature:** A number, such as cell count or estimated delay.
- **Categorical feature:** A category, such as process corner or design type.
- **Labelled data:** Examples have known target answers.
- **Unlabelled data:** Examples have no supplied target labels.

## 2. Illustrative dataset

This synthetic dataset is only for learning; it is not measured silicon data. The target is whether a design run passes a timing requirement.

| Run | Cell count (thousands) | Estimated delay (ns) | Utilisation (%) | Process corner | Timing result |
|---|---:|---:|---:|---|---|
| R1 | 12 | 0.82 | 62 | Typical | Pass |
| R2 | 18 | 1.15 | 78 | Slow | Fail |
| R3 | 10 | 0.76 | 55 | Typical | Pass |
| R4 | 21 | 1.28 | 81 | Slow | Fail |
| R5 | 15 | 0.94 | 68 | Fast | Pass |
| R6 | 17 | 1.08 | 73 | Typical | Fail |

**Features:** Cell count, estimated delay, utilisation and process corner.  
**Target/label:** Timing result (Pass/Fail).  
**Sample:** One row, for example R1.  
**Dataset:** All six rows together.

## 3. Data types

| Data | Type | Reason |
|---|---|---|
| Cell count | Numerical | It is a count represented by a number |
| Utilisation | Numerical | It is a percentage |
| Process corner | Categorical | It names a category |
| Timing result | Categorical target | It is Pass or Fail |

## 4. Data cleaning and quality

Before training, engineers should check relevance, consistency and whether the data is available at prediction time. Cleaning may include correcting units, removing duplicates, investigating impossible values, handling missing values and checking labels.

- **Missing value:** A measurement was not recorded.
- **Noisy data:** A value is affected by measurement variation or an error.
- **Inconsistent label:** Similar outcomes are labelled differently without a valid reason.
- **Unrepresentative data:** The dataset does not cover the situations where the model will be used.

More rows do not automatically mean better data. For example, mixing nanoseconds and picoseconds can mislead a model. Data collected only from one process corner may perform poorly on another.
