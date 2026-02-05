# TinyML: MNIST Digit Classification & INT8 Quantization

### 🧮 Objective
As part of my MSc in Embedded AI, this project demonstrates the mathematical optimization of a Deep Learning model for resource-constrained hardware using **Post-Training Quantization (PTQ)**.

### 📉 The Optimization Results
| Metric | Original (FP32) | Quantized (INT8) | Change |
| :--- | :--- | :--- | :--- |
| **Model Size** | 450 KB | 115 KB | ~75% Reduction |
| **Accuracy** | 98.2% | 97.9% | < 0.5% Loss |
| **Latency** | Baseline | 3.2x Faster | Optimized |

### 🛠️ The Math Behind the Code
Using the linear mapping _**x = S(q - Z)**_, I transformed the weights from 32-bit floating point to 8-bit integers. This allows the model to run on microcontrollers (like ESP32 or STM32) that lack a Floating Point Unit (FPU).

### 🚀 How to Run
1. Clone the repo.
2. Open `notebooks/MNIST_Quantization_Analysis.ipynb`.
3. Run the cells to see the size comparison.
