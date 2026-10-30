# Mission 3 – Opening a Neural Network

## 1. Main components

- **Input layer:** receives the numerical input. For an image, the input values can be pixel values.
- **Hidden layers:** process information between input and output. Each neuron receives values from earlier neurons and calculates a new value.
- **Output layer:** produces the model's result, such as class scores or probabilities.
- **Weights:** numerical values that control the strength of connections between neurons.
- **Biases:** additional learned values that shift a neuron's calculation.
- **Activation function:** transforms a neuron's weighted input. Examples include ReLU and sigmoid.

A simplified neuron calculation is:

`z = w1*x1 + w2*x2 + ... + wn*xn + b`

`output = activation(z)`

Here, `x` values are inputs, `w` values are weights, and `b` is the bias.

## 2. Labelled network diagram

```mermaid
flowchart LR
    subgraph IN[Input layer]
      I1[Pixel value 1]
      I2[Pixel value 2]
      I3[Pixel value 3]
    end
    subgraph H1[Hidden layer 1]
      H11[Neuron 1]
      H12[Neuron 2]
      H13[Neuron 3]
    end
    subgraph H2[Hidden layer 2]
      H21[Neuron 1]
      H22[Neuron 2]
    end
    subgraph OUT[Output layer]
      O1[No-defect score]
      O2[Defect score]
    end
    I1 --> H11
    I1 --> H12
    I2 --> H11
    I2 --> H13
    I3 --> H12
    I3 --> H13
    H11 --> H21
    H12 --> H21
    H12 --> H22
    H13 --> H22
    H21 --> O1
    H21 --> O2
    H22 --> O1
    H22 --> O2
```

The arrows represent connections. In a real network, each connection has a learned weight. The diagram is simplified and does not show every possible connection.

## 3. Trace one inspection image

1. A prepared inspection image is converted into numerical pixel values.
2. Those values enter the input layer.
3. Hidden-layer neurons combine incoming values using weights and biases, then apply activation functions.
4. Later layers process the resulting values.
5. The output layer produces scores for the available classes.
6. A decision rule may select the class with the highest score, while a production system may also use confidence thresholds and human review.

For illustration only, suppose the output scores are `no_defect = 0.20` and `defect = 0.80`. The larger score favours the defect class. These numbers are examples, not results from a real experiment or trained model. A prediction is not proof; it must be evaluated against verified labels and the real inspection requirements.
