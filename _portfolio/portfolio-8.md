---
title: "Vision-Language Model for SuperTuxKart (VLM + LoRA)"
excerpt: "Trained a vision-language model on SuperTuxKart data using custom QA generation and LoRA fine-tuning, achieving >70% accuracy on unseen visual queries<br/><img src='/images/vlm-tux-example.png'>"
collection: portfolio
---

## Project Overview
Built a **vision-language model (VLM)** pipeline that learns to answer questions about visual scenes from the **SuperTuxKart** game. The project focused on designing an effective **data pipeline** to convert raw scene metadata into QA pairs and fine-tuning a VLM using **LoRA adapters**.

## Key Features

- **Custom VLM Dataset Generation**:
  - Parsed raw SuperTuxKart simulation data to extract image annotations and scene metadata
  - Automatically generated question-answer pairs across multiple categories (object count, color, position, etc.)
  - Created a large-scale JSON-based dataset for training with minimal manual annotation
  <img src='/images/vlm-qa-gen.png'>

- **LoRA-based Vision-Language Fine-Tuning**:
  - Fine-tuned a pretrained VLM on the generated dataset using LoRA adapters
  - Achieved accurate visual reasoning with a compact model size under **50MB**
  - Supported question answering over diverse camera viewpoints and scenarios

- **Training & Evaluation**:
  - Used provided scripts to fine-tune and benchmark the model on validation/test splits
  - Avoided data leakage by programmatically separating training and validation QA pairs
  - Achieved over **70% accuracy** on held-out test questions; eligible for extra credit with >85%

- **Visualization and Debugging**:
  - Implemented visualization tools to inspect QA pairs and align answers with visual context
  - Validated dataset correctness using image overlays and semantic validation
  <img src='/images/vlm-visualization-debug.png'>

## Technical Details

- **Languages & Frameworks**:
  - Python, PyTorch, Hugging Face Transformers
  - LoRA (PEFT) for parameter-efficient VLM fine-tuning
  - JSON, OpenCV, and Matplotlib for data annotation and visualization

- **System Architecture**:
  - Image + metadata → question/answer generator → fine-tuned VLM → accuracy evaluation
  - Modular data loading via `data.py` and LoRA integration in `base_vlm.py`

## Results

- Created a synthetic vision-language dataset from simulation metadata
- Trained a VLM with LoRA adapters that generalizes to unseen image questions
- Achieved >70% test accuracy on visual QA tasks, with potential for 85%+ using advanced filtering
- Demonstrated end-to-end control over VLM performance via data-centric engineering

[View Project on GitHub](https://github.com/qyingwu/advances_dl/tree/main/homework_04_v4)
