---
title: "Barnes-Hut Algorithm Implementation (C++)"
excerpt: "Parallel N-body simulation using Barnes-Hut algorithm and MPI for distributed computing, achieving near-linear speedup<br/><img src='/images/simulation.png'>"
collection: portfolio
---

# Parallel Barnes-Hut N-body Simulation

## Project Overview
Implemented a sophisticated parallel N-body simulation using the Barnes-Hut algorithm with MPI for distributed computing. This project demonstrates advanced parallel programming concepts and optimization techniques for complex physical simulations.

## Key Features
- **Barnes-Hut Algorithm Implementation**:
  - O(n log n) complexity optimization over naive O(n²) approach
  - Spatial partitioning using octree data structure
  - Center of mass approximation for distant body interactions
  - Dynamic tree reconstruction for moving bodies

- **Parallel Processing Architecture**:
  - Distributed computation using MPI
  - Load balancing for irregular data structures
  - Efficient communication patterns for body distribution
  - Dynamic work distribution as bodies move
  <img src='/images/speedupgraphstep1000.png'>

- **Physics Engine Components**:
  - Gravitational force calculation with softening
  - Leapfrog-Verlet integration for position updates
  - Multipole Acceptance Criteria (MAC) optimization
  - Boundary condition handling

- **Visualization and Analysis**:
  - OpenGL-based real-time visualization
  - Performance monitoring and analysis tools
  - Configurable simulation parameters
  - Interactive visualization controls
  <img src='/images/simulation.png'>

## Technical Details
- **Language & Technologies**:
  - C++ for core implementation
  - MPI for parallel processing
  - OpenGL/GLFW for visualization
  - Make-based build system

- **Performance Optimizations**:
  - Spatial locality improvements
  - Communication overhead reduction
  - Load balancing strategies
  - Memory access pattern optimization

## Results
The implementation demonstrates excellent scalability across multiple processors, with performance measurements showing:
- Near-linear speedup up to 8 processors
- Efficient handling of large particle systems
- Balanced communication-to-computation ratio
- Stable numerical integration over long time periods

[View Project on GitHub](https://github.com/qyingwu/parallel_systems/tree/main/lab5)