---
title: "Parallel CUDA KMeans Clustering (C++/CUDA)"
excerpt: "High-performance implementation of KMeans clustering algorithm using CUDA parallel computing <br/><img src='/images/cuda.png'> <br/><img src='/images/totalSpeedUp.png'> "
collection: portfolio
---


## Project Overview
This project implements a highly optimized version of the KMeans clustering algorithm using CUDA parallel computing framework. By leveraging the massive parallel processing capabilities of GPUs, the implementation achieves significant speedup compared to traditional CPU-based approaches.

## Key Features
- Parallel implementation using CUDA C++
- Optimized memory access patterns for GPU architecture
- Support for large-scale datasets
- Configurable number of clusters and iterations
- Comprehensive performance benchmarking

## Implementation Approaches

### 1. CUDA Global Memory Implementation
- Direct implementation using CUDA global memory
- Basic parallel processing without memory optimization
- Baseline performance measurements
<img src='/images/cudaGmemSpeedup.png'>

### 2. CUDA Shared Memory Optimization
- Enhanced implementation utilizing shared memory
- Reduced global memory access latency
- Improved thread block cooperation
- Significant performance improvement over global memory version
<img src='/images/cudaShmemSpeedup.png'>

### 3. CUDA Thrust Library Implementation
- High-level implementation using Thrust library
- Simplified parallel algorithms and data structures
- Automatic optimization of common operations
- Excellent balance of performance and code maintainability
<img src='/images/cudaThrustSpeedUp.png'>

## Performance Comparison
- Global Memory: Baseline performance
- Shared Memory: 2-3x speedup over global memory
- Thrust: Comparable performance to shared memory with simplified code
<img src='/images/cuda_comparison.png'>


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

[View Project on GitHub](https://github.com/qyingwu/parallel_systems/blob/master/lab2/Lab2Report/Lab2.pdf)