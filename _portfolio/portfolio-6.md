---
title: "Auto-Regressive Image Generation & Compression (PyTorch)"
excerpt: "Built a custom auto-regressive image generator and BSQ quantizer for compressing SuperTuxKart game images using deep learning techniques in PyTorch<br/><img src='/images/bsq_generation.png'>"
collection: portfolio
---

## Project Overview
Built a complete deep learning pipeline for **auto-regressive image generation and compression**, from patch-level encoding to token-based generation. The system combines **Binary Spherical Quantization (BSQ)** with a **Transformer-based autoregressive model**, achieving effective image representation and sampling from scratch.

## Key Features

- **Patch-Level Autoencoder**:
  - Encoded images into patch-wise latent embeddings using a shallow encoder-decoder network
  - Trained on SuperTuxKart game images with flexible patch size configuration
  - Enabled dimensionality reduction for token-level processing

- **Binary Spherical Quantization (BSQ)**:
  - Implemented custom binary quantizer with straight-through estimator
  - Converted float features into binary {-1, +1} vectors and indexed tokens
  - Achieved ~6× dataset compression with minimal loss using tokenized patches
  <img src='/images/bsq_diagram.png'>

- **Auto-Regressive Transformer**:
  - Designed and trained a **causally masked transformer decoder** to model next-token prediction
  - Flattened patch tokens and learned sequential dependencies with cross-entropy loss
  - Generated coherent low-resolution image patches and reconstructed them via decoder
  <img src='/images/gen_pos_2.png'>

- **Image Generation & Sampling**:
  - Implemented sampling loop for generating novel token sequences and decoding to full images
  - Compared generation quality with and without positional embeddings
  - Supported generation from scratch or conditional inputs

- **Optional Compression (Extra Credit)**:
  - Explored entropy coding of auto-regressive outputs to reduce image size below **500 bytes per frame**
  - Demonstrated compression performance comparable to lossy formats like JPEG

## Technical Details

- **Languages & Tools**:
  - Python, PyTorch, NumPy
  - TensorBoard for training visualization
  - Custom tokenizer and quantizer modules

- **Model Architecture**:
  - Patch Autoencoder → BSQ Bottleneck → Tokenization → Transformer Decoder
  - Fully trainable end-to-end setup with checkpointed training for each stage

- **Challenges Addressed**:
  - Efficient binarization on Apple Silicon (MPS) by replacing bit-shift with differentiable arithmetic
  - Ensured compatibility and precision across devices during quantization and decoding

## Results

- Achieved **~7× dataset compression** with tokenized patches
- Generated novel image samples with up to **4500 bits/image** using a compact transformer
- Enabled end-to-end generative modeling from images with no pretrained models
- Demonstrated a complete VQ-like pipeline using only custom components

[View Project on GitHub](https://github.com/qyingwu/advances_dl/tree/main/homework2_v5_2_28)
