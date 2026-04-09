# 🧠 Brain Tumor Detection — DataSprint Hackathon

## Problem Statement
Brain MRI images ko classify karna 4 classes mein:
- Glioma Tumor
- Meningioma Tumor  
- Pituitary Tumor
- No Tumor

## Approach
- Custom CNN (3 Conv blocks) built from scratch
- Data Augmentation (flip, rotation)
- Class weighting for imbalanced data
- BatchNorm + Dropout for regularization

## Results
| Metric | Score |
|--------|-------|
| Validation Accuracy | 79.9% |
| F1 Score | 0.79 |
| Best Class | Pituitary (F1: 0.92) |

## Model Architecture
```
Input (128x128 grayscale)
    ↓
Conv2D(32) → BatchNorm → ReLU → MaxPool → Dropout
    ↓
Conv2D(64) → BatchNorm → ReLU → MaxPool → Dropout
    ↓
Conv2D(128) → BatchNorm → ReLU → MaxPool → Dropout
    ↓
Flatten → Dense(256) → Dropout
    ↓
Output (4 classes)
```

## Tech Stack
- Python
- PyTorch
- Scikit-learn
- OpenCV / PIL
- Matplotlib / Seaborn

## Competition
DataSprint — NIST University Data Science Club



## 🔗 Links
- [Kaggle Notebook](https://www.kaggle.com/code/soaebhasan/tumor-problem-datasprint-soaeba)
- [Competition](https://www.kaggle.com/competitions/datasprint)