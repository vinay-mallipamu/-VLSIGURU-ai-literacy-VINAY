# Mission 5 — Experiment and Observe

## Purpose
Investigate whether increasing neural-network complexity always improves classification. This activity uses the interactive TensorFlow Playground and does not require Python.

**Tool:** https://playground.tensorflow.org/

## Procedure
1. Open the Playground and select a simple classification dataset.
2. Record the dataset, input features, activation function, learning rate, regularisation and starting network structure.
3. Start training and observe the decision boundary and training behaviour.
4. Add a hidden layer or change the number of neurons.
5. Train again under comparable settings.
6. Compare the decision boundary, training behaviour and (where shown) test performance.
7. Save screenshots and record what you actually observed.

## Experiment log — fill in after your own run

| Item | Starting configuration | Modified configuration |
|---|---|---|
| Dataset | [enter] | Same dataset |
| Input features | [enter] | [enter] |
| Hidden layers | [enter] | [enter] |
| Neurons per layer | [enter] | [enter] |
| Activation | [enter] | [enter] |
| Learning rate | [enter] | [enter] |
| Regularisation | [enter] | [enter] |
| Training observations | [your observation] | [your observation] |
| Test observations | [your observation] | [your observation] |
| Screenshot | [add file path] | [add file path] |

## Questions and interpretation
- **What changed?** Describe the decision boundary and training behaviour you saw, not what you expected to see.
- **Did the more complex network always perform better?** Do not assume so. Use the test behaviour shown by your experiment as evidence.
- **Complexity and patterns:** additional neurons or layers can represent more complex boundaries, but can also fit noise or become harder to train.
- **Why is training performance insufficient?** A model can fit its training examples while failing on unseen data. Generalisation must be checked.
- **How is Playground different from real inspection images?** Playground uses simplified, synthetic 2D data. Real inspection images have high-dimensional pixels, process variation, rare defects, labelling uncertainty and operational constraints.
- **What evidence is needed for practical use?** Representative independent data, appropriate class-wise metrics, tests across lots and conditions, robustness checks, error analysis, latency/resource measurements and human/engineering acceptance.

## Conclusion template
> In my experiment, the starting network had [configuration] and the modified network had [configuration]. I observed [specific change in decision boundary / training behaviour]. The more complex network [did / did not] improve the test result in this run. This suggests that model complexity alone does not guarantee better generalisation. I would need representative real inspection data and independent evaluation before claiming suitability for semiconductor inspection.

**Important:** The template above is not a claim that an experiment has already been performed. Replace bracketed fields with your own recorded evidence and attach screenshots.
