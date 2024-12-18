---
title: "Two-Phase Commit Protocol Implementation in Rust"
excerpt: "A robust implementation of the distributed 2PC protocol leveraging Rust's safety features<br/><img src='/images/participantLog.png'> <br/><img src='/images/coordinatorLog.png'>"
collection: portfolio
---


## Project Overview
Developed a comprehensive implementation of the Two-Phase Commit protocol using Rust, leveraging the language's powerful type system and memory safety guarantees for distributed transaction management.

## Key Features

### Distributed Transaction Management
- Implemented coordinator and participant nodes
- Handled distributed state management across multiple processes
- Ensured atomic commit/abort decisions across the system

### Rust Safety Features Utilization
- Leveraged Rust's ownership model for safe concurrent operations
- Implemented thread-safe communication channels
- Used type system guarantees to prevent race conditions
- Applied error handling patterns using Result and Option types

### Protocol Implementation
- **Phase 1 (Prepare)**:
  - Vote request distribution
  - Participant state validation
  - Response collection and timeout handling
  
- **Phase 2 (Commit/Abort)**:
  - Global decision broadcasting
  - Transaction finalization
  - Recovery mechanisms

## Technical Details
- **Language**: Rust
- **Key Features Used**:
  - Async/await patterns
  - Channel-based communication
  - Thread safety primitives
  - Error handling mechanisms
  
## Architecture Components
- Coordinator node implementation
- Participant node implementation
- Network communication layer
- State management system
- Recovery mechanisms

## Results
Successfully implemented a robust and type-safe 2PC protocol that ensures:
- Transaction atomicity across distributed processes
- Fault tolerance and recovery capabilities
- Deadlock prevention
- Consistent state management

[View Project on GitHub](https://github.com/qyingwu/parallel_systems/tree/master/lab4) <!-- Add your GitHub link here -->