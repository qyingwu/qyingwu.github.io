---
title: "Deep Learning Projects in Computer Vision"
excerpt: "A collection of deep learning projects focusing on image classification and autonomous driving <br/><img src='/images/controller.png'>"
collection: portfolio
---


## Project Overview
A comprehensive series of deep learning projects implemented using PyTorch, focusing on computer vision tasks and neural network architectures.

## Key Projects

### 1. Image Classification with SuperTuxKart Dataset
- **Dataset Implementation**:
  - Developed custom PyTorch DataLoader for SuperTuxKart image dataset
  - Implemented efficient image processing pipeline handling 64x64 RGB images
  - Created robust data handling for 6 distinct classes (background, kart, pickup, nitro, bomb, projectile)
  - Utilized PIL and torchvision for optimized image loading and transformation

- **Model Architecture**:
  - **Linear Classifier**:
    - Implemented basic linear classification model
    - Designed input layer handling (3,64,64) tensor inputs
    - Created output layer producing 6-class predictions
  
  - **Multi-Layer Perceptron (MLP)**:
    - Developed non-linear classification architecture
    - Implemented multiple hidden layers with ReLU activations
    - Optimized layer sizes for parameter efficiency
    - Achieved improved accuracy over linear baseline

- **Training Pipeline**:
  - Implemented custom loss function using softmax cross-entropy
  - Developed flexible training loop supporting multiple model architectures
  - Integrated validation monitoring and model checkpointing
  - Applied SGD optimization with hyperparameter tuning


### 2. Advanced CNN Architecture for SuperTuxKart Classification
- **CNN Model Architecture**:
  - Designed and implemented a custom CNN classifier achieving >85% test accuracy
  - Developed sophisticated convolutional layers for efficient feature extraction
  - Optimized model architecture for 64x64 RGB input images
  - Implemented stride and padding strategies for optimal spatial reduction
  - Created final classification layer producing 6-class logits

- **Performance Monitoring & Visualization**:
  - Integrated TensorBoard logging system for comprehensive training analytics
  - Implemented real-time monitoring of:
    - Training loss per iteration
    - Training accuracy per epoch
    - Validation accuracy per epoch
  - Developed custom visualization tools for model predictions
  - Created performance dashboards for model evaluation

- **Training Infrastructure**:
  - Implemented flexible training pipeline supporting:
    - Batch processing
    - Learning rate scheduling
    - Model checkpointing
    - Cross-entropy loss optimization
  - Integrated GPU acceleration support
  - Developed Google Colab compatibility for cloud training
  - Achieved significant performance improvement over MLP baseline

- **Technical Achievements**:
  - Successfully maintained model size under 20MB while maximizing accuracy
  - Implemented proper image normalization within model architecture
  - Created robust validation procedures to prevent overfitting
  - Developed efficient data processing pipeline for training and inference

### 3. Advanced CNN Optimization and Semantic Segmentation
- **Enhanced CNN Classification**:
  - Achieved 90%+ classification accuracy through advanced optimization techniques:
    - Implemented input normalization and data augmentation pipeline
    - Designed residual blocks for improved gradient flow
    - Applied dropout for regularization
    - Developed comprehensive data augmentation strategy:
      - Geometric transformations
      - Color jittering
      - Lighting variations
    - Implemented early stopping and weight regularization
  - Optimized training pipeline achieving 94% accuracy

- **Fully Convolutional Network (FCN) Implementation**:
  - Transformed CNN architecture into fully convolutional design
  - Developed architecture supporting arbitrary input resolutions
  - Implemented pixel-wise classification for 5 classes:
    - Background
    - Kart
    - Track
    - Bomb/Projectile
    - Pickup/Nitro
  - Created skip connections and residual pathways for improved feature propagation

- **Dense Prediction Optimization**:
  - Handled class imbalance challenges (96% background/track)
  - Implemented Intersection-over-Union (IoU) evaluation metric
  - Developed custom loss weighting strategy
  - Created specialized data augmentation pipeline for dense prediction:
    - Synchronized image-label transformations
    - Resolution-preserving augmentations
    - Custom dense transform implementations

- **Technical Implementation Details**:
  - Utilized advanced PyTorch features:
    - ConvTranspose2d for upsampling
    - Skip connections via tensor concatenation
    - Adam optimizer with custom learning rate scheduling
  - Implemented proper padding and stride management
  - Created efficient feature pyramid architecture
  - Developed custom confusion matrix for IoU tracking


### 4. Point-Based Object Detection System
- **Custom Object Detector Implementation**:
  - Developed point-based object detection system for SuperTuxKart
  - Implemented detection for three object classes:
    - Karts
    - Bombs/Projectiles
    - Pickup items
  - Achieved high accuracy metrics:
    - AP scores > 0.75 for karts
    - AP scores > 0.45 for projectiles
    - AP scores > 0.85 for pickups

- **Heatmap-Based Detection Architecture**:
  - Designed dense prediction network for object center localization
  - Implemented efficient peak extraction algorithm:
    - GPU-accelerated local maxima detection
    - Custom max-pooling based peak finding
    - Threshold-based detection filtering
  - Created multi-channel output for simultaneous class detection
  - Developed confidence scoring mechanism for detection ranking

- **Advanced Training Pipeline**:
  - Implemented specialized loss functions:
    - Binary Cross-Entropy with Logits
    - Focal Loss for handling class imbalance
  - Created custom data transformations:
    - Heatmap generation for ground truth
    - Synchronized image-label augmentations
  - Integrated TensorBoard monitoring for training visualization

- **Performance Optimization**:
  - Implemented dual evaluation metrics:
    - Point-in-box detection accuracy
    - Center-distance measurement (5px threshold)
  - Developed efficient detection post-processing:
    - Local maxima filtering
    - Confidence thresholding
    - Size-aware detection handling
  - Achieved test set performance exceeding baseline requirements

### 5. Vision-Based Autonomous Driving System
- **Low-Level Controller Development**:
  - Implemented precise steering control system for SuperTuxKart
  - Developed advanced control algorithms for:
    - Steering angle calculation
    - Acceleration management
    - Brake timing
    - Drift activation
    - Nitro optimization
  - Achieved efficient completion times:
    - Under 50s for Zengarden and Lighthouse tracks
    - Under 60s for Hacienda and Snowtuxpeak
    - Under 70s for Cornfield Crossing and Scotland

- **Vision-Based Planning System**:
  - Designed CNN-based planner for aim point prediction
  - Implemented encoder-decoder architecture for:
    - Image feature extraction
    - Spatial understanding
    - Aim point heatmap generation
  - Created custom spatial argmax layer for precise point prediction
  - Developed robust data collection pipeline across multiple tracks

- **Training Infrastructure**:
  - Created comprehensive dataset generation system:
    - Automated data collection across 6 different tracks
    - Generated paired image and aim point data
    - Implemented efficient data storage and loading
  - Developed specialized training pipeline:
    - Custom loss functions for aim point prediction
    - Real-time visualization tools
    - Performance monitoring systems

- **System Integration and Performance**:
  - Successfully integrated planning and control systems
  - Achieved reliable autonomous navigation on:
    - 6 known test tracks
    - Previously unseen validation tracks
  - Implemented robust error handling and recovery
  - Optimized system for real-time performance




## Technical Stack
- **Framework**: PyTorch
- **Language**: Python
- **Key Libraries**: 
  - torchvision
  - numpy
  - matplotlib
  - PIL

## Results
The projects demonstrate progressive improvement in model architecture design and implementation, showcasing both theoretical understanding and practical application of deep learning concepts.

[View Projects on GitHub](https://github.com/qyingwu/deepLearning/tree/main)<!-- Add your GitHub link here -->