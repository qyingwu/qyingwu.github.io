---
title: "Reasoning-Based Unit Conversion with SmolLM2 (LLM + LoRA + RFT)"
excerpt: "Built a unit conversion language model using in-context learning, LoRA fine-tuning, and rejection-based RL on top of SmolLM2 for reasoning-aware generation<br/><img src='/images/unit-conversion-llm.png'>"
collection: portfolio
---

## Project Overview
Trained a reasoning-capable unit conversion model using **SmolLM2**, combining **in-context learning**, **LoRA-based supervised fine-tuning**, and **rejection sampling fine-tuning (RFT)**. The system was designed to perform both numerical conversions and explain reasoning steps in a chain-of-thought format.

## Key Features

- **Batched Text Generation**:
  - Implemented both sequential and batched decoding pipelines for **SmolLM2-1.7B**
  - Optimized input padding, attention masking, and output decoding for efficient GPU utilization

- **In-Context Learning with CoT Prompting**:
  - Engineered a system/user/assistant dialogue prompt to guide LLM reasoning
  - Used **chain-of-thought (CoT)** prompting to improve multi-step conversion accuracy
  - Achieved high answer correctness and reasoning coherence through tuned chat templates

- **Supervised Fine-Tuning (SFT) with LoRA**:
  - Fine-tuned the base LLM with LoRA adapters (<20MB), targeting unit conversion tasks directly
  - Used `<answer>{value}</answer>` format for explicit numeric supervision
  - Trained using Hugging Face’s `Trainer` with gradient checkpointing for memory efficiency

- **Rejection-Based Fine-Tuning (RFT)**:
  - Generated diverse CoT responses via temperature sampling and selected correct completions
  - Constructed a dataset of [question, correct reasoning, answer] triples
  - Re-trained model on this enhanced dataset, yielding improved accuracy and interpretability
  <img src='/images/rft_sampling_success.png'>

- **Evaluation & Generation**:
  - Evaluated model on reasoning steps, answer rate, and generation correctness
  - Supported custom prompts, temperature control, and batch decoding for inference

## Technical Details

- **Languages & Libraries**:
  - Python, PyTorch, Hugging Face Transformers, LoRA (PEFT), SmolLM2
  - TensorBoard for logging and progress tracking

- **LLM Techniques Used**:
  - Chain-of-Thought prompting
  - LoRA-based parameter-efficient fine-tuning
  - Rejection-based data filtering and reward modeling

- **Challenges Solved**:
  - Avoided `generate` performance bottlenecks with custom batched decoding
  - Ensured compatibility with custom chat templates and JSON-based RFT dataset format
  - Tuned LoRA rank to stay under 50MB model limit while preserving performance

## Results

- Achieved >85% valid answer rate and >50% accuracy with in-context CoT prompting
- Improved accuracy further using LoRA SFT and RFT with CoT data
- Enabled interpretable unit conversion via step-by-step model reasoning
- Demonstrated end-to-end LLM training without relying on pretrained pipelines

[View Project on GitHub](https://github.com/qyingwu/advances_dl/tree/main/homework3_v3)
