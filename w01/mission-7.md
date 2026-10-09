7:Explain CPU, GPU, and NPU, and what hardware runs AI


## 1. What is a CPU and what is it good at?

CPU stands for Central Processing Unit. It is one of the main parts of a computer. It runs programs, follows instructions and manages different tasks. It is good at handling different types of work and making decisions based on conditions.

## 2. What is a GPU and why is it useful for AI?

GPU stands for Graphics Processing Unit. It was originally designed to handle graphics, but it is also useful for AI. AI models need to perform many calculations, and a GPU can handle many of them at the same time. This helps speed up AI tasks.

## 3. What is an NPU or AI accelerator?

An NPU stands for Neural Processing Unit. It is designed to handle AI-related calculations efficiently. It can run certain AI tasks using less power than a general-purpose processor. This is useful in devices like smartphones and laptops.

## 4. What does parallel computation mean?

Parallel computation means doing multiple calculations at the same time instead of doing each one separately.

For example, if I have to add ten different pairs of numbers, I can calculate several pairs at the same time if the calculations are independent. This saves time.

## 5. Why does AI depend on compute and memory?

AI models need to perform a large number of calculations to produce results. They also need memory to store the model's parameters and the information being processed. If the processor is slow or there is not enough memory, the AI model may take longer to respond.

## 6. Training vs Inference

| Training                                                    | Inference                                                |
| ----------------------------------------------------------- | -------------------------------------------------------- |
| The model learns from data.                                 | The trained model is used to give an answer.             |
| It involves repeated calculations over training data.       | It performs calculations for a particular input.         |
| It usually needs more computing resources for large models. | It can run on a GPU, NPU or CPU, depending on the model. |
| The goal is to learn useful patterns.                       | The goal is to produce a result.                         |

## 7. Simple Diagram

```text
┌─────────────────────────┐
│     AI APPLICATION      │
│  Chatbot or Voice App   │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│        AI MODEL         │
│   Learns or predicts    │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│   SOFTWARE / FRAMEWORK  │
│  PyTorch or TensorFlow  │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│    CPU / GPU / NPU      │
│  Performs calculations  │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│         MEMORY          │
│ Stores data and model   │
│      parameters         │
└─────────────────────────┘
```

## 8. One Real AI Workload: Voice Assistant

A voice assistant is an example of AI that I use in everyday life. When I speak to my phone, the system processes my voice and tries to understand what I said.

A CPU can manage the general tasks, while a GPU or NPU can help with AI calculations. An NPU is useful for this task because it can process AI workloads efficiently while using less battery power. The exact hardware depends on the phone and how the voice assistant is designed.

## What I Learned

I learned that AI does not work only through software. It also needs hardware to perform calculations and memory to store the required data. CPUs, GPUs and NPUs have different roles, and choosing suitable hardware can improve AI performance and reduce power consumption.

## Source

NVIDIA — What Is a GPU?
https://www.nvidia.com/en-us/glossary/gpu/

Google Cloud — What Is a GPU?
https://cloud.google.com/discover/what-is-a-gpu

