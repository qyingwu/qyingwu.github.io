---
title: "Parallel CUDA KMeans Clustering (C++/CUDA)"
excerpt: "High-performance implementation of KMeans clustering algorithm using CUDA parallel computing<br/><img src='totalSpeedUp.png'>"
collection: portfolio
---

# CUDA KMeans Clustering Implementation

## Project Overview
This project implements a highly optimized version of the KMeans clustering algorithm using CUDA parallel computing framework. By leveraging the massive parallel processing capabilities of GPUs, the implementation achieves significant speedup compared to traditional CPU-based approaches.

## Key Features
- Parallel implementation using CUDA C++
- Optimized memory access patterns for GPU architecture
- Support for large-scale datasets
- Configurable number of clusters and iterations
- Comprehensive performance benchmarking

## Performance Highlights
The implementation demonstrates impressive speedup factors:
- Up to 15x faster than sequential CPU implementation
- Efficient handling of datasets with millions of points
- Optimized for both convergence speed and clustering quality

## Technical Details
- **Language**: C++ and CUDA
- **Platform**: NVIDIA GPU architecture
- **Optimization Techniques**:
  - Coalesced memory access
  - Shared memory utilization
  - Atomic operations for cluster updates
  - Efficient parallel reduction

## Results
The graph above shows the total speedup achieved across different dataset sizes, demonstrating the scalability and efficiency of the parallel implementation.

[View Project on GitHub](#) <!-- Add your GitHub link here -->