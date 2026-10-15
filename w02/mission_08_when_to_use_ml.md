# Mission 8 — Does This Problem Actually Need ML?

## Example problem

**Goal:** Identify physical-design runs that may fail timing, early enough to help engineers decide which runs need attention.

## Compare a fixed rule with a possible ML solution

| Point | Rule-based solution | Possible ML solution |
|---|---|---|
| Method | Apply a known threshold, such as flagging estimated delay above a limit | Learn relationships from historical features and known timing outcomes |
| Data needed | Current measurement and chosen threshold | Representative historical examples with trustworthy pass/fail labels |
| Strength | Simple, transparent and easy to test | May capture relationships that are hard to express with a few rules |
| Limitation | A fixed threshold may miss interactions among features | Can make mistakes, drift and needs evaluation |
| Failure mode | Wrong threshold or incorrect measurement | Poor labels, biased data, leakage, overfitting or changed conditions |
| Evaluation | Check false alarms and missed failures | Compare on held-out designs using recall, precision and other relevant measures |

## Decision

I would start with a simple rule-based baseline because it is easier to explain and may already solve the problem. I would consider ML only if the rule is not good enough, suitable historical data exists, and evaluation shows useful improvement on unseen designs.

The team should measure how many real timing failures are detected, how many passing runs are incorrectly flagged, and whether the model saves engineering time. A model prediction should help prioritise investigation; final timing sign-off must still use the approved design flow.

## Sources
- Google, [Understand the Problem](https://developers.google.com/machine-learning/problem-framing/problem)
- Google, [Framing an ML Problem](https://developers.google.com/machine-learning/problem-framing/ml-framing)
- Google, [Problem Framing Summary](https://developers.google.com/machine-learning/problem-framing/summary)
