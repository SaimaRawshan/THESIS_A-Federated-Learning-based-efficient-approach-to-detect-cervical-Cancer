# THESIS_A-Federated-Learning-based-efficient-approach-to-detect-cervical-Cancer

## Overview
This project proposes a privacy-preserving federated learning framework for automated cervical cancer detection using Pap smear images. The system introduces a lightweight deep learning architecture called **FedPapVisionNet** designed to operate efficiently in decentralized medical environments.

The framework enables collaborative training across multiple clients (institutions) without sharing sensitive patient data, ensuring privacy while maintaining high diagnostic performance.

## Key Features
- Privacy-preserving Federated Learning framework
- Lightweight deep learning model: **FedPapVisionNet**
- Support for IID and Non-IID data distributions
- Comparison with multiple pretrained deep learning models
- Evaluation using multiple federated optimization algorithms

## Dataset
The experiments use the **SIPaKMeD (Single-cell Pap Smear)** dataset which contains **4049 cervical cell images** categorized into five classes:

- Dyskeratotic
- Koilocytotic
- Metaplastic
- Parabasal
- Superficial-Intermediate

## Data Preprocessing
The following preprocessing steps were applied:

- Image resizing to **128×128**
- Normalization
- Data augmentation:
  - Random horizontal flipping
  - Random rotation
  - Color jitter
  - Affine transformations

## Federated Learning Algorithms
The framework evaluates three federated aggregation strategies:

- **FedAvg**
- **FedProx**
- **SCAFFOLD**

These algorithms help analyze model performance under both **IID** and **Non-IID** data distributions.

## Model Architectures
The study evaluates multiple models including:

### Pretrained Models
- VGG16
- VGG19
- MobileNetV2
- ResNet18
- ResNet50
- DenseNet121
- EfficientNetB0
- Vision Transformer (ViT)

### Hybrid Models
- DualEffiMob-CBAM
- EffiResAttention

### Proposed Model
**FedPapVisionNet**
- Lightweight architecture
- Only **390,215 trainable parameters**
- Designed for federated environments
- Uses residual learning and attention mechanisms

## Experimental Setup
Training configuration:

- Optimizer: AdamW
- Learning rate:  
  - IID: 0.001  
  - Non-IID: 0.0005
- Batch size: 32 (IID) / 10 (Non-IID)
- Communication rounds:
  - IID: 25–200
  - Non-IID: 50
- Hardware:
    - NVIDIA RTX 4080 Super GPU
    - WSL2
           

## Results

Key results achieved:

| Method             | Accuracy      |
|--------------------|---------------|
| IID (FedAvg)       | **95.68%**    |
| Non-IID (FedProx)  | **86%**       |
| Non-IID (SCAFFOLD) | **90%**       |

The results demonstrate that **FedPapVisionNet** provides strong performance while maintaining data privacy.

## Applications
This framework can be applied in:

- Privacy-preserving medical AI
- Distributed healthcare systems
- Automated cervical cancer screening
- Federated medical image analysis

## Authors
- Chowdhury Saima Rawshan  
- Fahim Shahriar Ahmed  
- Sayani Das  
- Sadia Habib Nizhum  
- Sackline Naien Ridvi  

Department of Computer Science and Engineering  
BRAC University

## Supervisor
Md. Ashraful Alam, PhD  
Associate Professor  
BRAC University
