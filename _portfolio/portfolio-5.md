---
title: "Low-Memory Deep Network Optimization (PyTorch)"
excerpt: "Memory-efficient deep learning with half precision, LoRA, QLoRA, and 4-bit quantization using PyTorch<br/><img src='/images/lowmem-summary.png'>"
collection: portfolio
---

## Project Overview
Implemented memory-optimized versions of a large-scale deep network (`BigNet`, ~19M parameters) using advanced quantization and fine-tuning techniques in PyTorch. This project demonstrates techniques for deploying deep models under strict memory constraints while preserving training capability and output accuracy.

## Key Features
- **Half Precision & Quantization**:
  - Converted full-precision weights to `float16` to halve memory usage
  - Applied **4-bit block quantization** with custom de/quantization logic
  - Achieved up to **7× memory reduction** in model storage and training overhead

- **Parameter-Efficient Fine-Tuning**:
  - Integrated **LoRA** adapters on top of half-precision base model
  - Extended to **QLoRA** for low-rank training on quantized weights
  - Verified convergence and functional correctness via model comparison and noise training objectives

- **Benchmarking & Validation**:
  - Custom memory profiler to validate actual and theoretical memory usage
  - Model output comparisons with original `BigNet` (within tight numerical tolerance)
  - Backward training tests for LoRA and QLoRA under constrained GPU memory
  <img src='/images/lowmem-memory-chart.png'>

## Technical Details
- **Languages & Technologies**:
  - Python, PyTorch
  - Custom quantization modules
  - No external dependencies (e.g., HuggingFace)

- **Techniques Used**:
  - Half precision `float16` linear layers
  - 4-bit groupwise quantization with normalization
  - Pre-hook state dict management for loading quantized weights
  - Mixed-precision forward/backward pass handling

## Results
The implementation achieves:
- Up to **7× memory reduction**
- Minimal output error (≤ 0.002) from baseline
- Training convergence with **LoRA** and **QLoRA**
- Enables deployment of large models on low-resource environments

[View Project on GitHub](https://github.com/qyingwu/advances_dl/tree/main/homework1)
