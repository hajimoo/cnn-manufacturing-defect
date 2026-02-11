# CNN-based Manufacturing Defect Detection

## Overview
This project builds a CNN-based image classification model to detect defective products in manufacturing images.

## Motivation
In real manufacturing environments, missing defective products (false negatives) can cause significant losses.
Therefore, Recall was treated as the most important metric.

## Dataset
- Training:
  - Normal: 1102
  - Defective: 59
- Test:
  - Normal: 276
  - Defective: 15

The dataset is highly imbalanced.

## Preprocessing
- Resize to 256x256
- Normalize pixel values (0–1)
- RGB conversion
- Label encoding (0: normal, 1: defect)

## Model
- AutoKeras ImageClassifier
- Loss: Binary Cross Entropy
- Metric: Accuracy
- Validation split: 0.2
- Epoch: 3

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve

## Result
The model achieved high performance on the test set.
However, due to limited data size and possible data similarity, further validation is required.

## Future Improvements
- Data augmentation
- Class weighting
- Cross-validation
- Larger dataset collection
